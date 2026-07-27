# FortisBC (fortisbc)

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
