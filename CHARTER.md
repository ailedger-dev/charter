# AILedger Charter — v1.4

## Purpose

AILedger makes AI-influenced decisions in regulated industries provable — so customers, regulators, and courts can see what a system did and verify it. The rule we build to is simple: an audit trail is only worth paying for if it catches what actually went wrong. Paperwork that passes a regulator while the problem continues helps no one, so we don't build it.

## Scope: what AILedger does and does not do

AILedger sits at the audit layer of AI-influenced decisions, not the decision layer or the remediation layer:

- **Detection (yes):** Identify bias, drift, disparate impact, and other failure modes in AI-influenced decisions, with thresholds anchored to published standards (see [STANDARDS.md](./STANDARDS.md)).
- **Reporting (yes):** Produce structured Decision Event records, Integrity Chain verifications, and statistical findings as audit-grade evidence usable by customers, regulators, and adversarial reviewers.
- **Remediation (no, by design):** AILedger does not propose, recommend, or implement remediation for the AI behavior it detects. Remediation is the customer's responsibility, executed by their compliance, legal, and regulatory counsel. This separation is structural: an audit substrate that also remediated would mean customers grading their own work, which is exactly the audit theater this Charter exists to prevent.

AILedger facilitates accountability. It does not absolve it. Where a customer needs formal certification, AILedger supports certification partners with evidence; it does not itself certify.

## Working as intended

Customers detect bias, drift, and disparate impact in their own systems before regulators or plaintiffs do — early, internally, where issues are cheapest to fix. The populations those systems act on are treated more consistently, and customers carry less regulatory and litigation risk. Regulators and adversarial reviewers treat AILedger output — Decision Events, Integrity Chain verifications, Witnessed Inferences — as evidence. That credibility is the product, and it is what customers pay for.

## Failure mode

A product like this fails by becoming theater: audit trails intact and meaningless, thresholds tuned to suppress findings, "we have a compliance tool" standing in for any real change. When that happens the customer ends up more exposed, not less — the appearance of compliance is the first thing a regulator takes apart, and the record AILedger produced becomes the evidence used against them. AILedger is built to avoid this because defensibility is the entire value of the product.

## Use cases we decline

AILedger sells across B2B and B2G. The list below is specific use cases — not sectors or company types:

- Companies whose underlying AI use is itself the harm (predictive policing, social scoring, deceptive targeting of vulnerable populations)
- Companies that request detection configurations specifically designed to suppress findings
- Companies whose primary purpose is paperwork generation rather than catching problems
- Companies under active enforcement action who want AILedger as an improper litigation defense in bad faith to suppress harm that the regulation is meant to prevent rather than showing ongoing accountability under the regulation.

## Features we won't build

- Configurable detection thresholds that allow suppression below standards-aligned defaults*
- "Compliance mode" that generates reports without underlying detection
- Removal of required-action workflows for detected events
- Selective logging that excludes specific decision categories at customer request

*Specific standards anchoring detection defaults are listed in [STANDARDS.md](./STANDARDS.md). The principle of standards-anchoring is the Charter commitment; the specific list is maintained in that document and updates without requiring board approval.

## Decisions requiring board review

- Weakening any detection primitive below its launch sensitivity
- Accepting a customer from a refused category
- Subjective determinations of bad-faith use per Use-cases-we-decline §4 (including but not limited to bad-faith litigation defense)
- Removing or making optional any required-action workflow
- Acquisition offers or exit decisions that would change product direction
- Any amendment to this charter (requires unanimous Board of Directors approval)

## Exit conditions

- Detection primitives demonstrably fail to catch harm in real customer deployments and can't be fixed
- Regulatory environment shifts such that AILedger's substantive features become commercially impossible to sell against competitors offering audit theater
- Founder no longer able to refuse customers without bankruptcy
- Majority of the Board of Directors no longer voting to maintain refusals

## Public commitment

This charter is published from day one. Customers, regulators, and the public can hold AILedger accountable to it. Amendments are versioned publicly so changes are visible. A commitment that can be revised quietly is worth nothing to the people relying on it; that is why the revision history is open.

## Review cadence

At a minimum, reviewed annually by Board of Directors.

## Regulatory context

Updated 2026-05-20, post-Digital Omnibus. The binding obligations on August 2, 2026 are Article 27 FRIA (deployers in credit scoring, insurance pricing, public services, education, and employment), Article 50 transparency, financial-sector high-risk AI, and GPAI provider obligations. Most other Annex III standalone high-risk obligations move to December 2, 2027, and Annex I product-embedded systems to August 2, 2028. This narrows the immediate regulatory surface but does not change AILedger's principle: catch actual harm, not paperwork. The FRIA living-document requirement makes continuous evidence infrastructure more important, not less.

This section is informational. The principles, refused-customer categories, refused-feature categories, and amendment rules above are the binding Charter commitments and are unchanged.

## Change log

- **v1.4 (2026-05-30):** Editorial revision for plainer, more commercial language (KIS), plus two clarifications: (1) a lead line on Customers-we-refuse stating that AILedger sells across B2B and B2G and declines specific use cases, not sectors or company types; (2) a line in Scope noting AILedger supports certification partners with evidence but does not itself certify; (3) renamed the "Customers we refuse" header to "Use cases we decline" (label only). No binding commitment changed — the four refused-customer categories, four refused-feature categories, board-review triggers, exit conditions, STANDARDS-anchoring rule, and amendment procedure are unchanged in force and wording. Minor textual revision per the amendment procedure.
- **v1.3 (2026-05-27):** Added Scope section between Purpose and Working as intended, clarifying that AILedger sits at the audit layer of AI-influenced decisions, not the decision layer or the remediation layer.
- **v1.2 (2026-05-20):** Added Regulatory context section reflecting the May 7, 2026 Digital Omnibus political agreement. Non-substantive update; no principle changes.
- **v1.1 (2026-05-18):** Jake-authored rewrite. Restructured into Purpose / Working as intended / Failure mode / Customers we refuse / Features we won't build / Decisions requiring board review / Exit conditions / Public commitment / Review cadence.
