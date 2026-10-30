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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Klarna Kosma is the Open Banking platform spun out of Klarna in March 2022 as a dedicated sub-brand and business unit. Built on the connectivity infrastructure Klarna originally created for SOFORT, Kosma offers a single PSD2 XS2A API that aggregates more than 15,000 banks across 27 European and UK markets with >95% per-market coverage. The platform exposes Account Information Services (AIS) and Payment Initiation Services (PIS) plus higher-level products — Kosma Insights (categorised transaction, income, and affordability data across 200+ categories), Kosma KYC (account ownership and identity verification), and Kosma Payments (white-labeled account-to-account bank transfers). Kosma serves banks, lenders, fintechs, merchants, SMEs, and freelancers, and also powers Klarna's own BNPL underwriting and SOFORT bank-transfer rails. The XS2A API is paired with an embeddable XS2A App / JS widget that handles consumer bank selection and Strong Customer Authentication (SCA), and a Consent API that exposes the full PSD2 consent lifecycle.

**Areas:** Open Banking · PSD2 · AIS · PI · Account Information · Payment Initiation · KYC · Identity Verification · Categorization · Insights · Embedded Finance · Buy Now Pay Later

## Klarna Kosma on APIs.io

Everything profiled for Klarna Kosma is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/klarna-kosma/](https://apis.io/providers/klarna-kosma/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Klarna Kosma XS2A API](https://apis.io/apis/klarna-kosma/klarna-kosma-xs2a-api/) — The XS2A API is the server-side endpoint set used by TPPs and merchants to create and control Open Banking sessions and flows under PSD2. The XS2A API…
- [Klarna Kosma Auth API](https://apis.io/apis/klarna-kosma/klarna-kosma-auth-api/) — The Auth API is the client-session companion to the XS2A API. Whenever the Open Banking flow requires consumer interaction (bank selection, strong customer…
- [Klarna Kosma Consent API](https://apis.io/apis/klarna-kosma/klarna-kosma-consent-api/) — The Consent API exposes the PSD2 consent lifecycle so TPPs can list, inspect, refresh, and revoke the consents granted by Payment Service Users (PSU). PSD2…
- [Klarna Kosma Insights API](https://apis.io/apis/klarna-kosma/klarna-kosma-insights-api/) — Kosma Insights turns raw Open Banking transaction data into categorised spend, income, and affordability signals. Insights covers 200+ spend categories and…
- [Klarna Kosma KYC API](https://apis.io/apis/klarna-kosma/klarna-kosma-kyc-api/) — Kosma KYC layers account ownership and identity verification on top of the Kosma AIS connectivity. It confirms that the consumer authenticating against…
- [Klarna Kosma Payments API](https://apis.io/apis/klarna-kosma/klarna-kosma-payments-api/) — Kosma Payments is the white-labeled PSD2 Payment Initiation Service (PIS) product. It lets merchants and platforms trigger account-to-account bank transfers…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Klarna Kosma Domain Security](https://apis.io/security/klarna-kosma/klarna-kosma-domain-security/)
- [Klarna Kosma Vulnerability Disclosure](https://apis.io/security/klarna-kosma/klarna-kosma-vulnerability-disclosure/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.klarna.com/)
- [Documentation](https://docs.openbanking.klarna.com/)
- [Getting started](https://docs.openbanking.klarna.com/index.html)
- [Support](https://www.klarna.com/kosma/)
- [Terms of service](https://www.klarna.com/legal/)
- [Privacy policy](https://www.klarna.com/international/privacy-notice/)
- [GitHub](https://github.com/klarna)

## API Evangelist rating

**Kin Score 24.6** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 71.4 |
| Contract quality | 6.5 |
| Contract governance | 0.0 |
| Operational transparency | 5.3 |
| Developer ergonomics | 54.8 |
| Access clarity | 21.1 |

**Agent readiness 3.8** — human-only

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | documented (partial credit) |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 20.5** — Banking & Open Finance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/klarna-kosma/](https://apis.io/providers/klarna-kosma/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Klarna Kosma: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/klarna-kosma/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
