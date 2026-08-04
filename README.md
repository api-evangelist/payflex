# Payflex

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

Payflex is a South African Buy Now Pay Later (BNPL) platform that enables
merchants to offer interest-free installment payment options at checkout.
Consumers can split purchases into up to four payments over six weeks, with the
first 25% paid upfront. Payflex settles the full order amount to merchants
upfront (less commission) and assumes all credit and fraud risk.

## API

The Payflex Merchant API is a REST API secured with OAuth2 Client Credentials.
It supports both hosted (redirect) and embedded (iFrame) checkout flows and
covers the full order lifecycle.

**Production base URL:** `https://api.payflex.co.za`  
**Sandbox base URL:** `https://api.uat.payflex.co.za`  
**Authentication:** `POST https://auth.payflex.co.za/auth/merchant`

### Key Endpoints

| Method | Path | Description |
|--------|------|-------------|
| POST | `/order/productSelect` | Create an order and initiate checkout |
| GET | `/order/{orderId}` | Retrieve order status and details |
| POST | `/order/{orderId}/refund` | Issue a full or partial refund |
| GET | `/configuration` | Retrieve merchant payment limits |

### Authentication

Payflex uses the OAuth2 Client Credentials flow. Submit `client_id`,
`client_secret`, `audience`, and `grant_type=client_credentials` to the
auth endpoint to receive a bearer token. Credentials are issued by the Payflex
merchant team during onboarding.

## Platform Integrations

Payflex provides official plugins and modules for:

- [WooCommerce](https://github.com/PayFlexSA/payflex-woocommerce-plugin)
- [Magento 2.4](https://github.com/PayFlexSA/payflex-magento-2-4-module)
- [OpenCart 3](https://github.com/PayFlexSA/payflex-opencart-3-extension)
- [OpenCart 4](https://github.com/PayFlexSA/payflex-opencart-4-extension)
- [PrestaShop 8](https://github.com/PayFlexSA/payflex-prestashop-8-module)

## Links

- Website: https://payflex.co.za/
- Developer Docs: https://docs.payflex.co.za/
- Merchant Portal: https://merchant.payflex.co.za/login
- Merchant Hub: https://payflex.co.za/merchant/
- Support: https://payflex.co.za/support/
- GitHub: https://github.com/PayFlexSA

## APIs.json

This repository is an [APIs.json 0.19](https://apisjson.org/) profile for
Payflex, maintained by [API Evangelist](https://apievangelist.com).
