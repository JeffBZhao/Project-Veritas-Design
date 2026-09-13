# Project Veritas

> A Decentralized Platform for Rational Deliberation · Public Design Whitepaper

[中文版 (Chinese Version)](./README.md)

This repository is a public record of the core design of **Project Veritas**, established to timestamp and attribute authorship. Project source code is hosted in a separate repository (link may be added here if applicable).

This document is licensed under [CC BY 4.0](./LICENSE) — you are welcome to cite, discuss, and build upon this work, provided the original design is credited.

---

# Project Veritas — Design Whitepaper

**Designer: JeffBZhao**
**First published: 2026-Aug-02**
**Version: v1.1 (added Real-Person Verification section)**

> Copyright & attribution notice: The core mechanism designs described in this whitepaper (the atomic topic structure, the AP energy-point economy, the reputation and jury system, the tiered real-person verification framework, graph-based visualization, the AI logic-deconstruction pipeline, cross-language resonance mechanisms, etc.) are original concepts created by JeffBZhao. You are welcome to cite, discuss, and build derivative work from this design, but please credit the original source in any citation, reproduction, or derivative work.

---

## Abstract

Project Veritas is a design proposal for a decentralized platform for rational public deliberation. Its core goal is to counter emotional polarization and the spread of misinformation online by replacing "engagement/virality" with "logical topology" as the organizing principle of public discourse. The platform itself does not adjudicate what is true — it only safeguards the rigor of the argumentation process. The judgment of truth and falsehood always remains with the participants; what the platform provides is a structure that allows that judgment to be well-organized and clearly presented.

---

## 1. Core Vision

The traditional "post and comment" structure of social media inherently rewards emotional, instantaneous reactions and engagement-driven algorithmic amplification, leading to fragmented and polarized public discourse. Project Veritas proposes an alternative structure: **Everything is a Topic** — every piece of substantive argument is, by design, an independent node that can be cited, verified, and rebutted, rather than a comment buried in a thread.

The platform positions itself as **the guardian of process**, not the arbiter of truth.

## 2. A Flat Topic Network

- The traditional post-and-nested-comment model is abolished. Any stance a user takes must be attached to an explicit, structured reason.
- Users can spend resources to create a new argument, or cite an existing high-value argument at zero cost. This design is intended to discourage redundant re-litigation of the same point and to encourage the reuse and accumulation of argumentation, rather than the unbounded creation of noise.

## 3. The Action Points (AP) & Reputation Economy

In the absence of centralized moderation, the platform relies on a self-contained economic constraint to suppress bot activity and low-cost spam:

- **Reputation Score**: Accrues slowly over time through recognition from other users. It determines a user's action-point ceiling and serves as the threshold for entry into higher governance roles (e.g., the jury).
- **Action Points (AP)**: A daily-replenishing action budget. Different actions (creating a new topic, posting an argument, voting, citing an existing argument, etc.) consume different amounts of AP, and citing existing content is deliberately made far cheaper than creating new content — structurally nudging users toward reusing existing argumentation rather than fragmenting the discourse further.

The underlying philosophy: **free speech does not mean speech at zero cost**. Replacing human moderation with economic constraints is a more decentralized form of governance, and one that is harder for any single actor to unilaterally manipulate.

## 4. Real-Person Verification: A Tiered Trust System

The decentralized reputation and jury system rests on one precondition: an account must correspond to a real, unique individual — not an entity that can be cloned indefinitely. If the cost of creating an account is zero, penalties to a reputation score carry no real deterrent, and jury votes can be manipulated at scale by armies of puppet accounts. The platform therefore preserves space for anonymous participation while introducing a tiered real-person verification framework as the first line of defense against Sybil attacks and coordinated inauthentic behavior ("astroturfing").

Because "reach" and "privacy protection" are goals that often pull in opposite directions, the platform adopts a dual-track verification strategy rather than mandating a single method:

- **Privacy-first track**: Uses zero-knowledge-proof-based biometric verification services (in the manner of World ID). This proves only that "this is a unique real person," without requiring a name or government ID. This track appeals to privacy-sensitive users and aligns well with the platform's decentralized ethos, though such services currently have limited global reach.
- **Traditional KYC track**: A mature third-party identity verification provider (in the manner of Stripe Identity) matches a government-issued ID against a user selfie. The platform's own servers never store any ID images or real names — they receive only a verification-passed token and a unique hash used to prevent duplicate registrations from the same identity.

Users who complete neither track are not excluded from the platform, but operate under constrained permissions: their reputation score is locked at the lowest tier, their daily AP replenishes slowly, they cannot serve on a jury or initiate formal motions, and access to high-cost features such as the AI logic-deconstruction tool is tightly rate-limited. Completing either verification track grants a user a baseline reputation score, restores their daily AP to the normal rate, and unlocks eligibility to be randomly selected for jury duty and to participate in higher tiers of governance.

The underlying logic: **anonymous participation is not prohibited, but it inherently carries a higher trust cost** — real governance power is reserved for accounts that have proven themselves to be a distinct individual.

## 5. Dynamic Graph Visualization

Abstract logical exchanges are visualized as a dynamic "nebula" graph:

- Supporting, opposing, and extending arguments are rendered with distinct colors and edge styles.
- Nodes that have been debunked or that violate platform rules enter a translucent "ghost state" rather than being deleted outright, preserving the traceability of the process.
- Node size is rendered using absolute, backend-computed values rather than pure frontend relative scaling, avoiding the loss or visual distortion of long-tail content that relative scaling tends to cause.

## 6. Cross-Language "Parallel Universes" and "Resonance Wormholes"

Different language communities are deliberately isolated into independent content pools, avoiding pointless conflict driven purely by language barriers. At the same time, the backend computes semantic similarity to identify topics in different language communities that are, at their core, discussing the same underlying logic, and connects them visually via a "wormhole." This lets users see that people across different cultures and languages may be arguing about the very same underlying issue.

## 7. The AI Gatekeeper and Cost-Aware Rationality Controls

The platform uses AI assistance to reduce the cost of human moderation and improve discussion quality:

- **Semantic deduplication**: Uses vector similarity to identify duplicate topics, nudging users to cite rather than re-post, reducing fragmentation.
- **Logic diagnostics**: Objectively evaluates newly posted content for inflammatory language or clear logical fallacies — evaluating the *quality of the argument*, not the correctness of the stance.
- **Usage quotas**: Each user's daily quota of AI-assisted calls is capped (and tied to the verification tier described in Section 4). This is both a realistic constraint on operating costs and a structural defense against automated abuse.

## 8. Decentralized Adjudication and Recusal

Rather than a centralized content arbiter, the platform introduces a decentralized dispute-resolution mechanism:

- When a topic is flagged for fabricated evidence, personal attacks, or similar violations, the system randomly selects users who meet the reputation threshold to form a **blind jury**, who render a verdict without visibility into each other's or the parties' identities.
- **Conflict-of-interest recusal**: The plaintiff, the defendant, and jurors who took part in the initial trial automatically lose their voting rights in any subsequent public review of that case, preventing the same group from repeatedly controlling the outcome.
- When public objection to a verdict significantly exceeds public agreement (beyond a set multiple), a higher-tier review is triggered, providing a correction path for potential misjudgment.

## 9. Tiered Evidence Grading

The platform grades the sources cited in an argument rather than treating all sources as equal — ranging from pure logical inference, to a single self-published source, to mainstream media and full video documentation, up to cross-verified academic and court-level documents. Different evidence tiers receive markedly different visual weight in the interface: weak evidence is collapsed by default, strong evidence is highlighted by default. The goal is to let a reader instantly perceive how solid the evidence behind a claim actually is, without the platform making that judgment on the reader's behalf.

## 10. Logic Deconstruction: From Long-Form Text to an Argument Tree

For the long-form persuasive essays common online, the platform provides an AI-assisted deconstruction pipeline: a piece of natural-language text is decomposed into underlying premises, inference relations (AND/OR logic gates), and a final conclusion. Each premise is linked to any existing fact-checks on the platform. If a premise is debunked, the entire logic chain and conclusion that depend on it are clearly flagged as "circuit-broken" — letting a reader see, at a glance, exactly how solid the foundation beneath a long essay's conclusion actually is.

## 11. Community Governance and Open-Source Strategy

The platform's long-term governance vision does not chase traditional search-engine traffic; instead, it relies on visually compelling graph content spreading organically across social platforms. Incentives for code contributors are deliberately decoupled from judicial/adjudication authority (technical skill is not equivalent to fairness in judgment); contributors are instead rewarded with public recognition and higher participation quotas, preserving a clear boundary between procedural justice and technical contribution.

---

## Conclusion

Project Veritas attempts to answer a specific question: **if a platform genuinely does not want to be the arbiter of truth, what can it rely on to counter misinformation and emotional polarization?** This design's answer is: structure rather than censorship, economic constraints rather than manual takedowns, and decentralized procedural justice rather than centralized authority. This design continues to evolve; this whitepaper documents its core ideas at their current stage.

---

## Version History

- **v1.0** (2026-Aug-02): First public release.
- **v1.1**: Added Section 4, "Real-Person Verification: A Tiered Trust System," clarifying the Sybil-attack defense and the mapping between verification tier and permissions.

---

*This document is a public design record. Discussion and constructive feedback are welcome. Any citation of, or derivative work based on, this design should credit JeffBZhao as the original designer.*
