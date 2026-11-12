# Peter Izzard Photography — deep research

Research date: 2026-08-15 (Asia/Shanghai)  
Scope: public, read-only research and browser viewing only. No login, contact, form submission, image download/reuse, Demo, deployment, payment, CAPTCHA bypass, or changes outside this directory.

## Decision

**HOLD — do not advance to Demo.**

This replaces the Round 05 working KEEP with a stricter, falsifiable result. The required real-browser confirmation of two material main-site problems is unavailable. Playwright previously encountered a Cloudflare verification page on the homepage and `403 Forbidden` on Contact, Weddings and Family. The authorised follow-up in the **Codex in-app normal browser** also reached homepage `https://www.peterizzardphotography.com.au/` with final title `403 Forbidden`; its complete visible DOM was only `403 Forbidden` and `openresty/[REDACTED_HOST]`. No CAPTCHA was clicked and no further/repeated browser or Chrome attempt was made. A source-level representation suggests plausible issues, but that is not a substitute for visitor-path verification.

## What is confirmed

| Question | Evidence | Result |
| --- | --- | --- |
| Current operation | Merchant source: the Fine Art contact page rendered in a real browser, identifies “Peter Izzard Photography,” shows the business email/phone and an active Shopify cart/payment surface. Merchant source: the Commercial site rendered and describes current commercial services, phone and contact routes. | Consistent with current operation; these are merchant-controlled sources. |
| Independent/local corroboration | Destination Kiama 2026 visitor guide, already retained in Round 05, independently lists Peter Izzard Photography with Kiama-area business details. | Local listing corroborated; it does not prove legal ownership. |
| Peter's relationship to the business | Fine Art contact page says “Contact Peter Izzard Photography”; main-site public representation names Peter and the business; Commercial site uses the same mobile number. | Public operator/brand association supported. Legal ownership and decision authority are **UNKNOWN**. |
| Public contact route | `[REDACTED_EMAIL]` appears on the rendered Fine Art contact page, along with `0431 776 036`. DNS on 2026-08-15 returned MX `peterizzardphotography-com-au.mail.protection.outlook.com`. | Public business email + domain routing confirmed. Mailbox delivery is not tested. |
| Instagram | Both accessible sites link to `https://www.instagram.com/southcoast_photographic/`. Agent-reach doctor reports Instagram needs an uninstalled Chrome extension; no installation/login attempted. | Official-link association supported; activity in the last 90 days is **UNKNOWN**. |

Sources: [main site](https://www.peterizzardphotography.com.au/), [Fine Art contact](https://peterizzardfineartphotography.com.au/pages/contact), [Commercial site](https://www.southcoastphotographic.com.au/), and [Destination Kiama guide](https://kiama.com.au/wp-content/uploads/2025/12/DK-2026-Visitor-Guide_FINAL-1.pdf). Retrieved/checked 2026-08-15.

## Browser and audit record

### Main-site visitor-path result

| Route requested | Real-browser observation | Qualification use |
| --- | --- | --- |
| Homepage | Cloudflare verification page, title “请稍候…”. Console recorded repeated failed challenge-resource requests. | Capability/environment gap, **not** a customer defect. |
| `/contact/` | `403 Forbidden` / openresty in Playwright. | Cannot verify CTA or form behavior. |
| Weddings | `403 Forbidden` / openresty in Playwright. | Cannot verify visitor experience. |
| Family / Portrait | `403 Forbidden` / openresty in Playwright. | Cannot verify visitor experience. |
| Commercial | `https://www.southcoastphotographic.com.au/` rendered in Playwright: distinct navigation, phone/email routes, service pages and current blog surface. | Confirms a separate, functioning destination. |
| Landscape / Shop | Fine Art Shopify contact page rendered in desktop and at 390×844: mobile `Menu` button, contact details, shop/cart/login and payment methods are present. | Confirms a separate, functioning commerce/fine-art destination. |

### Minimum-unblock follow-up — in-app normal browser

- Tool: Codex In-app Browser, ordinary desktop viewport, 2026-08-15.
- Attempt: one direct, read-only homepage navigation only; no login, form submission, CAPTCHA interaction, proxy/VPN/DNS change, extension installation, or retry.
- Final URL: `https://www.peterizzardphotography.com.au/`.
- Raw visible result: page title `403 Forbidden`; DOM: heading `403 Forbidden`, separator, `openresty/[REDACTED_HOST]`; no console warnings/errors captured.
- Alternative-path decision: **not attempted**. The authorisation permits a Chrome attempt only if the in-app browser is unavailable; it was available but blocked. The instruction then limits this situation to one truthful report rather than repeated/fingerprint-changing attempts.
- Remaining concrete technical gap: an ordinary unblocked browser must view homepage + Contact and operate the `Send an email` control, then capture desktop/mobile rendering of Weddings and Family. Until that evidence exists, no candidate issue counts toward the two-problem gate.

Local evidence: [main Cloudflare screenshot](output/playwright/main-cloudflare.png), [Fine Art desktop](output/playwright/fineart-contact-desktop.png), [Fine Art mobile](output/playwright/fineart-contact-mobile.png), Playwright snapshots/logs under `.playwright-cli/`.

The required `audit-website` surface audit was also run. It crawled zero main-site pages because bot protection blocked it; its scores/issues are excluded from the decision. See [audit output](output/squirrel-main-quick.llm). In particular, neither the audit block, browser 403 responses, nor the Cloudflare challenge may be represented as a defect experienced by ordinary customers.

### Main-site problem candidates — deliberately not counted as confirmed

1. The public page representation exposes several service categories and directs Commercial and Landscape/Shop to different domains. That may dilute a first-time generic enquiry path, but the browser could not assess the rendered navigation or intent cues.
2. The same representation gives `Send an email` a `javascript:void(0)` target. It may open a JavaScript form/modal in a normal visitor browser; its live behavior is **UNKNOWN**, so it is not evidence of a broken email CTA.
3. The rendered text repeats “Based on the NSW South Coast.” This is a minor copy issue, not a material conversion problem.

Therefore there are **zero real-browser-confirmed material main-site problems** in this pass, not the required two.

## Multi-site interpretation and static scope

The evidence supports a reasonable intentional architecture rather than a simple “fragmented website” sales claim:

- the main domain covers wedding/portrait/pet identity and discovery;
- South Coast Photographic is a separately rendered commercial-services destination;
- Fine Art is a live Shopify shop with collections, cart/payment capability, exhibitions and contact.

This division can serve distinct audiences and search intents. Do not pitch consolidation or replacement without owner confirmation.

The only potentially valid AU$800 static use case is a **new, narrow, non-replacement introductory page for one stable service** (for example, a selected wedding or family-enquiry campaign). It may contain approved identity text, a small approved image set, stable process/testimonial text, service area, phone/email/Instagram and outbound links to the existing specialist sites.

It must not contain or promise: product catalogue, cart/checkout, inventory, pricing that changes, booking/availability calendar, enquiry form backend, client galleries/login, blog, SEO migration, store replacement, tracking, ongoing content work, or use of images/testimonials without written rights clearance.

## Brand-investment / ability-to-pay signals

These are signals only, not buying intent or proof of AU$800 affordability.

1. **Merchant-controlled:** Fine Art is a functioning Shopify storefront with cart and recognised payment-method surface visible in the real browser.
2. **Merchant-controlled:** separate branded main, commercial and fine-art destinations, with curated portfolios and distinct service journeys.
3. **Independent:** the current Destination Kiama guide retains the business in its local creative/photography listing.

## AU$800 case and red team

**Support, if later verified:** a highly bounded page could package existing stable proof and route one audience to phone/email without integrations; the candidate already has a local listing and an own-domain business email.

**Against / strongest red team:** the existing three-site estate already assigns different functions to portfolio, commercial work and sales. The two accessible specialist destinations are not obviously abandoned and one supports commerce. A mature photographer may gain nothing from another page; a new page can introduce SEO/cannibalisation and brand-consistency costs. Curating images and obtaining copyright/testimonial permissions can exceed the fixed-scope value. No budget, timing or owner demand has been evidenced.

## Falsifiable go/no-go

**GO only when all are true:**

1. An ordinary-browser or owner-provided capture verifies at least two material problems on the intended main-site visitor path (including a direct test of the `Send an email` control).
2. The owner identifies one stable service/audience that lacks an adequate existing path and explicitly wants an additional page, not a consolidation/replacement.
3. The owner supplies or approves rights-cleared images, text/testimonials and a fixed contact route; no booking, commerce, migration or ongoing-content need enters scope.
4. Outreach consent/lawful basis and a workable unsubscribe process are separately verified before any send.

**NO-GO / DROP if:** the existing destinations already satisfy that service path; the desired work includes shop/booking/content/SEO migration; or rights/content selection cannot fit a fixed one-time page.

**Minimum next action:** obtain no further marketing action. First, perform one owner-approved or ordinary-browser read-only visual check of the main homepage and Contact flow from a non-blocked environment. If it fails to reveal two material defects and a narrow missing path, change this record to DROP.

Status: **研究完成，待 PMO 验收**. Decision remains **HOLD** solely because the above bounded ordinary-browser technical evidence gap is still fillable by one later read-only check.
