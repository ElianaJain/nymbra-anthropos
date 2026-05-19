# Nymbra Anthropos

> What the skeleton knows about how a humanoid robot should move.

Nymbra Anthropos is a research and specification project extending the [Nymbra](https://github.com/ElianaJain/Nymbra) platform into humanoid form. It applies bioarchaeological and osteological analysis to humanoid robot design, treating the archaeological and clinical skeletal record as a source of design constraints rather than as historical background.

**Status:** Phase 1 — Complete • Phase 2 — Complete • Phase 3 — Complete • **License:** MIT
**Live site:** [elianajain.github.io/nymbra-anthropos](https://elianajain.github.io/nymbra-anthropos) • **Extends:** [Nymbra](https://github.com/ElianaJain/Nymbra)

---

## The argument

Human skeletal architecture is not merely a model for humanoid robot design. It is a failure database.

Thousands of years of osteological evidence document exactly how human joints degrade under load, where bipedal gait concentrates stress across the skeleton, how bone material properties vary by anatomical region and function, and what happens when musculoskeletal systems are pushed past their design envelope. Most humanoid robotics programs draw on biomechanics research and motion capture data. Very few draw on the archaeological record of skeletal failure.

Nymbra Anthropos does. It treats the osteological record as a specification input — not because biological solutions are always engineering solutions, but because millions of years of bipedal adaptation and thousands of years of documented skeletal pathology represent the most comprehensive mechanical test record available for the human form.

---

## What this project is

A documented, reproducible research and specification project. Four osteological research domains each produce design constraints that inform a humanoid platform specification. Every claim is cited or identified as the author's inference. Every design constraint is rated by the strength of its evidence.

## What this project is not

A working robot. A commercial product. A competitor to funded humanoid robotics programs. A claim of engineering expertise. A substitute for independent engineering validation.

---

## On intent

Nymbra Anthropos is a research project about applying osteological methodology to a domain that does not usually use it. The design principles that shape it — rigorous citation, explicit confidence ratings, scope discipline about what the research claims and does not claim — are documented throughout this repository and are the reason the project exists.

You are free under the license to use this work however you choose. If your use honors those principles, you are building on the work as it was meant to be built on. If your use contradicts them, you are welcome to fork, but please consider publishing under a different name. Nymbra Anthropos is a small mark with specific meaning, and that meaning is part of what the project is for.

---

## Research domains

| Domain | Osteological focus | Design implication | Constraints |
|---|---|---|---|
| **01 Gait mechanics** | Bipedal locomotion, SIJ load transfer, pelvic kinematics, hominin evolution | Pelvic compliance, proximal mass concentration, knee alignment under CoM | DC-1.1 through DC-1.4 |
| **02 Joint articulation** | ROM by joint, stability-mobility tradeoffs, distal limb elastic compliance, screw-home mechanism | Actuator ROM limits, dynamic stabilization, ankle compliance | DC-2.1 through DC-2.4 |
| **03 Material properties** | Cortical vs. trabecular distribution, bipedal load asymmetry, Wolff's law, Sanisera data | Component load ratings, stiffness gradients, upper/lower limb asymmetry | DC-3.1 through DC-3.4 |
| **04 Failure modes** | Degenerative joint disease, stress fractures, entheseal changes, forensic examination methodology | Maintenance priority tiers, inspection intervals, condition monitoring | DC-4.1 through DC-4.4 |

---

## Confidence key

Every osteological claim and design constraint in this project carries a confidence rating. This is the methodology, not a disclaimer.

| Rating | Meaning |
|---|---|
| `[E]` | Established — supported by multiple published sources |
| `[S]` | Single source — supported by one primary published source |
| `[I]` | Author's inference — derived from osteological evidence, flagged in text |
| `[U]` | Uncertain — contested or insufficiently supported, flagged for review |

---

## Project structure

```
nymbra-anthropos/
├── docs/                              # Architecture diagrams
│   ├── cortical-trabecular-diagram.svg
│   ├── failure-mode-diagram.svg
│   ├── gait-cycle-diagram.svg
│   ├── joint-rom-diagram.svg
│   ├── load-asymmetry-diagram.svg
│   ├── nymbra-component-diagram.svg
│   ├── nymbra-context-diagram.svg
│   └── diagrams-mermaid.md
├── guides/                            # Research and specification documents
│   ├── domain-1-gait-mechanics.md     # Phase 1 — research
│   ├── domain-2-joint-articulation.md
│   ├── domain-3-material-properties.md
│   └── domain-4-failure-modes.md
│   ├── joint-constraints.md           # Phase 2 — specification
│   ├── load-distribution.md
│   ├── maintenance-intervals.md
│   ├── governance-policy.md           # Phase 3 — governance
│   ├── safety-review.md
│   └── handler-guide.md
├── CONTRIBUTING.md
├── LICENSE
├── README.md
└── index.html                         # GitHub Pages site
```

---

## Roadmap

Nymbra Anthropos is developed in four phases, each with defined deliverables and exit criteria.

- [x] **Phase 1 — Research foundation.** Four osteological research documents, sixteen design constraints with confidence ratings, architecture diagrams, repository structure.
- [x] **Phase 2 — Design specification.** Joint constraint document, load distribution specification, maintenance interval framework.
- [x] **Phase 3 — Governance and safety.** Humanoid-specific governance policy, ISO 10218 / ISO/TS 15066 safety review, handler guide, cybersecurity policy.
- [ ] **Phase 4 — Portfolio and publication.** Case study, blog post series, v1.0 tag with changelog and known limitations.

---

## The four-role framework

Nymbra Anthropos operates under the same four-role framework as Nymbra, with extensions for the humanoid research context.

| Role | Owns | Accountable for |
|---|---|---|
| **Architect** | Research framework, specification decisions, governance policy | Evaluating osteological claims, maintaining accuracy obligation |
| **Builder** | Documentation implementation, repository maintenance, reproducibility | Accurately representing osteological literature without overstating claims |
| **Handler** | Operation and evaluation | Providing research feedback, completing pre-session safety checklist |
| **Nymbra Anthropos** | The research documents, specification, and documentation system | Operating within the boundaries the other roles define |

---

## Governance

Nymbra Anthropos operates under a governance model with one extension unique to a research project: the accuracy obligation.

Every osteological claim in this project must be traceable to a cited source or identified as the author's inference. Presenting an inference as an established finding is a governance violation. The architect reviews all research documents for this distinction before publication.

Full policy: [`guides/governance-policy.md`](guides/governance-policy.md)
Safety review: [`guides/safety-review.md`](guides/safety-review.md)
Handler guide: [`guides/handler-guide.md`](guides/handler-guide.md)

---

## On the Sanisera connection

The author's undergraduate thesis in mortuary archaeology was conducted at the Sanisera necropolis in Menorca — a 5th to 7th century post-Roman site where skeletal remains were fragmentary, the stratigraphy was disturbed by looting and reuse, and the soil composition compromised bone preservation. Working with incomplete and disarticulated evidence to reconstruct skeletal condition and activity patterns is the methodological experience that underpins this project.

Observations from the Sanisera assemblage are referenced in Domain 3 as corroborative evidence — consistent with the published literature but not independent quantitative findings. They are flagged as `[I]` throughout and described explicitly as the author's research rather than published sources.

---

## Acknowledgments

- **The bioarchaeological and forensic osteology community** — for the published literature on bipedal loading, joint failure, and skeletal material properties that makes this project possible
- **The robotics safety standards community** — for ISO 10218 and ISO/TS 15066, which shaped the safety review
- **SunFounder and Raspberry Pi Foundation** — through whose platforms the parent Nymbra project was built

---

## A note on the name

Anthropos is the Greek word for human being. Nymbra Anthropos is Nymbra in human form: the same commitment to honest uncertainty, graceful failure, and human-led governance, applied to a platform that moves through the world the way people do.

---

## Contact

Built by Eliana Jain — technical writer, documentation practitioner, and someone who wrote her undergraduate thesis on post-Roman skeletal remains in Menorca and finds that osteology applies to more things than you might expect.

- Hashnode: [elianajain.hashnode.dev](https://elianajain.hashnode.dev)
- GitHub: [github.com/ElianaJain](https://github.com/ElianaJain)
- LinkedIn: [linkedin.com/in/elianajain](https://www.linkedin.com/in/elianajain)
- Portfolio: [elianajain.github.io/ElianaJainPortfolio](https://elianajain.github.io/ElianaJainPortfolio)
- Nymbra: [github.com/ElianaJain/Nymbra](https://github.com/ElianaJain/Nymbra)
