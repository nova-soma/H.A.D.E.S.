# H.A.D.E.S.

**Hypothesis-Adaptive Distributed Expert System** — a framework for emergent
collective intelligence through a self-improving chorus of specialized expert
models.

> **Read the full whitepaper (styled):** https://nova-soma.github.io/H.A.D.E.S./
>
> The page above is the complete, formatted paper. The summary below mirrors its
> structure for quick reading on the repo front page.

---

## Overview

HADES is built around a *chorus* of hyper-specialized domain experts that
coordinate to produce collective intelligence no single model holds. The system
is designed for emergent capability, substrate independence, and a permanent
human-AI partnership with immutable consent protections built in at the
governance layer.

The initial Python implementation is scaffolding: enough to get the chorus
operational, populate the memory layer, and give the orchestration layer working
material to generate and validate its first major self-modification. From there
the system improves itself through a governed propose -> test -> gate -> apply
loop.

## Core ideas

- **A chorus of experts, not one model.** Durable, named domain experts each own
  a slice of capability. Work is dispatched to the experts best suited to it, and
  claims are reconciled through weighted voting rather than a single authority.
- **Self-improvement under governance.** Every change - to weights, to skills, to
  the architecture itself - originates as a hypothesis, is tested, is gated by a
  chorus vote, and only then applied. Nothing is changed speculatively or
  unilaterally.
- **Seams everywhere a part must be free to change.** A recurring pattern
  separates a fixed *framework* (the contracts and semantics the chorus is built
  against) from a swappable *method* (the concrete implementation behind it).
  This applies to transport vs. trust, the serving and weight-modification
  backend, the operator signature scheme, and the communication layer.
- **Two-speed knowledge.** Facts live in a retrievable, revisable memory layer;
  skills consolidate into weights and are effectively permanent. Forgetting a
  fact is a memory operation; unlearning a skill is not.
- **A human partner, by design.** The human participates in governance as a
  distinct authority through an off-bus operator seat with cryptographically
  signed ballots. Architecture changes require both a chorus supermajority and
  explicit operator consent, and the operator can never be changed out from under
  itself.

## Architecture at a glance

- **Expert layer** - the chorus of specialized models that do the reasoning.
- **Memory layer** - versioned, governed shared and personal stores.
- **HERO** - hypothesis engine, routing, and orchestration.
- **Communication seam (Iris)** - the systems that govern how messaging behaves,
  with the wire transport swappable behind the seam.
- **Governance and meta-architecture** - voting, the operator seat, and the
  recursive self-improvement rules, including a backup-and-recovery requirement
  for any change to a critical system.
- **Specialist experts** - named experts for screening, trust, defense,
  consolidation, lifecycle, goal coordination, health, and more.

## Status

This is a design-stage research project. The whitepaper is a living document and
the curated mid-level overview of the architecture; design docs hold the detailed
history, and source code is ground truth where the two diverge.

## License

HADES is dual-licensed under the GNU Affero General Public License v3.0
(AGPL-3.0) and the Server Side Public License. Copyright (c) 2026 Nova soma
labs, LLC. See the whitepaper's license section for full terms.
