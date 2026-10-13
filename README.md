# PureFX Detailing — spec mockup

**STATUS: LEAD — not signed. FIRST WEBSITE**: they have none, and no domain. Spec mockup only. Not deployed. All photography is stock placeholder. `noindex, nofollow` on every page.

Built 2026-10-12 from `PROMPT.md`. Plain static HTML/CSS/JS, no build step. Open `index.html`.

## The pitch, built in

- **The 4.9 from 257 reviews is the pitch, not a page figure.** The review surface is built, filterable and empty on purpose. Every card says why. The rating appears only inside that mandated flag text.
- **The service matrix is the centrepiece.** 13 services × 3 tiers, with every cell `[INCLUDED? — CONFIRM]`, every price a flag, and sedan / SUV / truck as a second axis.
- **Service Areas is a top-level nav item**, and the coverage map doubles as navigation for the location pages.

## Pages (27)

| File | What it is |
|---|---|
| `index.html` | Includes:<br>• hero (type on paper, photo in a frame beside it)<br>• proposition<br>• 3 steps<br>• 13 numbered service rows<br>• **the matrix** and the size axis<br>• tint<br>• paint correction<br>• before/after<br>• coverage map and 20 chips<br>• reviews (empty)<br>• payments ("No checks.")<br>• about<br>• the dark quote form |
| 13 service pages | `auto-detailing` · `full-body-wash` · `car-waxing` · `clay-bar-treatment` · `wheel-washing` · `interior-vacuuming` · `seat-shampooing` · `steam-cleaning` · `interior-scenting` · `engine-detailing` · `headlight-polishing` · `paint-correction` · `window-tinting`. Steam, scenting and tint are short by design |
| `mobile-detailing-marietta` · `-alpharetta` · `-kennesaw` | **Three worked example location pages.** Area prose is a visible client-supply flag. FAQs and nearby links differ per area (by geography) |
| `mobile-detailing-atlanta-metro.html` | The hub, kept distinct from a future Atlanta city page |
| `service-areas.html` | Coverage map plus all twenty URLs. Dallas and Canton carry `-ga` |
| `packages` · `services` · `reviews` · `about` · `contact` · `faq` · `privacy` · `terms` | Legal pages are DRAFT-bannered |

## Design: THE SERVICE MATRIX

- **Palette:** paper `#FBFBF9` and ink `#101214`, with hairlines `#E2E2DD` / `#C9C9C2` and graphite `#6E7278`.
- **Accent (v2, Alex's call on 2026-10-13, overriding the brief's "no accent hue"):** electric violet `#5B34F0` (6.1:1 on paper), with a 7% wash. It is used on CTAs, active nav, eyebrows, the second half of the H1, the recommended matrix column and tier card, chips and focus. It collides with no other detailing lead.
- **One dark surface:** the quote form, which replaces the Instagram DM thread.
- **Type:** Funnel Display (display, never set over an image), Host Grotesk (body), Geist Mono (labels and figures, tabular, load-bearing in the matrix).
- **Photos:** each sits inside a 1px frame. None is full-bleed and none sits behind type. The hero is a whole white car, front three-quarter (Pexels 10029878). It replaced the door-handle close-up in v2. Its fender emblem, wheel-cap mark and tyre lettering are removed, and it has no LUT or heavy grade.
- **Not used:** gradient bands, gloss, specular highlights, reflections, wet edges or Glaze's occlusion device.
- **Motion:**
  - Hairlines rule in from left to right.
  - Matrix rows rise with a 60ms stagger.
  - The tick-draw behaviour is built but never fires, because there are no confirmed ticks.
  - There are no count-ups.
  - All of it is off under reduced motion.
- **Mobile:** the matrix becomes three stacked tier cards. There is no horizontal scroll.

## Required checks (run on all built HTML, CSS and JS)

- **Prices:** no `$` figure anywhere, and no `priceRange`.
- **The matrix:** no tick in any cell, and no dash standing in for "no".
- **Window tint:** no VLT percentage and no limo / blackout / darkest wording. No tint photo is used; the slot is a client-supply frame.
- **Coating:** no durability figure. Ceramic coating appears only inside `[CONFIRM WHETHER CERAMIC COATING IS AN OFFERED SERVICE]`.
- **Steam and scent:** no health or biocidal verb anywhere, including alt text, meta, comments and JSON-LD.
- **Engine and headlights:** no performance, resale, safety or visibility claim.
- **People and reviews:** no staff name (Devin, Cooper, Josiah, Ray), no review text, no stars, no `aggregateRating`.
- **Marques and environment:** no marque, no environmental claim.
- **Hours:** no 24/7 claim and no `openingHours`.

## Calls made (for Alex)

- **Before/after:** the slider's "before" side is a labelled client-supply panel, not a second stock photo. Two different stock photos placed as a before/after imply a result.
- **ct-pressure-washing-475:** checked as the brief asked. It is a conventional banded light site, not table-led, with no `<table>` anywhere. No collision.
- **Water and power:** not stated by PureFX, so it is asked in the form and flagged. It is never claimed either way.

## ⚠️ Pre-launch blockers (PROMPT.md, these block launch)

- **L1 domain:** check today.
- **L2 tint certification and Georgia VLT in writing**
- L3 prices and a filled-in matrix
- L4 ceramic coating: offered or not
- L5 water, power and stormwater
- L6 licensing and insurance
- L7 paint correction wording
- **L8 review display terms and per-customer permission**
- L9 booking availability
- L10 where the form goes (it replaces DMs)
- L11 email and SMS
- L12 durations
- L13 radius and travel fee
- L14 team names and permission
- **L15 the twenty location pages are a content job**
- L16 real photography
- L17 logo
- L18 tie the Google Business Profile to the site
- L19 and L20 Terms and Privacy, including tint re-dos

No DNS exists yet. When it does: web records only, **never MX**.
