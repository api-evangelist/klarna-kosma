# Klarna Kosma

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Klarna Kosma is the Open Banking platform that Klarna spun out in March 2022 as a dedicated sub-brand and business unit. Built on the connectivity infrastructure Klarna originally created for SOFORT, Kosma packages PSD2 Account Information Services (AIS) and Payment Initiation Services (PIS) into a single XS2A API that aggregates more than 15,000 banks across 27 European and UK markets with >95% per-market coverage. The same platform powers Klarna's own BNPL underwriting and is sold externally to banks, lenders, fintechs, merchants, SMEs, and freelancers.

This catalog entry profiles Klarna Kosma's public API surface as of May 2026. Kosma does not publish downloadable OpenAPI specifications for its XS2A, Auth, Consent, Insights, KYC, or Payments APIs, so this repository is documentation-only: no `openapi/`, `capabilities/`, `rules/`, `json-schema/`, `json-structure/`, `json-ld/`, `examples/`, or `vocabulary/` artifacts are generated. The `apis.yml` captures the documented APIs, products, environments, and tooling. If Kosma publishes machine-readable specs in the future, they should be added under the canonical artifact subfolders.

## APIs

### Klarna Kosma XS2A API
The XS2A API is the server-side endpoint set used by TPPs and merchants to create and control Open Banking sessions and flows under PSD2. It drives AIS (accounts, balances, transactions) and PIS (account-to-account transfers). Sessions are created against `api.openbanking.klarna.com` (production) or `api.openbanking.playground.klarna.com` (sandbox); the resulting token is handed to the XS2A App for the consumer-facing SCA flow.

### Klarna Kosma Auth API
The client-session companion to the XS2A API, hosted at `authapi.openbanking.klarna.com`. Whenever the flow requires consumer interaction (bank selection, SCA, multi-step forms), the Auth API exposes the session-scoped endpoints used to obtain and submit forms. It is the API surface behind the embeddable XS2A App / JavaScript SDK.

### Klarna Kosma Consent API
The Consent API exposes the PSD2 consent lifecycle so TPPs can list, inspect, refresh, and revoke consents granted by Payment Service Users (PSU). PSD2 requires that Klarna and its clients keep PSU information aligned with active consents — the Consent API is the programmatic surface for meeting that obligation.

### Klarna Kosma Insights API
Kosma Insights turns raw Open Banking transaction data into categorised spend, income, and affordability signals across 200+ categories. It surfaces income streams, recurring outflows, and cash-flow patterns, and is the AIS-derived data product behind Klarna's own BNPL underwriting and the same product sold externally to lenders, fintechs, and merchants.

### Klarna Kosma KYC API
Kosma KYC layers account ownership and identity verification on top of AIS connectivity. It confirms that the authenticating consumer is the legitimate account holder, returns verified attributes, and supports KYC, AML, and onboarding workflows for lenders, fintechs, neobanks, and crypto on-ramps across the EEA and UK.

### Klarna Kosma Payments API
Kosma Payments is the white-labeled PSD2 PIS product. It triggers account-to-account bank transfers directly from a consumer's bank, bypassing card rails. Sessions are created against `/xs2a/v1/sessions` on the XS2A API; the consumer authenticates via the XS2A App; Kosma orchestrates SCA and settlement confirmation with the ASPSP.

## Environments

| Environment | Base URL |
|---|---|
| Production XS2A API | `https://api.openbanking.klarna.com` |
| Production Auth API | `https://authapi.openbanking.klarna.com` |
| Playground XS2A API | `https://api.openbanking.playground.klarna.com` |

A PSD2 test bank supports embedded, decoupled, and redirect SCA methods plus consent management.

## Tags

Open Banking, PSD2, AIS, PIS, Account Information, Payment Initiation, KYC, Identity Verification, Categorization, Insights, Embedded Finance, BNPL, Lending, Fintech, Banking.

## Key Features

- PSD2-licensed AIS and PIS across the EEA and UK via Klarna Bank AB (publ)
- Single XS2A API aggregating 15,000+ banks in 27 countries with >95% per-market coverage
- Embeddable XS2A App / JavaScript widget for consumer bank selection and Strong Customer Authentication
- Auth API for client-session consumer interactions
- Consent API covering the full PSD2 consent lifecycle
- Kosma Insights — transaction categorisation across 200+ categories with income and affordability signals
- Kosma KYC — account ownership and identity verification on top of AIS connectivity
- Kosma Payments — white-labeled PSD2 PIS for merchant checkout and platform payouts
- Sandbox environment with PSD2 test bank covering all three SCA methods
- Underpins Klarna's own BNPL underwriting and SOFORT bank-transfer rails

## Resources

- Portal — [klarna.com/kosma](https://www.klarna.com/kosma/)
- Documentation — [docs.openbanking.klarna.com](https://docs.openbanking.klarna.com/)
- XS2A API URLs and environments — [docs.openbanking.klarna.com/xs2a/urls.html](https://docs.openbanking.klarna.com/xs2a/urls.html)
- XS2A App — [docs.openbanking.klarna.com/xs2a/xs2a-app.html](https://docs.openbanking.klarna.com/xs2a/xs2a-app.html)
- PSD2 test bank — [docs.openbanking.klarna.com/xs2a/test-bank-psd2.html](https://docs.openbanking.klarna.com/xs2a/test-bank-psd2.html)
- AIS Quick Start — [docs.openbanking.klarna.com/xs2a/quick-start-ais-accounts.html](https://docs.openbanking.klarna.com/xs2a/quick-start-ais-accounts.html)
- PIS Quick Start — [docs.openbanking.klarna.com/xs2a/quick-start-pis.html](https://docs.openbanking.klarna.com/xs2a/quick-start-pis.html)
- Klarna GitHub — [github.com/klarna](https://github.com/klarna)
- UK Open Banking listing — [openbanking.org.uk/regulated-providers/klarna-kosma](https://www.openbanking.org.uk/regulated-providers/klarna-kosma/)
- Launch press release (March 2022) — [klarna.com/international/press](https://www.klarna.com/international/press/klarna-launches-klarna-kosma-sub-brand-and-business-unit-to-harness-rapid-growth-of-open-banking-platform/)

## Maintainer

Kin Lane — API Evangelist — [apievangelist.com](https://apievangelist.com)
