# Sierra Space

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
