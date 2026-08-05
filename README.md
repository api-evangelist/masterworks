# Masterworks

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

Masterworks is a New York fintech platform that securitizes blue-chip contemporary art. It buys
paintings by artists such as Picasso, Basquiat, Warhol, Monet and Banksy, places each work in its own
LLC, files it with the SEC as a separate Regulation A offering, and sells fractional shares to retail
investors — who can also trade those shares on a Masterworks-operated secondary market.

## API surface

Masterworks publishes **no developer program** — no developer portal, no API documentation, no
OpenAPI, no SDKs, no CLI, no sandbox, no Postman collection, no MCP server and no A2A agent card.

It does operate a single GraphQL endpoint at `https://api.masterworks.com/graphql`, the private
backend for its own web and mobile clients. That endpoint answers **anonymous schema introspection**,
so the complete machine-readable contract is publicly readable: 516 queries, 621 mutations, 5
subscriptions and 1,584 types, captured verbatim in
[`graphql/masterworks-schema.graphql`](graphql/masterworks-schema.graphql). Every data field is
guarded by an `@authenticate` directive and returns `invalidAuthentication` (status 401) without a
first-party token, so the schema is readable but the data is not.

- Website: https://www.masterworks.com/
- Help Center: https://knowledge.masterworks.com/en/knowledge
- Academy (education/blog): https://www.masterworks.com/academy/posts
- GitHub: https://github.com/MasterworksIO
- Secondary-market listing (how this company entered the harvest backlog): https://forgeglobal.com/masterworks_stock/
