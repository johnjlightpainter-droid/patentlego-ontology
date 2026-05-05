# PatentLEGO Ontology

**A universal, open vocabulary for decomposing patents into functional building blocks — and mapping how they connect into systems.**

> *"An AI that turns patents into LEGO blocks — and shows you how to build with them."*

---

## What This Is

Patent databases are full of knowledge that no one can use.

Not because the knowledge is secret — but because it's buried in legal language, siloed into individual records, and organized around *ownership* rather than *function*. There is no standard for describing what a patent actually **does**, what it **needs**, what it **produces**, or how it might **connect** to other patents to form something useful.

The PatentLEGO Ontology is an attempt to build that standard.

It defines a structured vocabulary for tagging any patent as a functional **block** — with typed inputs, typed outputs, purpose categories, energy roles, scale, domain, and explicit connection points. When blocks are tagged consistently, a matching engine can identify when the output of Patent A is compatible with the input of Patent B, and suggest systems that no one has assembled yet.

This ontology is the foundation. The matching engine, the visual system builder, the community tagging effort — all of it depends on how well this vocabulary captures what patents actually *do*.

---

## Current Version

**v0.1 — Public Draft for Community Review**
Released: May 2026
Author: John J. "The Light Painter"
License: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

---

## Core Concepts

### The Patent Block

Every patent is decomposed into a `PatentBlock` with:

| Field | Description |
|-------|-------------|
| `id` | Patent number (e.g., US2025123456A1) |
| `plain_title` | Plain-English title |
| `purpose` | One-sentence problem statement |
| `purpose_category` | Controlled vocabulary (GEN, STORE, CONVERT, DISTRIBUTE, etc.) |
| `inputs` | Typed list of what the patent needs to operate |
| `outputs` | Typed list of what the patent produces |
| `energy_balance` | Net energy role (producer, consumer, transformer, etc.) |
| `scale` | Operational scale (personal, residential, industrial, etc.) |
| `domain` | Technical domain (MECH, ELEC, THERM, BIO, etc.) |
| `connection_points` | Explicit attach points for other blocks |
| `confidence_score` | 0.0–1.0 tagging confidence |

### Purpose Categories

| ID | Category | Plain Definition |
|----|----------|-----------------|
| GEN | Generate | Creates or harvests a resource |
| STORE | Store | Retains a resource for later use |
| CONVERT | Convert | Transforms one resource type into another |
| DISTRIBUTE | Distribute | Moves a resource from one point to another |
| CONTROL | Control | Regulates, monitors, or modulates a process |
| STRUCTURE | Structure | Provides physical support or enclosure |
| SENSE | Sense | Detects or measures a condition |
| INTERFACE | Interface | Connects two systems that wouldn't otherwise couple |
| TREAT | Treat | Purifies or processes a resource |
| EMIT | Emit | Produces a signal, field, or radiative output |
| COMPUTE | Compute | Processes information |
| ACTUATE | Actuate | Converts a signal into physical action |

### System Templates

Predefined connection patterns that recur across domains:

| Template | Pattern | Example Context |
|----------|---------|-----------------|
| SYS-GEN-STORE-DIST | GEN → STORE → DISTRIBUTE | Off-grid power, rainwater catchment |
| SYS-SENSE-CTRL-ACT | SENSE → CONTROL → ACTUATE | Robotics, smart home automation |
| SYS-CONV-STORE-CONV | CONVERT → STORE → CONVERT | Hydrogen energy storage |
| SYS-TREAT-STORE-DIST | TREAT → STORE → DISTRIBUTE | Water purification |
| SYS-SOURCE-TREAT-USE-TREAT | Closed loop | Greywater recycling |
| SYS-EMIT-SENSE-PROCESS | EMIT → SENSE → COMPUTE | LiDAR, radar, ultrasound imaging |

---

## Example: A Fully Tagged Block

```json
{
  "id": "US2025123456A1",
  "plain_title": "Solar panel powers a dehumidifier that pulls water from air and filters it",
  "purpose": "Produce potable water from ambient air using only solar energy",
  "purpose_category": "GEN",
  "inputs": [
    { "type": "energy.radiative", "subtype": "solar_irradiance", "specification": ">400 W/m²", "optional": false },
    { "type": "fluid.gas", "subtype": "air_ambient", "specification": ">30% RH, 15-45°C", "optional": false }
  ],
  "outputs": [
    { "type": "fluid.liquid", "subtype": "water_potable", "specification": "<50 TDS, WHO standard", "is_primary": true },
    { "type": "waste.thermal", "subtype": "heat_rejected", "specification": "~35°C exhaust", "is_waste": true }
  ],
  "energy_balance": "consumer",
  "scale": "residential",
  "domain": ["THERM", "AQUA", "ELEC"],
  "confidence_score": 0.92,
  "review_status": "community_reviewed"
}
```

This block connects to: **STORE** (water tank) → **DISTRIBUTE** (drip irrigation) → **SENSE** (soil moisture) → **CONTROL** (valve controller) — five patent blocks, one working off-grid irrigation system.

---

## Roadmap

### v0.1 (Current)
- [x] Core block structure
- [x] Purpose category vocabulary (12 categories)
- [x] Input/output taxonomy with direct-match subtype mirroring
- [x] Energy balance classification
- [x] Scale and domain vocabularies
- [x] Connection type taxonomy
- [x] System templates (6 patterns)
- [x] Confidence and community review flags

### v0.2 (Planned)
- [ ] Temporal constraints (time-of-day availability, warm-up requirements)
- [ ] Geographic constraints (climate, latitude, elevation)
- [ ] Safety and hazard flags
- [ ] Cost/complexity tiers (DIY → Lab-grade)
- [ ] Interoperability standards (ISO, IEEE, ANSI)
- [ ] TRL (Technology Readiness Level) 1–9
- [ ] License/openness flags (expired patents, known thickets)

### Future
- [ ] Reference validator (Python script for block consistency checking)
- [ ] Community tagging guide
- [ ] Seed dataset: 50 hand-tagged well-known patents
- [ ] Matching engine specification

---

## How to Contribute

This ontology improves through use. The fastest way to find gaps is to try tagging real patents with it and notice where the vocabulary breaks down.

**Ways to contribute:**
- **Tag a patent.** Use the block structure to tag any patent you know well. Submit as a pull request or open an issue.
- **Dispute a category.** If a controlled vocabulary term doesn't capture something real, open an issue explaining what's missing and why.
- **Propose an extension.** New input/output subtypes, new system templates, new connection types — all welcome.
- **Review existing tags.** Community review raises `confidence_score` and `review_status`. Any expert eyes on a tagged block are valuable.

**Ground rules:**
- Attribute the ontology per CC BY-SA 4.0 if you build on it
- Keep the vocabulary as minimal as possible — resist adding categories that can be expressed as combinations of existing ones
- All disputes welcome; personal attacks are not

---

## License

**Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**

You are free to share and adapt this material for any purpose, including commercial use, as long as you give appropriate credit to the original author and distribute any derivative works under the same license.

[Full license text](https://creativecommons.org/licenses/by-sa/4.0/legalcode)

---

## Author

**John J. "The Light Painter"**
Artist, inventor, systems thinker.
May 2026

*This ontology is dedicated to everyone who ever had a good idea and no way to know it had already been half-built by three other people.*
