# patentlego-ontology
An open vocabulary for decomposing patents into functional building blocks and mapping how they connect into systems. CC BY-SA 4.0.
I Built the Vocabulary That Patent AI Is Missing — And I'm Giving It Away
I'm not a software engineer. I'm not a patent attorney. I'm an artist who makes illuminated signs out of layered acrylic and dichromatic film.
But I've spent a long time thinking about how things connect — how light passes through layers, how systems work together, how pieces that were made independently can combine into something none of them could do alone.
A few weeks ago, I started thinking about patents the same way.

The Problem Nobody Talks About
Patent databases contain an extraordinary amount of human ingenuity. Decades of solved problems, tested mechanisms, documented innovations — all of it technically public, all of it technically accessible.
And almost none of it usable.
Not because it's secret. Because it's organized wrong.
Patent databases are organized around ownership. Who filed. When. What claim they're making. But they don't answer the question an inventor actually needs:
"What already exists that could be a piece of what I'm trying to build?"
More specifically: if Patent A produces something, and Patent B needs that something as an input — that's a connection. That's a system waiting to be assembled. But no tool on earth will show you that connection today, because there's no shared vocabulary for describing what patents do at a functional level.
That's the gap I wanted to close.

What I Built
I wrote a patent ontology.
An ontology is a structured vocabulary — a way of describing things so consistently that a machine (or a person, or a community) can reason about relationships between them.
The PatentLEGO Ontology v0.1 defines a standard way to decompose any patent into a functional block with:

Purpose — what problem does it solve? (12 controlled categories: Generate, Store, Convert, Distribute, Control, Sense, Treat, Actuate, and more)
Inputs — what does it need to operate? (typed by resource: energy, fluid, material, signal, field)
Outputs — what does it produce? (same types, so outputs of one block can be directly matched to inputs of another)
Energy role — is this a producer, consumer, transformer, or storage unit?
Scale — personal? residential? industrial? municipal?
Domain — mechanical, electrical, thermal, biological, chemical?
Connection points — where can other patent blocks attach?

When patents are tagged consistently with this vocabulary, a matching engine can find when the output of Patent A is compatible with the input of Patent B — and suggest systems no one has assembled yet.

What This Makes Possible
Here's a simple example.
You're building an off-grid water system. You enter your concept. The tool finds:

Patent A — generates water from atmospheric humidity using solar energy (GEN)
Patent B — stores potable water with gravity-fed pressure (STORE)
Patent C — distributes water through drip irrigation with flow control (DISTRIBUTE)
Patent D — senses soil moisture and triggers valve control (SENSE → CONTROL)

Five blocks. One working system. Built from patents that were already public — just never connected.
That's what this ontology makes possible once someone builds the matching engine on top of it.

Why I'm Publishing It Openly
I could try to commercialize this. The concept brief is written. The ontology is structured enough that a developer could start building on it tomorrow.
But I keep coming back to something I believe at a level that's hard to argue with:
Humanity cannot move forward with knowledge that is gatekept.
The patent system already slows innovation by locking up ideas. An open standard for navigating that system — for finding the connections the system was never designed to surface — belongs to everyone.
So I'm publishing the PatentLEGO Ontology v0.1 under CC BY-SA 4.0. Free to use, free to build on, free to adapt — as long as you share what you make the same way.
If you build a tool on this ontology, your tool gets to carry the same openness forward. That's the deal. I think it's a fair one.

What I'm Asking For
I'm not a developer. I can't build the matching engine or the visual system builder myself — not right now, not with everything else on my plate.
What I can do is release the foundation and trust that the right people will find it.
If you're a developer, a researcher, a patent attorney, a systems thinker, or an inventor who sees what this could become:

Read the full ontology on GitHub (link coming)
Tag a patent using the block structure and submit it
Open an issue if the vocabulary breaks down on something real
Build something and tell me about it

This is v0.1. It will have gaps. The gaps are the contribution — find them, name them, and help close them.

One Last Thing
The one-line pitch for the tool this ontology enables:
"An AI that turns patents into LEGO blocks — and shows you how to build with them."
I came up with that because it's how I think about my own work. Every piece I make is a system of layers — light, film, acrylic, color, angle — that only becomes something when they're assembled in the right order.
Patents are the same. The knowledge is already there. Someone just needs to show people how to build with it.
I'm hoping that someone is reading this right now.

John J. "The Light Painter"
Artist. Sign maker. Systems thinker.
May 2026
PatentLEGO Ontology v0.1 — CC BY-SA 4.0 — GitHub link coming soon
