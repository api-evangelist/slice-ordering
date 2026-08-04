# Slice (slice-ordering)

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

Slice is a done-for-you online ordering, marketing, payments, and point-of-sale platform for independent pizzerias. It serves more than 19,000 shops across all 50 states and 3,000+ cities. Consumers order through [slicelife.com](https://slicelife.com) and the Slice apps; shop owners run their business through [slice.com](https://slice.com), the Owner's Portal ([owners.slicelife.com](https://owners.slicelife.com)), and the Slice Register POS.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/slice-ordering/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/slice-ordering/refs/heads/main/apis.yml)

## API Access Model

Slice is **not** an open, self-serve API platform. It is a full-service ("done-for-you") SMB platform, so its programmatic surfaces are built for its own apps and for vetted partners rather than for open third-party development.

- Slice publishes a developer portal titled **"Slice Public API"** at [developer.slicelife.com](https://developer.slicelife.com/), built on Stoplight (project slug `slice-public-api`). However, the endpoint reference is rendered client-side behind the portal app, is not openly browsable or downloadable, and there is no self-serve API-key signup.
- A separate merchant/banking API portal exists at [developer.slicebank.com](https://developer.slicebank.com/) for Slice's financial-services surfaces; it is gated (returns 403 to anonymous requests).
- Integration is **partner-gated** and arranged through Slice's partnerships team (`partner@slicelife.com`).
- No public OpenAPI, Postman, or Open Collection definition is available, so none is fabricated here.

The APIs below are therefore **logical, modeled groupings** derived from the platform's known merchant surfaces (for example, the Owner's Portal exposes shop menu items at `owners.slicelife.com/shops/{id}/menu/items`). They are not taken from a published Slice specification.

## Tags

- Online Ordering
- Food Delivery
- Pizzerias
- Restaurants
- Point of Sale
- Payments
- SMB
- Partner API

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs (Modeled)

### Slice Shops API (Modeled)

Logical grouping for the pizzeria (shop) records that anchor the Slice platform - profile, address, hours, service areas, and pickup/delivery availability. No public endpoint reference is documented; access is partner-gated.

- **Human URL:** [https://developer.slicelife.com/](https://developer.slicelife.com/)

### Slice Menu API (Modeled)

Logical grouping for a shop's menu - categories, items, sizes, toppings, and pricing (the Owner's Portal exposes shop menu items at `owners.slicelife.com/shops/{id}/menu/items`). No public endpoint reference is documented; access is partner-gated.

- **Human URL:** [https://developer.slicelife.com/](https://developer.slicelife.com/)

### Slice Orders API (Modeled)

Logical grouping for online orders placed for pickup or delivery - cart, checkout, order status, and fulfillment. Central to Slice's per-order commercial model. No public endpoint reference is documented; access is partner-gated.

- **Human URL:** [https://developer.slicelife.com/](https://developer.slicelife.com/)

### Slice Customers API (Modeled)

Logical grouping for the diner accounts, order history, and marketing/loyalty relationships that Slice manages on behalf of shops (consumer identity is handled via Auth0). No public endpoint reference is documented; access is partner-gated.

- **Human URL:** [https://developer.slicelife.com/](https://developer.slicelife.com/)

## Pricing (Platform, not API)

Slice's pricing is a merchant/platform model, not API pricing. Slice charges partner pizzerias a flat **per-order fee** (widely reported at ~$2.25, waived on orders under $10) instead of the 10-30% percentage commissions charged by large marketplaces. Slice Register (the POS) adds card-processing fees (~2.5%), with optional marketing and listing-management add-ons. Slice does not publish per-call, per-order, or per-location **API** pricing, so no Plans, Rate Limits, or FinOps artifacts are included.

## Common Properties

- [GitHub Organization](https://github.com/slicelife)
- [LinkedIn](https://www.linkedin.com/company/slice)
- [Website (Consumer)](https://slicelife.com)
- [Website (Merchant)](https://slice.com)
- [Developer Portal](https://developer.slicelife.com/)
- [Merchant/Banking Developer Portal](https://developer.slicebank.com/)
- [Sign Up](https://slice.com/get-started/)
- [Pricing](https://slice.com/pricing/)
- [Blog](https://blog.slicelife.com/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
