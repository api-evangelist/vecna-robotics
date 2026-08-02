# Vecna Robotics

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
