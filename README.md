# FortisBC (fortisbc)

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

FortisBC is a British Columbia energy utility and a subsidiary of Fortis Inc., delivering natural gas to more than 1,054,000 customers and electricity directly to close to 185,000 customers across the province's Southern Interior, plus liquefied natural gas from the Tilbury and Mt. Hayes facilities, renewable natural gas, and EV charging. It sits at the regulated distribution tier of the value chain — the wires-and-pipes monopoly that meters the customer — under British Columbia Utilities Commission oversight, in a province with no wholesale electricity market and no consumer energy data right. Its API posture is honestly none: no developer portal, no published API, no OpenAPI, and no Green Button.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/fortisbc/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fortisbc/refs/heads/main/apis.yml)

## Tags

- Energy
- Canada
- Utilities
- Electricity
- Natural Gas
- Gas Distribution
- Smart Metering
- Renewables
- EV Charging
- LNG

## Timestamps

- **Created:** 2026-07-27
- **Modified:** 2026-07-27

## APIs

None. FortisBC publishes no public API.

Probed anonymously on 2026-07-27: the `developer.`, `developers.`, `api.`, `docs.`, `data.`, `gis.`, `maps.`, `opendata.`, `services.`, `my.` and `portal.` subdomains do not resolve, and `/developers`, `/api`, `/docs`, `/data`, `/openapi.json`, `/swagger.json`, `/api-docs`, `/.well-known/openid-configuration`, `/.well-known/security.txt`, `/llms.txt` and `/about-us/open-data` all return HTTP 404 on `www.fortisbc.com`. A `github.com/FortisBC` organization exists but has 0 public repositories.

## Mandate

- **Regime:** none
- **Status:** none
- **Data standard:** no standard reference found

No consumer energy data mandate applies. Ontario's Green Button obligation (O. Reg. 633/21, November 2021, with Green Button Alliance certification required by November 2023) binds only Ontario local distribution companies; Nova Scotia's Bill 145 binds only Nova Scotia Power; Australia's Consumer Data Right is an Australian statute. British Columbia has enacted no equivalent, and the Green Button Alliance states it has "heard only minor discussions of Green Button in British Columbia to-date."

This is not a mandate that went unimplemented. It is the control case — no mandate, and correspondingly nothing built.

## Data access

- **Consumer data API:** no. Account holders reach their own usage through the SiteMinder-protected customer login at [accounts.fortisbc.com](https://accounts.fortisbc.com) and export billing information as a text file or spreadsheet. No third-party API, no Green Button Download My Data, no Connect My Data.
- **Market data open:** no. Rates, BCUC filings and Kootenay Lake levels are published as web pages and PDFs. British Columbia has no wholesale market operator publishing feeds. The outage map at [outages.fortisbc.com](https://outages.fortisbc.com/outages) is a Bing Maps web app with no documented data endpoint.
- **The one automated flow:** FortisBC pushes commercial natural gas consumption data into the US EPA's ENERGY STAR Portfolio Manager (adapted for Canada by Natural Resources Canada) on customer request. The customer connects to "FortisBC natural gas" in Portfolio Manager, accepts FortisBC's terms, waits up to 24 hours for acceptance, then validates each meter with a FortisBC account number, last bill date and amount at "full access" sharing. Three years of history plus ongoing consumption is released. The API in that exchange belongs to the EPA, not to FortisBC.

## Access gate

**customer-account-required.** There is no signup, no key request, no application form and no partner program. A developer must be a FortisBC account holder, and for the automated gas flow must additionally hold an ENERGY STAR Portfolio Manager account and complete that platform's consent and meter-validation steps.

## Auth model

CA/Broadcom SiteMinder web agent with SAML 2.0 SSO (`ciam.fortisbc.com` → `ciamidp.fortisbc.com`), human interactive login only. No OpenID Connect discovery document is served — `www.fortisbc.com/.well-known/openid-configuration` returns 404, and the 200 on the `accounts.` host is a WAF block page, not a discovery document. No OAuth, no API keys, no third-party authorization surface.

## Home market

Canada — British Columbia. Regulated by the British Columbia Utilities Commission (BCUC). Parent: Fortis Inc.

## Properties

- [Website](https://www.fortisbc.com/)
- [LinkedIn](https://www.linkedin.com/company/fortisbc)
- [Blog](https://www.fortisbc.com/about-us/news-events/stories)
- [Login](https://accounts.fortisbc.com)
- [Documentation — My energy use](https://www.fortisbc.com/accounts/open-close-or-move-your-account/my-energy-use)
- [Documentation — Manage your online account](https://www.fortisbc.com/accounts/open-close-or-move-your-account/manage-your-online-account)
- [Documentation — Energy-efficiency tools for natural gas business customers](https://www.fortisbc.com/services/commercial-industrial-services/energy-efficiency-tools-for-natural-gas-business-customers)
- [Terms of Service — Portfolio Manager](https://www.fortisbc.com/services/commercial-industrial-services/energy-efficiency-tools-for-natural-gas-business-customers/portfolio-manager-terms-and-conditions)
- [Privacy](https://www.fortisbc.com/privacy)
- [Status Page — Outages](https://outages.fortisbc.com/outages)

## Maintainers

- Kin Lane — kin@apievangelist.com
