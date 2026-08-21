# Handoff: Tripti Crafts — Homepage (Direction 1b, "Warm Heritage")

## Overview
Homepage for **Tripti Crafts**, an intergenerational handloom-saree house built in memory of Tripti Bagchi. The page is story-first: the brand's origin narrative leads, the catalogue supports. This is the single approved direction ("1b — warm heritage shopfront") selected out of several explorations.

## About the Design Files
The file in this bundle (`Tripti Homepage.dc.html`) is a **design reference created in HTML** — a high-fidelity prototype showing intended look and behavior, **not production code to copy directly**. The task is to **recreate this design in the target codebase's existing environment** (React, Vue, Next, etc.) using its established components, tokens, and patterns. If no environment exists yet, pick the most appropriate framework and implement there.

Note: the prototype is authored as a "Design Component" — markup uses inline styles and a couple of template constructs (`{{ accent }}` bindings and `<sc-if>` conditionals). Treat these as plain props/conditionals when porting (see State Management). All imagery is placeholder (diagonal-stripe blocks with captions marking what photo goes where).

## Fidelity
**High-fidelity.** Final colors, typography, spacing, and layout. Recreate pixel-closely using the codebase's libraries; substitute real saree photography for the striped placeholders.

## Screens / Views

### Homepage (single scrolling page, desktop-first, full-width)
Page background `#faf4e9` (ivory), body text color `#332a20`, base font **Jost**. Sections top to bottom:

1. **Announcement bar** — full-width, background = accent maroon `#7a2e2e`, text `#f6e9d6`, centered, 12px uppercase, letter-spacing .14em, padding 11px. Copy: "Handwoven in Bengal · Complimentary shipping on orders over ₹5,000".

2. **Header** — flex row, space-between, padding 24px 56px, bottom border `1px solid #e6d9bf`. Left nav links (New Arrivals / Sarees ▾ / Shop by Weave), centered wordmark "Tripti Crafts" in **Marcellus** 30px color `#6e2b2b` letter-spacing .06em, right nav (Our Story / Search / Cart (0)). Nav links: 12px uppercase, letter-spacing .14em, color `#5a4b34`.

3. **Hero** — 2-col grid `1fr 1.15fr`. Left cell: background `#f3ead6` (warm sand), padding 92px 56px, centered vertically. Eyebrow "Since 2023 · In her memory" (DM Mono 12px, accent). H2 "Every saree / remembers / a woman." in Marcellus 66px, line-height 1.06, color `#3a2a20`. Paragraph (max-width 400px, 16px/1.7, `#5f5340`). Two CTAs in a flex gap-16 row: primary (bg accent, text `#faf4e9`, padding 16px 30px) + secondary (1px border `#6e2b2b`, text `#6e2b2b`). Right cell: min-height 620px placeholder image ("hero portrait · draped saree"); when ornaments on, a `1px rgba(169,125,58,.6)` inset frame + two 26px gold corner brackets (`#a97d3a`).

4. **Ornament divider** (ornaments only) — centered: two 110px hairlines `#d8c39a` flanking a 9px rotated-45° diamond. NOTE: this diamond was edited to green `#1F5A2C` (user's direct edit).

5. **Story ribbon** — 2-col grid `.9fr 1.1fr`, padding 40px 56px 90px. Left: min-height 460px placeholder ("portrait of Tripti Bagchi"), right margin 56px. Right: eyebrow "Our story", H3 "Tripti means satisfaction." (Marcellus 46px), two paragraphs (16px/1.8 `#5f5340`), text link "Read the full story →" with 1px bottom border `#6e2b2b`.

6. **Shop by weave** — background `#f3ead6`, padding 82px 56px. Centered eyebrow "Find your drape" + H3 "Shop by weave" (Marcellus 40px). 6-col grid, gap 26px; each item = circular placeholder (aspect-ratio 1, border-radius 50%, striped fill) + uppercase label 14px `#5a4b34`. Weaves: Tussar, Kalamkari, Kantha, Khadi, Pure Silk, Kota.

7. **Founder's favourites** — padding 88px 56px. Header row: eyebrow "Handpicked" + H3 "Founder's favourites" (40px) left, "View all →" link right. 4-col grid, gap 30px. Each card: 4:5 placeholder image, product name (Marcellus 20px), attribute subtitle (12px `#8a7350`), a stock indicator row, and a price/Add row (price 15px `#3a342a`; "Add" = 1px accent border button, accent text, padding 8px 14px).
   - Card 1 "Tusser Shivori" / mirror work / ₹10,500 — has **green+gold "Handloom mark" badge** top-left of image (bg `#123d1a`, text `#d9b98a`, 1px border `#a97d3a`, DM Mono 10px). In stock.
   - Card 2 "Raw Silk Jori" / jori border / ₹12,500 — In stock.
   - Card 3 "Tusser Pure Kota" / airy handloom / ₹12,500 — In stock.
   - Card 4 "Cotton Khadi" / everyday drape / ₹6,700 — **Low stock**.
   - "In stock" = 6px green dot `#1f5a2c` + label `#1f5a2c`. "Low stock" = 6px gold dot `#c98a2c` + label `#a97d3a`. Both 11px uppercase.

8. **The makers ("hands behind")** — 2-col grid `1.1fr 1fr`, background = accent maroon `#7a2e2e`, text `#f4e4cf`. Left: min-height 440px maroon striped placeholder ("film · the hands behind Tripti"). Right: padding 88px 56px; eyebrow "The makers" (`#d9b98a`), H3 "The hands behind every weave." (Marcellus 42px `#fbeedb`), paragraph (`#e6cfb4`), outlined CTA "Meet the weavers" (1px `#d9b98a` border, `#fbeedb` text).

9. **Values strip** — 4-col grid, top border `#e6d9bf`, each cell 40px 24px centered with a right divider except the last. Each: 8px rotated-45° **green** diamond `#1f5a2c` + uppercase 13px label `#5a4b34`. Labels: 100% Handwoven, Natural Fibres, Ready Blouse Option, Ships Worldwide.

10. **Newsletter ("Join the Tripti circle")** — background `#f3ead6`, padding 88px 56px, centered. Ornament divider (gold diamond), eyebrow "Join the Tripti circle" (accent), H3 "Her story, and the newest weaves, / straight to your inbox." (Marcellus 44px), paragraph (max-width 520px). Input + Subscribe row (max-width 520px, gap 12px): input bg `#faf4e9`, 1px border `#d8c39a`; Subscribe button bg accent, text `#faf4e9`. Fine print "We send a note or two a month. Unsubscribe anytime." (12px `#8a7350`).

11. **Footer** — background `#332a20` (dark umber), text `#e6ddcb`, padding 76px 56px 46px. 4-col grid `1.4fr 1fr 1fr 1.2fr`, gap 44px: brand blurb; Shop links; House links; Contact (hello@tripticrafts.com, Kolkata West Bengal, Instagram · Facebook). Column headings DM Mono 11px uppercase `#8a7d66`. Bottom bar: top border `#47402f`, "© 2026 Tripti Crafts · Handwoven in India".

## Interactions & Behavior
- All links/buttons are placeholders (`href="#"`); wire to real routes: Sarees/Shop by Weave → shop grid, product cards → product detail, Our Story/Read the full story/Meet the weavers → about, Cart → cart.
- Hover: global link hover color `#a97d3a` (gold). Add subtle image-zoom / card lift on product cards per codebase conventions.
- Newsletter: capture email, validate, POST to list provider; success/error states per app patterns.
- Cart count in header is dynamic.
- Responsive: desktop-first here. A separate 402px mobile prototype exists (notch header, stacked hero, 3-across weave tiles, 2-up product grid, sticky bottom tab bar) — collapse multi-col grids to 1–2 cols on mobile.

## State Management
- `accent` (string, default `#7a2e2e`) — brand accent color; drives announcement bar, eyebrows, primary CTAs, "Add" buttons, makers band, newsletter button. Kept as a prop for theming; can be a static token in production.
- `showOrnaments` (boolean, default true) — toggles decorative frames, corner brackets, and diamond dividers. Optional in production; if kept, gate the ornament elements on it.
- Cart item count; newsletter form state (idle/submitting/success/error).

## Design Tokens
Colors:
- Ivory (page bg): `#faf4e9`
- Warm sand (section fill): `#f3ead6`
- Deep maroon (accent): `#7a2e2e`
- Wordmark maroon (logo/links/outlines): `#6e2b2b`
- Antique gold (ornaments/hover): `#a97d3a`; on-maroon gold `#d9b98a`
- Dark umber (footer/body): `#332a20`; body copy `#5f5340`; nav `#5a4b34`; captions `#8a7350`
- Hairline rule: `#e6d9bf` / `#d8c39a`
- Heritage green (highlight only — badge, in-stock dot, values diamonds): `#123d1a` (badge bg), `#1f5a2c` (dots/diamonds/labels)
- Low-stock gold: dot `#c98a2c`, label `#a97d3a`
- Image placeholder stripes: `#ecdcc3`/`#f3e6cf`, `#e9d6b8`/`#f1e2c6`, `#e6d3b3`/`#efe0c4`

Typography:
- Display/headings: **Marcellus** (serif), weight 400
- Body/UI: **Jost** (300/400/500)
- Eyebrows/labels/meta: **DM Mono** (400/500), uppercase, letter-spacing .14–.24em
- (Cormorant Garamond is loaded but the finalized design uses Marcellus for headings)
- Scale: H2 hero 66px, H3 section 40–46px, newsletter H3 44px, body 16px, meta 11–13px

Spacing: section padding ≈ 82–92px vertical / 56px horizontal; grid gaps 26–44px. Layout content is full-width (no max-width wrapper on the page).

Border/shape: ornaments 1–2px gold; product images 4:5; weave tiles circular; no border-radius on cards/buttons (square corners throughout).

## Assets
No real images — all placeholders (captioned diagonal-stripe blocks) mark photo slots: hero portrait, portrait of Tripti Bagchi, weave category thumbnails (×6), product images (×4), makers film still. Fonts via Google Fonts (Marcellus, Jost, DM Mono, Cormorant Garamond). No icon set — decorative diamonds are CSS.

## Files
- `design_handoff_tripti_homepage/Tripti Homepage.dc.html` — the finalized 1b homepage (copy of project root `Tripti Homepage 1b.dc.html`).
- `design_handoff_tripti_homepage/support.js` — runtime for the prototype's template constructs; **reference only, not for production**.
- Project also contains `Tripti Palette.dc.html` (color reference) and `Tripti Homepage.dc.html` (multi-direction exploration canvas — not the final).
