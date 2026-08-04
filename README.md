# Sierra Space

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

Sierra Space is a commercial space and defense technology company headquartered in Louisville, Colorado, spun out of Sierra Nevada Corporation as an independent entity in April 2021. It designs and manufactures the Dream Chaser reusable spaceplane and Shooting Star cargo module, the LIFE expandable habitat and the Orbital Reef commercial space station (with Blue Origin), Eclipse-class satellites for national security and on-orbit servicing, VORTEX propulsion and hypersonics, space solar arrays and power systems, environmental control and life support systems, and a broad spaceflight hardware catalog.

- Website: https://www.sierraspace.com/
- About: https://www.sierraspace.com/about/
- Spaceflight hardware catalog: https://www.sierraspace.com/spaceflight-hardware-catalog/
- Payload User's Guide: https://www.sierraspace.com/payload-users-guide/
- Newsroom: https://www.sierraspace.com/newsroom/

## API surface

**None public.** Sierra Space is a hardware and mission-systems manufacturer, not a software
platform. Full contract discovery was run on 2026-07-31 and every probe missed — no developer
portal, no API reference, no OpenAPI/Swagger, no GraphQL, no MCP server, no AsyncAPI, no A2A
agent card, and no first-party SDKs on npm or PyPI. See
[`well-known/sierra-space-well-known.yml`](well-known/sierra-space-well-known.yml) for the full
probe record, including the WordPress soft-404 false positives and the DNS-only, publicly
unreachable `api.sierraspace.com` host.

## Artifacts

| Artifact | Method | Notes |
|---|---|---|
| [`llms/sierra-space-llms.txt`](llms/sierra-space-llms.txt) | searched | Provider-published `llms.txt`, saved verbatim from https://www.sierraspace.com/llms.txt |
| [`well-known/sierra-space-well-known.yml`](well-known/sierra-space-well-known.yml) | probed | `/.well-known/*` all 404; contract-discovery + subdomain record |
| [`security/sierra-space-domain-security.yml`](security/sierra-space-domain-security.yml) | probed | TLS 1.3; no HSTS, no DNSSEC, no CAA; SPF present, DMARC `p=none` |

Sierra Space publishes a real `llms.txt` and an AI-crawler policy in `robots.txt` that blocks
model-training crawlers (GPTBot, ClaudeBot, Google-Extended, CCBot, Applebot-Extended) while
allowing user-triggered retrieval agents — a deliberate agent-access posture, captured in the
well-known artifact.
