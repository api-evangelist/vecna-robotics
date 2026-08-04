# Vecna Robotics

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

Vecna Robotics is a Waltham, Massachusetts material-handling automation company, spun out of Vecna Technologies in 2018, that builds autonomous mobile robots (AMRs) — autonomous forklifts, pallet trucks, tuggers, conveyor and lifter platforms — together with **Pivotal**, its end-to-end orchestration software suite for warehouse and manufacturing operations.

- Website — https://www.vecnarobotics.com/
- About — https://www.vecnarobotics.com/company/about-us/
- Pivotal Software Suite — https://www.vecnarobotics.com/the-vecna-system/pivotal-software-suite/
- Partners — https://www.vecnarobotics.com/partners/
- GitHub — https://github.com/vecnarobotics
- Secondary market — https://forgeglobal.com/vecna-robotics_stock/

## API posture

Vecna markets "flexible API integrations" into existing WMS / MES / ERP environments, but as of the
2026-08-02 enrichment pass it publishes **no developer portal, no API reference, and no
machine-readable API contract**. Contract discovery probed the marketing host, the apex domain, six
candidate developer subdomains (none resolve), and the partner-portal host for OpenAPI, Swagger,
GraphQL, MCP `tools/list`, and A2A agent cards — all missed.

Two genuine machine-readable surfaces were found and captured:

| Artifact | What it is |
|---|---|
| `llms/vecna-robotics-llms.txt` | A real, provider-published `/llms.txt` (v1.0, updated 2026-01-14) declaring AI indexing / training / RAG / summarization as allowed and citation encouraged. Saved verbatim. |
| `well-known/vecna-robotics-openid-configuration.json` | The live OpenID Connect discovery document served anonymously by the Vecna Robotics Salesforce Experience Cloud **partner portal** (`vecnarobotics.my.site.com`). Feeds `authentication/`, `scopes/` (36 scopes), and `conformance/`. |

No A2A agent card exists on any host, so no `a2a/` artifact was written — that artifact is
search-only and is never authored on a provider's behalf.
