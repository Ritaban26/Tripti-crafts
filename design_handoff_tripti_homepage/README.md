# Handoff: Tripti Crafts — Homepage (4 directions)

## Overview
Tripti Crafts is an intergenerational, story-forward saree e-commerce brand founded in memory of Tripti Bagchi. This package contains **four homepage design directions** to be rebuilt as **basic, standalone HTML files** (one file per direction), each with a **responsive phone view** driven purely by CSS (no framework required). Each direction leads with the brand story, then flows into a product/shop section.

The goal: a developer produces **4 clean HTML/CSS files** (optionally 1 shared stylesheet) that render the desktop layout on wide screens and reflow to a single-column mobile layout below ~768px. Content is placeholder-ready — real photography and final copy drop in later.

## About the Design Files
The file in this bundle (`Tripti Homepage.dc.html`) is a **design reference created in HTML** — a prototype showing intended look, layout, and hierarchy across four directions on one pannable canvas. It uses a small internal templating runtime (`support.js`) and is **not production code to copy directly**.

The task is to **recreate the four directions as plain, self-contained HTML files** using standard HTML5 + CSS3 (and minimal/no JS). Strip the templating runtime, the canvas wrapper, and the option badges — those are authoring scaffolding, not part of the design. Resolve the two template tokens as fixed values (see Design Tokens):
- `{{ accent }}` → the direction's accent hex.
- `<sc-if value="{{ showOrnaments }}">…</sc-if>` → keep the enclosed ornament markup (always-on).

## Fidelity
**High-fidelity (hifi).** Colors, typography, spacing, and section structure are final-intent. Recreate the layouts faithfully. The only deliberate placeholders are:
- **Imagery**: all images are shown as diagonal/striped gradient blocks with a small caption label describing what goes there (e.g. "tall portrait · draped saree"). Replace with real `<img>` elements at the same aspect ratios.
- **Copy**: story text is representative; treat as final unless the client revises.

## Deliverables
Four HTML files, each desktop + responsive phone view:
1. `editorial.html` — Direction **1a** (Editorial, quiet & literary)
2. `warm-heritage.html` — Direction **1b** (Warm heritage, structured & celebratory) ← client's current favourite
3. `magazine-spread.html` — Direction **4a** (Warm magazine spread, asymmetric)
4. `memory-book.html` — Direction **4b** (Centred memory book, horizontal catalogue)

Each must include a single responsive phone view: the desktop grids collapse to one column, multi-column product grids become 1–2 columns, nav collapses to a hamburger, and font sizes step down. The prototype's device-framed mobile mock (option 2a) shows the *intended* mobile arrangement for the warm-heritage direction — use it as the reference for how all four should reflow.

---

## Global system (applies to all 4 directions)

### Typography
- **Serif display** (headlines, product names): *Cormorant Garamond* (1a, 4a, 4b) and *Marcellus* (1b). Load both from Google Fonts.
- **Sans body / nav**: *Jost* (weights 300/400/500).
- **Mono eyebrows / labels / meta**: *DM Mono* (400/500) — used for the small uppercase, wide-letter-spaced kicker labels and © lines.
- Google Fonts URL (already used by the prototype):
  `https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400;1,500&family=Jost:wght@300;400;500&family=Marcellus&family=DM+Sans:opsz,wght@9..40,400;9..40,500;9..40,700&family=DM+Mono:wght@400;500&display=swap`

### Type treatment conventions
- **Eyebrow/kicker**: DM Mono, 12px, `text-transform:uppercase`, `letter-spacing:.24em`, accent or muted brown color.
- **H2 hero**: serif, 500 weight, 66–92px, `line-height:.98–1.06`. Uses `<br>` line breaks and an *italic* accent word.
- **Body**: Jost, 16–17px, `line-height:1.75–1.85`, color `#514736`/`#5f5340`/`#5a5142`.
- **Pull-quote**: Cormorant Garamond *italic* 400, 46px, `line-height:1.28`.

### Base resets
```css
* { box-sizing: border-box; }
body { margin: 0; -webkit-font-smoothing: antialiased; text-rendering: optimizeLegibility; }
a { color: #6e2b2b; text-decoration: none; }
a:hover { color: #a97d3a; }
img { display: block; max-width: 100%; }
```

### Image placeholders (match in the rebuild until real photos arrive)
Diagonal weave-texture look:
```css
background: repeating-linear-gradient(135deg,#e6dcc7,#e6dcc7 11px,#eee5d3 11px,#eee5d3 22px);
```
Use `aspect-ratio` (3/4 for on-body portraits, 4/5 for product cards, 1/1 for weave circles) so replacing with `<img>` keeps layout stable.

---

## Direction 1a — Editorial (quiet & literary)
**Accent:** `#8a7d66` muted (this direction is near-monochrome; ink `#26221c` on bone `#f4efe6`).

- **Header**: centered-left wordmark "Tripti Crafts" (Cormorant 600, 26px) left; right nav row (Story / Sarees / Journal / Contact · Search · Cart (0)) — DM-mono-style uppercase 12px, `letter-spacing:.16em`, `#4a4234`. 1px bottom border `#ddd3bf`. Padding `26px 64px`.
- **Hero**: 2-col grid `1.05fr .95fr`. Left: eyebrow "An intergenerational saree house", H2 "Carrying her *spirit* forward." (92px), body, text link "Read her story →" with 1px bottom border. Right: full-bleed portrait placeholder (`min-height:640px`) with corner caption chip.
- **Story pull-quote**: centered band, top border, padding `104px 64px`. Eyebrow "Tripti · तृप्ति · satisfaction", italic 46px quote, `max-width:1000px`.
- **Weave detail band**: full-width 360px horizontal-stripe gradient with caption chip.
- **Featured "Recently woven"**: header row (title 44px + "View all sarees →"), 3-col grid `gap:40px`. Cards = 3/4 image + serif name (23px) + muted subtitle (12px) + price 15px.
- **Labour of love**: 2-col `1fr 1fr`, image left, text right (eyebrow, 40px H3, body).
- **Journal**: 2-col `gap:56px`, each = 260px image + serif 28px title + body.
- **Footer**: dark `#26221c`, wordmark + tagline left, two link columns (Shop / House) right. © line in DM Mono.

## Direction 1b — Warm heritage (structured & celebratory) ★ client favourite
**Accent:** `#7a2e2e` (deep maroon). Surface `#faf4e9`, panel `#f3ead6`, gold `#a97d3a`.

- **Announcement bar**: full-width accent bg, `#f6e9d6` text, centered, 12px uppercase `.14em`: "Handwoven in Bengal · Complimentary shipping on orders over ₹5,000".
- **Header**: 3-zone — left nav (New Arrivals / Sarees ▾ / Shop by Weave), centered wordmark *Marcellus* 30px maroon, right (Our Story / Search / Cart (0)). Bottom border `#e6d9bf`.
- **Hero**: 2-col `1fr 1.15fr`. Left panel bg `#f3ead6`, padding `92px 56px`: eyebrow "Since 2023 · In her memory", H2 *Marcellus* 66px "Every saree / remembers / a woman.", body, two buttons — primary (accent bg, `#faf4e9` text, `padding:16px 30px`) + outline (1px `#6e2b2b`). Right: portrait placeholder `min-height:620px` with **gold ornament frame** (inset 1px border `rgba(169,125,58,.6)` + 26px corner brackets top-left/bottom-right in `#a97d3a`).
- **Divider ornament**: centered row — 110px hairline `#d8c39a`, 9px gold diamond (rotated square), 110px hairline. Padding `44px 0`.
- **Story ribbon**: 2-col `.9fr 1.1fr`. Portrait placeholder left (`min-height:460px`, right margin 56px); right: eyebrow "Our story", H3 46px "Tripti means satisfaction.", two body paragraphs, "Read the full story →" link.
- **Shop by weave**: panel bg `#f3ead6`, centered header (eyebrow "Find your drape" + H3 40px). 6-col grid `gap:26px` of **circular** weave swatches (`border-radius:50%`, 1/1) + uppercase label: Tussar, Kalamkari, Kantha, Khadi, Pure Silk, Kota.
- **Founder's favourites**: header row (H3 40px + "View all →"). 4-col grid `gap:30px`. Card = 4/5 image + *Marcellus* 20px name + subtitle + row of price + "Add" button (1px accent border, accent text, `padding:8px 14px`).
- **Hands behind (makers band)**: full-width accent-maroon bg, 2-col `1.1fr 1fr`. Left = darker striped film placeholder `min-height:440px`. Right (`padding:88px 56px`): eyebrow "The makers" gold `#d9b98a`, H3 42px `#fbeedb`, body `#e6cfb4`, outline button "Meet the weavers" (1px `#d9b98a`).
- **Values strip**: 4-col, each cell centered, dividers `#e6d9bf`, gold diamond + uppercase label: 100% Handwoven / Natural Fibres / Ready Blouse Option / Ships Worldwide.
- **Footer**: dark `#332a20`, 4-col `1.4fr 1fr 1fr 1.2fr` — brand+tagline, Shop links, House links, newsletter (input + gold "Join" button). © line.

## Direction 4a — Warm magazine spread (asymmetric)
**Accent:** `#8f3b32` (warm brick). Surface `#f6f0e4`.

- **Header**: 3-zone, left nav (Her Story / Sarees / Weaves), centered Cormorant 600 28px wordmark, right (Search / Bag (0)). Bottom border `#ddd1ba`, padding `28px 60px`.
- **Asymmetric hero**: 2-col `1.05fr .95fr`. Left text (`padding:96px 64px 96px 60px`): eyebrow "Tripti · तृप्ति · satisfaction · Est. 2023" (`letter-spacing:.3em`), H2 Cormorant 82px "In her memory, / a house of / *handwoven* sarees." (accent italic word), body, two buttons (accent solid + 1px `#c9b48f` outline). Right: tall portrait placeholder `min-height:640px` with inset ornament border.
- **Pull-quote band**: full-width **accent bg**, `#f7ecdb` text, centered, `padding:80px 60px`. Eyebrow "Why we do this" gold `#f0cfa2`, italic Cormorant 46px quote, `max-width:960px`.
- **Offset image + weave list**: 2-col `.9fr 1.1fr`, `gap:64px`, `padding:96px 60px`. Left image `min-height:520px`. Right: eyebrow "Shop by weave", H3 46px "Six threads, / one house.", then a **list** of weaves — each row: serif 28px name (left) + "N pieces →" (right), separated by 1px `#d9cdb4` top borders. Rows: Tussar 12, Kalamkari 08, Kantha 15, Pure Silk 18.
- **Catalogue (staggered 3-up)**: header (H3 48px "Founder's favourites" + "View all sarees →"). 3-col grid `gap:40px`, `align-items:start`; **middle card offset down** with `margin-top:52px` for the magazine stagger. Card = 3/4 image + serif 25px name + subtitle + price.
- **Footer**: dark `#2a251d`, brand+tagline left, Shop/House link columns right, © line.

## Direction 4b — Centred memory book (horizontal catalogue)
**Accent:** `#b06a2c` (amber/ochre). Surface `#f2ead9`.

- **Header**: fully **centered** — wordmark Cormorant 600 30px on top, centered nav row below (Her Story / Sarees / Weaves / Journal / Bag (0)). Bottom border `#ddd1ba`, `padding:32px 60px 26px`.
- **Framed portrait opening**: centered, `padding:90px 60px 80px`. Eyebrow "In loving memory · Since 2023", H2 Cormorant 76px "Every saree we weave / carries *her* story." (`max-width:880px`), then a centered **framed portrait** (`max-width:760px`, 460px tall) with inset ornament border `rgba(176,106,44,.4)`, then body `max-width:620px`, then solid accent button "Read her full story".
- **Three chapters**: top border, 3-col, vertical dividers `#ddd1ba`. Each centered cell = big italic Cormorant number (01/02/03, 40px, accent) + serif 26px title + body. Titles: "Her love for the loom" / "The weavers we work with" / "The promise we keep".
- **Horizontal scrolling catalogue rail**: bg `#e9dfc9`, `padding:80px 0 80px 60px`. Header (eyebrow "The catalogue" + H3 48px "Founder's favourites" + "Browse all →"). Then a **horizontal `overflow-x:auto` flex rail**, `gap:28px`, cards `flex:0 0 300px` each = 3/4 image + serif 24px name + subtitle + price. 5 cards (Tusser Shivori, Raw Silk Jori, Tusser Pure Kota, Cotton Khadi, Kantha Silk). On mobile keep the horizontal swipe rail.
- **Footer**: dark `#2a251d`, **centered** — wordmark, tagline `max-width:420px`, centered link row (Story / Sarees / Journal / Contact), © line.

---

## Responsive / phone behavior (all four)
Single breakpoint at **≤768px** (a second polish breakpoint at ≤480px is optional):
- **Layout**: every 2-col hero / story / makers grid → `grid-template-columns:1fr` (stack, text after image or as designed). Section padding drops to ~`48px 22px`.
- **Nav**: collapse the header nav into a hamburger (☰) on the left, wordmark centered, cart/bag on the right — mirror the prototype's mobile mock (option 2a). A simple CSS-toggle or minimal JS drawer is fine.
- **Type scale**: hero H2 → ~40px, section H3 → ~30px, pull-quote → ~28px, body → 14–15px.
- **Product grids**: 4-col → 2-col; 3-col → 2-col (or 1-col at ≤480px). Weave circles 6-col → 3-col.
- **4b catalogue rail**: keep as horizontal swipe (`overflow-x:auto`), cards `flex:0 0 78vw` on phone.
- **Buttons**: full-width stacked with `gap:12px`; hit target ≥44px tall.
- **Announcement bar / values strip (1b)**: values strip 4-col → 2-col.
- The prototype's device mock (402px screen) is the canonical reference for 1b mobile; apply the same reflow logic to 1a/4a/4b.

## Design Tokens
**Accents (one per direction):** 1a `#8a7d66` (muted, near-mono) · 1b `#7a2e2e` · 4a `#8f3b32` · 4b `#b06a2c`.
**Surfaces:** 1a `#f4efe6` · 1b `#faf4e9` (panel `#f3ead6`) · 4a `#f6f0e4` · 4b `#f2ead9` (rail `#e9dfc9`).
**Ink / body text:** `#26221c`, `#2a251d`, `#332a20`; body muted `#514736` / `#5a5142` / `#5f5340`.
**Gold accent (1b ornaments):** `#a97d3a`, hairline `#d8c39a`.
**Dark footer bg:** `#26221c` / `#2a251d` / `#332a20`.
**Borders / hairlines:** `#ddd3bf`, `#ddd1ba`, `#e6d9bf`, `#d9cdb4`.
**Muted labels:** `#8a7d66`, `#8a7350`, `#8a7358`.
**Type sizes:** hero 66–92px · section H3 40–48px · pull-quote 46px · product name 20–25px · body 16–17px · eyebrow/meta 12px.
**Letter-spacing:** eyebrows `.24–.30em`; nav `.14–.16em`.
**Line-height:** hero `.98–1.06` · body `1.75–1.85` · quote `1.28`.
**Section padding (desktop):** ~`88–104px` vertical, `56–64px` horizontal.
**Radius:** mostly square (0). Only the weave swatches (1b/2a) are `border-radius:50%`.
**Shadow (card float in prototype only — not needed on the real page):** `0 30px 80px rgba(40,34,26,.18)`.

## Assets
No image assets are included — all imagery is placeholder gradient blocks with descriptive captions. Client will supply saree photography (on-body portraits, flat-lay/weave detail, a portrait of Tripti Bagchi, and a loom/maker film still). Fonts are all Google Fonts (Cormorant Garamond, Marcellus, Jost, DM Mono). No icon library — the few glyphs used (☰, cart, diamond) can be Unicode or simple SVG.

## Files
- `Tripti Homepage.dc.html` — the source prototype containing all four directions (1a, 1b, 4a, 4b) plus a device-framed mobile mock (2a). Open in a browser to see the intended rendering; use it as the visual source of truth. Ignore `support.js` and the `{{ }}` / `<sc-if>` template syntax — those are authoring-only.
