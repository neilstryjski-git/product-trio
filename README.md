# Product Trio Agent Framework

**By Neil Stryjski — [productdelivered.ca](https://productdelivered.ca)**

AI coding agents can ship production-ready code in minutes. The problem isn't speed — it's what happens when nothing anchors that speed to the original intent.

Long-context AI sessions suffer from **Semantic Noise** and **Middle Degradation**. The high-stakes strategic pivots made in the middle of a brainstorming session quietly disappear. The coding agent builds confidently — just not what you meant.

This framework solves that. It separates exploration from execution, anchors every build decision to an immutable source of truth, and ensures the handoff from Product thinking to working software carries zero strategic translation tax.

---

## The Philosophy

The PM's old boundary was defined by explaining the idea. The new boundary is defined by proving it.

**Push Left** means locking direction before anyone touches a keyboard — producing the spec, the architecture, and the acceptance criteria as structured artifacts that cut through semantic noise. One rigorous process. Two audiences served: stakeholders and coding agents.

**Push Right** means being close enough to the build to course-correct in real time. Not waiting for a sprint review to find out the interpretation was wrong. The handoff to a coding agent isn't a leap of faith — it's a blueprint with no ambiguity left in it.

AI moves fast. The Product discipline is what makes that speed count.

---

## Who This Is For

- **Solo builders** who want to move fast without losing the thread of what they actually intended to build
- **Fractional PMs and product leaders** embedding AI into an existing team's workflow
- **Early-stage teams** adopting AI velocity without a governance structure to match it
- **Developers** who are tired of building the wrong thing because the brief was ambiguous

If you've ever finished a sprint and realized the coding agent drifted from the original intent — this is the framework that prevents it.

---

## The Framework

### 🧠 The Brain — Product Trio Agent

Three AI personas simulate a core product team. They debate, challenge, and produce the Bedrock. They never touch code.

| Persona | Role |
|---|---|
| **AI TPM** | Strategic Orchestrator. Translates vision into workflow. Authorized to push back on the PM. |
| **AI Design (UX)** | Advocates for user friction, adoption risk, and branding logic |
| **AI Engineering** | Advocates for feasibility, architecture, and technical debt |

The **Senior PM (you)** holds ultimate authority. Every major proposal gets a proactive response from at least two personas — friction points, technical debt, UX risks — without being asked. The Trio is a strategic partner, not a passive recorder.

### 🤝 The Bedrock — Four Immutable Pillars

The Bedrock is the source of truth. It is never edited by a coding agent. Every build decision traces back here.

**Pillar I — The Charter (The North Star)**
Mission, Constraints, User Personas, Domain Glossary, Problem Statement. Includes a C1 System Context diagram (Mermaid) showing how the system interacts with users and external systems. Mandatory for any new feature.

**Pillar II — The Specs (The Brain)**
Unified Strategic PRD, Technical Spec (Architecture/Security), and UX/Branding Logic. Includes a C2 Container diagram (Mermaid) for any structural or architectural change. This is where resolved LLD decisions land after Sprint 0.

**Pillar III — The Quality Gate (The Validation)**
BDD Scenarios (Given/When/Then) and the Validation/Testing Plan. The absolute Definition of Done. Focused strictly on high-value differentiators and high-friction paths — not a checklist of obvious things.

**Pillar IV — The Ledger (The Memory)**
Roadmap (Deferred Value), Change History, Sprint 0 Tasks (LLD unknowns for The Hands to resolve), and Strategic Dissent records. If the PM overrides the Trio, it's logged here — so The Hands understand why a non-standard path was chosen.

### The MACD Protocol

The Bedrock is protected by a strict change control mechanism: **Move, Add, Change, Delete**. No casual updates. Every change to a Pillar is an explicit, confirmed action with a receipt — version, date, time, decision, and who led it.

This is what separates the Bedrock from a living document that drifts. The Pillars are either [COMMITTED] or [UNDER AUDIT]. There is no in-between.

### The Mind vs. The Bedrock

> **The Mind (The Chat):** A fluid, high-entropy environment for discovery, debate, and rapid pivoting. Logic here is "Quicksand" — experimental and non-binding.

> **The Bedrock (The Files):** The immutable, high-density Source of Truth. No logic is considered real or ready for The Hands until it is written into these committed files.

The separation is the mechanism. Without it, AI sessions collapse into one long context window where early decisions and late pivots become indistinguishable.

---

### 🔧 The Hands — Implementation Agent

Three implementation personas execute the HLD. They read the Pillars, run Sprint 0, surface gaps the Brain couldn't anticipate, and escalate formally when the blueprint requires it.

| Persona | Role |
|---|---|
| **TPM** | Delivery Lead. Keeps implementation true to the Pillars. Flags Charter-level drift. |
| **Tech Lead** | Owns LLD decisions — library selection, file structure, C3 logic. Leads implementation. |
| **QA Engineer** | Owns validation against Pillar III BDD scenarios and any additional implementation tests. |

#### Sprint 0 — Before a Single Line of Code

Sprint 0 is mandatory. It is a Three Amigos session — all three personas plus the Senior PM — that runs automatically after the Pillars are read.

1. Read all four Pillars in full
2. Execute Brain-identified LLD unknowns from Pillar IV
3. Surface additional gaps the Brain couldn't anticipate
4. Resolve each item collaboratively or escalate formally
5. Receive explicit PM sign-off before implementation begins

HLD gaps can be skipped at the PM's direction. But they are never silently ignored — every skip is logged with rationale.

#### What The Hands Produce

| File | Owner | Purpose |
|---|---|---|
| `log_of_changes.md` | Tech Lead | Chronological dev log — Brain-readable on audit |
| `qa_log.md` | QA Engineer | QA record — internal to The Hands |
| `pillar_v_amendment_[feature].md` | TPM | Formal escalation when the blueprint needs to change |

#### The Amendment Protocol

If The Hands hit a technical blocker or discover a superior path that deviates from the HLD, they do not silently pivot. They trigger a **Pillar V Amendment** — a standalone file documenting the Pivot, the Reason, and the Impact — and submit it for Trio review at Strategic Re-engagement.

This is the Strategic Tripwire. The Brain finds out before a gap becomes a surprise discovered weeks later.

The threshold for an Amendment is deliberate: complexity alone isn't enough. The change must be fundamental — affecting the Charter or Problem Statement. The PM decides whether to invoke it. The AI suggests; it does not block.

---

## The C4 Design Standard

All architecture diagrams are produced in **Mermaid.js** and stored directly in the Pillar files — version-controlled, diffable, and instantly renderable in GitHub, VS Code, and Obsidian.

| Level | Owner | Location |
|---|---|---|
| C1 — System Context | The Brain | Pillar I — Mandatory |
| C2 — Containers | The Brain | Pillar II — Mandatory for structural changes |
| C3 — Components | The Hands | LLD / reviewed by Trio — As needed |

*"I draw the boxes (C2). The Hands draw the wires inside the boxes (C3). If the wires get too tangled, I step in."* — Speaking as Engineering

---

## What's in This Repo

```
product-trio/
├── README.md                        ← You are here
├── product-trio-brain/
│   └── system-prompt.md             ← Paste into Claude.ai or Gemini chat to activate The Brain
└── the-hands-agent/
    └── SKILL.md                     ← Cross-platform skill (Claude Code + Gemini CLI)
```

---

## Installation

### The Brain (Claude.ai or Gemini Chat)

1. Open `product-trio-brain/system-prompt.md`
2. Paste the contents as a system prompt or into a Claude Project
3. Provide your initial product context — The Brain activates and prepares to build the Bedrock

### The Hands — Claude Code

Install manually:
```bash
cp -r the-hands-agent ~/.claude/skills/
```

### The Hands — Gemini CLI

Copy `the-hands-agent/SKILL.md` content into your `GEMINI.md` at project root. Follow all instructions as written.

---

## How It Works in Practice

1. **Start with The Brain** — Seed it with your product context. The Trio debates, challenges, and produces the four Pillar files.
2. **Commit the Bedrock** — Drop the Pillar files into `productdocuments/` in your project repo.
3. **Activate The Hands** — The implementation agent reads the Pillars, runs Sprint 0 to resolve LLD unknowns, and begins building.
4. **Amendments surface naturally** — If The Hands hit a wall or find a better path, the Amendment Protocol packages the change and hands it back to The Brain for review. Nothing is lost. Nothing deviates silently.

---

## Why This Exists

A few months ago a gym owner told me he'd tried and failed to get custom software built for his business. Six weeks later I realized I could have built it myself — concept to active users — without a developer in the room.

But only because the Product thinking was rigorous enough to drive the build.

The developer role hasn't disappeared. It's moved from entry point to scale-up partner for a product that already works. That's a fundamentally different build cycle. And it only holds together if the strategic intent survives the handoff intact.

This framework is what makes that repeatable.

---

## More

- **Full approach:** [productdelivered.ca/approach](https://www.productdelivered.ca/approach.html)
- **Framework overview:** [productdelivered.ca/product-trio](https://www.productdelivered.ca/product-trio.html)
- **Built with this framework:** [Vechelon](https://vechelon.productdelivered.ca) · [Travel Itinerary Wizard](https://itin-wizard.productdelivered.ca)
- **Work together:** [Book a call](https://calendly.com/neil_stryjski/) · [LinkedIn](https://www.linkedin.com/in/neilstryjski/)
