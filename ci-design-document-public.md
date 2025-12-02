# CI_DESIGN_DOCUMENT_PUBLIC_V1.0.md

**Version:** 1.0 (Public Concept Overview)  
**Author:** John Forrester  
**Status:** Documentation Only — No Algorithms or Implementation  
**Last Updated:** December 2025

---

## 0. Public Document Disclaimer

This document provides a **high-level, conceptual overview** of the Corruptibility Index (CI) and CI Score™ frameworks.

It is intentionally limited to:

- narrative descriptions,  
- conceptual architecture, and  
- non-technical explanations of metric families and subsystems.

It does **not** disclose:

- detailed formulas or algorithms,  
- implementation logic,  
- code, pseudocode, or data structures sufficient for replication,  
- any proprietary normalization or scoring methods.

All implementation details, including specific computation, model behavior, and code, are maintained separately in **internal, non-public artifacts**.

This document is **not** a product specification and does **not** describe a working system. It is provided for conceptual understanding, research interest, and public transparency about the *intent* and *philosophy* of the CI framework.

---

# 1. Introduction

## 1.1 Purpose of This Document

This document describes the **conceptual design** of the **Corruptibility Index (CI)** framework and its related CI Score™ concept. Its purpose is to:

- explain the overall **architecture and subsystems**,  
- describe the **metric families** at a high level,  
- outline the **data-source categories** that may inform analysis, and  
- articulate the **ethics and governance principles** behind CI.

It is suitable for:

- inclusion in public or documentation-only Git repositories,  
- informing researchers, journalists, and analysts about the conceptual approach,  
- supporting narrative framing for future scholarly or media engagement,  
- demonstrating the originality and scope of the framework **without** exposing technical implementation.

## 1.2 Scope

This Version 1.0 public design document includes:

- A conceptual overview of the **CI-Core** metric set (11 metrics)  
- A high-level description of the **CI subsystem architecture**  
- Non-technical **metric family summaries** for CI-Background, CI-Watch, CI-Screen, and CI-Monitor  
- A **conceptual** Metric → Data Source mapping (categories only)  
- A narrative explanation of how data is generally transformed into interpretable signals  
- Ethics, security, and misuse-prevention principles  
- A conceptual roadmap for future evolution of the framework

No code, formulas, or detailed scoring logic are included.

## 1.3 Intellectual Property Framing

This public document is intended to:

- record the **conceptual structure** of the Corruptibility Index,  
- outline the **novel combination** of metric families and subsystems,  
- demonstrate the **breadth and originality** of the architecture, and  
- create a public, timestamped reference for the system’s core ideas.

It is **not** intended to be sufficient for replication of the internal scoring engine or any proprietary implementation.

---

# 2. System Overview

## 2.1 High-Level Description

The **Corruptibility Index (CI)** is a conceptual framework for analyzing **corruption-risk patterns** related to public figures, political actors, appointees, and similar entities.

At a high level, CI imagines ingesting diverse, public, legally accessible information such as:

- financial and donation records,  
- political disclosures and voting histories,  
- real-estate and corporate ownership records,  
- legal and regulatory events,  
- media and public-interest signals,  
- network and association structures,

and transforming them into **interpretable risk-related signals** (metrics) that can be reviewed and compared.

The CI Score™ is envisioned as a **high-level indicator** that summarizes multiple conceptual risk dimensions into a single, interpretable signal for institutional or research use. This document does not describe how such a score would be mathematically derived.

## 2.2 Design Principles

The CI framework is guided by the following principles:

1. **Modularity**  
   Each metric family acts as a separate risk lens that can be considered independently.

2. **Explainability**  
   Each metric is intended to have a clear, human-understandable interpretation.

3. **Traceability**  
   Inputs, in principle, should come from documented, public, or verifiable sources.

4. **Subsystem Extensibility**  
   CI is envisioned as a platform with multiple use-case-specific subsystems, not a single monolithic score.

5. **Non-Predictive**  
   CI is about **risk exposure**, not predictions of guilt or future behavior.

6. **Defensibility**  
   Metrics are designed conceptually to avoid subjective or purely opinion-based inputs.

## 2.3 Architecture Summary

At a conceptual level, CI includes:

1. **CI-Core**  
   A family of 11 primary corruption-risk metrics intended to form a flagship conceptual index.

2. **CI Subsystems**  
   Distinct, complementary subsystems built on the same conceptual foundation:
   - **CI-Background** — Static due diligence and integrity framing  
   - **CI-Watch** — Ongoing monitoring and alerting  
   - **CI-Screen** — Lightweight screening for rapid checks  
   - **CI-Monitor** — Long-term pattern and drift analysis  

3. **Data Ingestion Layer (Conceptual)**  
   A notional intake layer for public data sources such as campaign-finance disclosures, property records, corporate registries, and media references.

4. **Transformation Layer (Conceptual)**  
   General processes by which raw public data would be reconciled, standardized, and associated with a subject.

5. **Metric Evaluation Layer (Conceptual)**  
   Conceptual logic that turns *patterns in the data* into **interpretable risk signals** for each metric.

6. **Aggregation & Interpretation Layer (Conceptual)**  
   A future point at which metric-level signals could be summarized into higher-level indicators, such as subsystem profiles and a CI Score™.

7. **Audit & Context Layer**  
   The principle that any future implementation should include clear context, sourcing, and interpretability.

No technical implementation details are provided in this document.

---

# 2A. CI Subsystem Architecture (Conceptual)

The CI framework defines four major conceptual subsystems in addition to CI-Core. These are intended to cover different **use-cases** and **time horizons**, while sharing a common conceptual foundation.

## CI-Core (Flagship Conceptual Index)

- Represents the **11 primary corruption-risk metrics** (see Section 3).  
- Envisions a composite indicator (CI Score™) summarizing these dimensions at a high level.  
- Intended to provide a structured view of **systemic risk patterns**, not a judgment of individuals.

## CI-Background (Static Due-Diligence)

Purpose: Provide a **static, context-rich profile** for a subject, suitable for:

- research,  
- onboarding and vetting,  
- editorial or investigative preparation,  
- institutional background review.

Example conceptual metric families within CI-Background:

- Identity integrity and alias continuity  
- Employment and appointment legitimacy  
- Litigation footprint  
- Financial transparency framing  
- Conflict-of-interest baseline  
- Known risk associations  
- Historical reputation deviation

## CI-Watch (Continuous Monitoring)

Purpose: Provide **ongoing awareness** of emerging risk-related signals.

Conceptually, CI-Watch might surface patterns like:

- sudden wealth or asset changes,  
- new entity formations,  
- shifts in policy alignment,  
- emergent legal exposure,  
- rapid changes in network relationships,  
- spikes in media attention or investigative focus.

CI-Watch is envisioned as an “alerting layer”, operating over time.

## CI-Screen (Lightweight Rapid Filter)

Purpose: Provide **fast, low-friction screening** for:

- hiring and staffing decisions,  
- campaign or volunteer vetting,  
- preliminary board or appointment checks.

CI-Screen emphasizes:

- a small set of key checks,  
- low complexity,  
- a clear, simple outcome (e.g., low/medium/high concern).

## CI-Monitor (Long-Term Pattern Tracking)

Purpose: Provide **long-horizon analytics** on:

- wealth and asset drift,  
- policy consistency over time,  
- convergence of donors and influencers,  
- network centrality and influence movement,  
- sustained legal or reputational “background noise”.

CI-Monitor is conceptually oriented towards **multi-year, systemic trends**, rather than short-term events.

---

# 3. Metric Architecture — CI-Core (11 Conceptual Metrics)

This section lists the **11 conceptual metric families** that constitute CI-Core. These are described in human terms only; no formulas or computation methods are included.

## 3.1 Donor Metrics

Focus: Patterns in donation behavior that may indicate **concentration, clustering, or unusual donor dynamics**.

Examples of conceptual considerations:

- whether financial support appears unusually concentrated among a small group,  
- how donor patterns cluster geographically, professionally, or organizationally,  
- whether donation flows appear atypical versus a reasonable baseline.

---

## 3.2 Wealth Anomaly

Focus: **Misalignment between observed assets and plausible legitimate income**.

Conceptually considers:

- publicly observable property holdings,  
- business affiliations and ownership interests,  
- declared financial disclosures,  
- broad alignment between visible assets and expected income bands.

---

## 3.3 Real Estate Patterning

Focus: **Real estate behaviors** that conceptually align with elevated risk:

- rapid flipping or short-hold properties,  
- clustering of properties across entities,  
- transfers through complex or opaque ownership structures.

---

## 3.4 Lobbyist Entanglement

Focus: Intensity and nature of **interactions with lobbyists or lobbying entities**.

Conceptually considers:

- frequency and density of documented interactions,  
- the extent of ongoing relationships,  
- transparency of disclosed vs. expected contacts.

---

## 3.5 Transactional Appointments

Focus: Appointments or roles that appear to align closely with **donations, favors, or network obligations**.

Conceptual questions may include:

- timing of appointments relative to financial or political support,  
- overlapping relationships across donors, appointees, and decision-makers,  
- structural patterns that suggest transactional rather than merit-based placement.

---

## 3.6 Policy Misalignment Risk

Focus: Divergence between:

- public positions,  
- actual voting or decision behavior, and  
- major sources of financial or political support.

Conceptual patterns may include:

- abrupt changes in policy stance,  
- divergence from long-held ideological baselines,  
- alignment shifts that appear correlated with external influences.

---

## 3.7 Social Ecosystem Alignment Score

Focus: The subject’s **embeddedness in high-risk ecosystems** of relationships and affiliations.

Conceptually considers:

- public associations with known high-risk individuals or entities,  
- recurring mutual endorsements or amplifications,  
- proximity to clusters associated with past corruption exposure.

---

## 3.8 Personal Conduct Anomalies

Focus: Publicly observable **personal behavior patterns** that correlate historically with higher corruption risk.

Examples might include:

- repeated minor ethics violations,  
- patterns of rule-bending or boundary-testing,  
- recurring integrity-related incidents over time.

---

## 3.9 Legal Irregularities

Focus: Legal events that are conceptually associated with elevated corruption risk, such as:

- regulatory enforcement actions,  
- civil suits with integrity implications,  
- patterns of investigation or sanctions.

---

## 3.10 Casino License Heuristic

Focus: A conceptual heuristic related to **gambling exposure, license holdings, and casino-related financial behaviors**, reflecting potential risk vectors tied to these domains.

This is presented as a **specialized, narrow-scope metric family**.

---

## 3.11 Investigative Pressure Index

Focus: The level of **sustained attention and scrutiny** from:

- journalists,  
- watchdog organizations,  
- regulators and investigators,  
- public-interest advocates.

Conceptually considers:

- intensity and persistence of scrutiny,  
- clustering of independent inquiries,  
- acceleration or deceleration of investigative focus.

---

# 4. Subsystem Metric Frameworks (Conceptual)

Beyond CI-Core, each subsystem is associated with **its own conceptual metric families**. These are designed to serve different use-cases while remaining consistent with CI’s overall philosophy.

## 4.1 CI-Background (Static Due-Diligence)

### Purpose

To produce a **static, context-rich background profile**.

### Conceptual Metric Categories

1. **Identity Integrity**  
   - alias continuity,  
   - identity anomalies,  
   - overlaps with shell or opaque entities.

2. **Employment & Appointment Legitimacy**  
   - role stability,  
   - unusual promotions or placements,  
   - patterns of board or committee stacking.

3. **Litigation Footprint**  
   - presence and nature of civil/regulatory cases,  
   - patterns in historic disputes.

4. **Financial Transparency Framing**  
   - clarity of declared vs. observed assets,  
   - opacity of ownership structures.

5. **Conflict-of-Interest Baseline**  
   - family businesses,  
   - advisory roles,  
   - overlapping corporate or organizational interests.

6. **Known Risk Associations**  
   - connections to individuals or entities already associated with significant risk.

7. **Historical Reputation Deviation**  
   - long-term media framing and unresolved controversies.

---

## 4.2 CI-Watch (Continuous Monitoring)

### Purpose

To surface **emerging or changing risk signals** over time.

### Conceptual Metric Categories

1. **Event-Driven Wealth Change Signals**  
   - sudden changes in visible asset patterns.

2. **New Entity Formation Activity**  
   - creation of new organizations, vehicles, or structures.

3. **Lobbying & Influence Activity (Current)**  
   - new or intensified lobbying interactions.

4. **Policy-Shift Divergence**  
   - abrupt changes in policy behavior vs. prior baseline.

5. **New Legal Exposure**  
   - new investigations or regulatory attention.

6. **Network Rewiring**  
   - rapid emergence or dissolution of key relationships.

7. **Media Velocity & Attention Surges**  
   - spikes in coverage or thematic clustering around certain topics.

8. **Donor Cluster Movements**  
   - short-term shifts in donor coalitions.

---

## 4.3 CI-Screen (Lightweight Rapid Filter)

### Purpose

To provide **quick, coarse-grained screening** for lower-stakes or higher-volume decisions.

### Conceptual Metric Categories

1. **Recent Litigation & Regulatory Flags**  
2. **Disclosure and Transparency Anomalies**  
3. **High-Risk Network Links (Basic Pass)**  
4. **Prior Conflict-of-Interest Incidents**  
5. **Career Gap or Role Anomalies**  
6. **Sanctions & Watchlist Hits**

CI-Screen conceptually favors **simple qualitative outcomes** (e.g., low / moderate / elevated concern), rather than detailed scoring.

---

## 4.4 CI-Monitor (Long-Term Pattern Tracking)

### Purpose

To highlight **slow-moving patterns and structural drift**.

### Conceptual Metric Categories

1. **Long-Horizon Wealth Drift**  
2. **Policy Consistency Over Time**  
3. **Donor & Influence Convergence**  
4. **Network Centrality & Power Migration**  
5. **Persistent Legal or Regulatory “Background Noise”**  
6. **Real Estate Accretion Trends**  
7. **Reputation Gravitation (Long-Cycle)**  
8. **Compliance Drift Patterns**

---

# 5. Conceptual Data Source Map

This section describes, at a high level, **what types of public data** are envisioned as inputs to CI. It does not specify particular APIs, endpoints, or technical integrations.

## 5.1 Metric Family → Data Category (Conceptual)

| Metric / Category              | Primary Data Category                          |
|--------------------------------|-----------------------------------------------|
| Donor Metrics                  | Campaign-finance and donation disclosures     |
| Wealth Anomaly                 | Property records, asset disclosures           |
| Real Estate Patterning         | Deeds, transfers, ownership registries        |
| Lobbyist Entanglement          | Lobbying and influence disclosures            |
| Transactional Appointments     | Appointment records, organizational roles     |
| Policy Misalignment Risk       | Voting records, policy positions, public statements |
| Social Ecosystem Alignment     | Public association and network information    |
| Personal Conduct Anomalies     | Public records and ethics disclosures         |
| Legal Irregularities           | Court records, regulatory and enforcement actions |
| Casino License Heuristic       | Gaming and license-related public registries  |
| Investigative Pressure Index   | Public investigations, watchdog/journalistic focus |
| CI-Background Categories       | Corporate, professional, litigation, and disclosure registries |
| CI-Watch Alerts                | Time-based changes in the above categories    |
| CI-Screen Checks               | Summary signals from litigation, sanctions, and disclosure integrity |
| CI-Monitor Patterns            | Long-term historical patterns from the above sources |

Actual technical methods, APIs, and integration details are **deliberately omitted**.

---

# 6. Conceptual Normalization & Aggregation (High-Level Only)

In any future implementation, CI envisions:

- **Bringing heterogeneous inputs onto a common conceptual scale**,  
- Avoiding over-reliance on any single metric,  
- Taking into account **recency, repetition, and context**,  
- Producing **interpretable ranges** or bands of concern, not hard labels.

Specific mathematical transformations, weighting strategies, and aggregation methods are **not described in this public document**.

---

# 7. Conceptual Scoring Flow (Non-Technical)

At a high level, a notional CI-inspired process might look like:

1. **Collect Public Data**  
   From legally accessible public records, disclosures, and media.

2. **Associate Data with a Subject**  
   Resolve identity, connect related records, and provide contextual grouping.

3. **Evaluate Metric Families Conceptually**  
   Consider each metric category as a separate risk lens (e.g., donors, legal exposure, network patterns).

4. **Summarize Signals**  
   For each metric family, derive a conceptual signal indicating low, moderate, or elevated concern.

5. **Combine into Higher-Level Views**  
   Subsystems (Background, Watch, Screen, Monitor) each present their own perspective.  
   CI-Core and CI Score™ conceptually represent a combined, multi-dimensional view.

Details of how this would be implemented, calculated, or operationalized are **intentionally withheld**.

---

# 8. Security, Ethics, and Misuse Prevention (Conceptual Framework)

## 8.1 Security & Data Integrity Principles

Any future implementation of CI-inspired ideas should:

- use only **lawful, public, and ethically sourced data**,  
- maintain clear **source attribution** and documentation,  
- provide appropriate protections for sensitive or borderline contexts,  
- ensure that system usage is **logged and auditable**.

## 8.2 Ethics & Fairness Guidelines

Core ethical principles for the CI framework include:

1. **Transparency of Reasoning**  
   Users should understand conceptually *why* a given signal appears elevated.

2. **Non-Predictive Use**  
   CI should be framed as a **risk-pattern framework**, not as a predictor of crimes or outcomes.

3. **Protection Against Bias**  
   The framework should avoid using protected characteristics or demographic variables as inputs.

4. **Context and Proportionality**  
   Single, isolated events should not be overinterpreted; repeated and corroborated patterns matter more than one-off anomalies.

5. **Respect for Legitimate Due Process**  
   CI-related outputs should not be seen as proof of wrongdoing, but as starting points for responsible analysis or oversight.

## 8.3 Misuse Prevention

CI should **not** be used for:

- harassment or political retaliation,  
- targeting private individuals,  
- disinformation or smear campaigns,  
- bypassing legal or ethical standards of due process.

Any real-world implementation should incorporate safeguards, usage policies, and oversight.

---

# 9. Public-Facing Roadmap (Conceptual)

This roadmap is **conceptual only** and describes how the CI framework might evolve as a documentation and research effort.

## 9.1 Near-Term Documentation Goals

- Continue refining the conceptual descriptions of metrics and subsystems.  
- Publish additional **non-technical whitepapers** and explainers.  
- Add visual diagrams explaining how CI views *patterns* rather than individuals.  
- Provide more public-facing material on **ethics, limitations, and appropriate use**.

## 9.2 Potential Future Directions (Non-Binding)

- Collaboration with researchers and academics on corruption-risk modeling as a **field of study**.  
- Development of educational materials for journalists and public-interest organizations.  
- Creation of synthetic, hypothetical case studies to illustrate how risk patterns might be interpreted in practice (without scoring real individuals).

These directions are speculative and do not describe a committed product roadmap.

---

# 10. Public Use and Interpretation

This design document:

- is **not** a rating of any specific person or entity,  
- does **not** provide scores,  
- does **not** include case studies,  
- does **not** disclose implementation details,  
- is entirely conceptual and illustrative.

Readers should interpret CI as a **framework for thinking** about corruption risk, not as a finished or deployed system.

---

# 11. Closing Notes

The Corruptibility Index (CI) and CI Score™ are intended to:

- stimulate **serious, structured thinking** about institutional risk,  
- provide a conceptual foundation for **future research**,  
- encourage more **data-aware transparency practices**, and  
- highlight the importance of **context, nuance, and ethics** in any risk-related analysis.

All technical details, including code, algorithms, formulas, and operational systems, remain **strictly internal** and are **not** part of this public document.

---

© 2025 The Corruptibility Index™ and CI Score™. All Rights Reserved.  
This document is provided for conceptual, educational, and research discussion purposes only.
