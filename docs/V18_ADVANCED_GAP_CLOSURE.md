# LandLedger v18 — advanced research-gap closure notes

This note captures the v18 gap-closure framing available in the project workspace. It is a research/integration record, not proof that the corresponding code or data files have been imported into this repository.

## Evidence model

Keep the following states separate in every API, dataset, UI, and evaluation:

1. **Official aggregate statistic** — government-published state/UT totals; not named people and not owner-to-parcel evidence.
2. **Source-captured owner/parcel evidence** — a record obtained from an identified source or authorised upload, with provenance and capture timestamp; not automatically verified legal title.
3. **Authority-reviewed evidence** — a designated authority has reviewed the supplied material under a recorded workflow; the system still does not independently adjudicate title.
4. **Legally authoritative title/registration** — must remain with the competent government/legal process; do not represent an application approval or blockchain event as statutory transfer.

## Integration controls

- Record source URL/identifier, jurisdiction, capture time, source type, and checksum for imported evidence.
- Preserve missing values as `null`; never infer zero or fill state-specific acquisition metrics from national totals.
- Do not scrape or publish personal owner data without a lawful public source, authorised export, or valid consent and access basis.
- Restrict personal owner information to authorised roles and avoid exposing it in public analytics or exports.
- Treat SHA-256 as a post-capture integrity check, not as proof that a source document was authentic when created.
- Keep synthetic ML evaluation clearly labelled `SYNTHETIC_TEST_ONLY`; block real-government model claims until an authorised, labelled dataset and evaluation protocol are available.
- Keep external RBIH/IPR integrations disabled until credentials, onboarding, and live response verification are completed.
- Keep Hyperledger Fabric privacy and network configuration separate from the local/mock ledger; a syntactically valid script is not evidence of a deployed network.

## Known unresolved dependencies in the v18 report

- No authorised labelled real-government fraud dataset was supplied; real-government ML gate remains blocked.
- No live RBIH credentials/onboarding or IPR API key were supplied.
- Docker/Fabric test-network deployment and Go dependency-backed build were unavailable in the reported environment.
- Full Vite production build and API integration suite were not completed in the reported environment.
- Public data and acquisition extracts do not establish complete nationwide parcel-title coverage or person-by-person owner relationships.

## Source status

The full v18 application source archive was not exportable from the connected project workspace during this GitHub operation. This document preserves the available v18 architecture and evidence controls; it must not be mistaken for the full implementation.
