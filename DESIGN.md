<!-- impeccable:design-schema 1 -->

---
colors:
  navy-deep: "#080F1E"
  navy: "#0B1628"
  navy-mid: "#0F1D35"
  navy-light: "#14253F"
  red: "#C41E2A"
  red-dark: "#9B1720"
  red-bright: "#E8242F"
  white: "#FFFFFF"
  white-90: "rgba(255,255,255,0.9)"
  white-70: "rgba(255,255,255,0.7)"
  white-50: "rgba(255,255,255,0.5)"
  white-30: "rgba(255,255,255,0.3)"
  white-15: "rgba(255,255,255,0.15)"
  white-08: "rgba(255,255,255,0.08)"
  white-04: "rgba(255,255,255,0.04)"
  flag-blue: "#1A3A6E"
typography:
  display: "Bebas Neue, sans-serif"
  body: "Barlow, sans-serif"
  condensed: "Barlow Condensed, sans-serif"
  secondary-display: "Instrument Serif, serif"
  secondary-body: "Outfit, sans-serif"
rounded: false
spacing:
  container-max: "1280px"
  container-padding: "40px"
  section-padding: "80px"
  card-padding: "32px"
  gap-grid: "24px"
  gap-small: "16px"
components:
  - nav
  - hero
  - stats-bar
  - service-card
  - service-featured-card
  - portfolio-card
  - portfolio-feature
  - talent-pillar
  - talent-showcase-item
  - contact-form
  - btn-primary
  - btn-outline
  - section-label
  - footer
---

## Overview

M3 Media is a dark, broadcast-industry corporate site. The design language is angular and masculine -- deep navy backgrounds, red accent color drawn from an American flag motif, skewed geometric stripes, and all-caps display typography. No border-radius anywhere; shapes use `clip-path` parallelograms instead. The site is single-theme (dark only) with no light mode. A secondary podcast landing page uses Instrument Serif + Outfit for a slightly editorial feel but shares the same navy/red palette.

## Colors

| Token | Hex / Value | Usage |
|---|---|---|
| `--navy-deep` | `#080F1E` | Page background, deepest layer |
| `--navy` | `#0B1628` | Section backgrounds (about, portfolio, contact) |
| `--navy-mid` | `#0F1D35` | Card body gradients, mid-layer fills |
| `--navy-light` | `#14253F` | Lighter card accents, showcase backgrounds |
| `--red` | `#C41E2A` | Primary accent -- CTAs, labels, dividers, icon strokes, hover borders |
| `--red-dark` | `#9B1720` | Hero stripe gradient end |
| `--red-bright` | `#E8242F` | Hover state for primary buttons |
| `--white` | `#FFFFFF` | Headings, stat numbers, card titles |
| `--white-90` | `rgba(255,255,255,0.9)` | Body text default, hero tagline |
| `--white-70` | `rgba(255,255,255,0.7)` | Section descriptions, nav links, contact text |
| `--white-50` | `rgba(255,255,255,0.5)` | Card body copy, stat labels, form labels |
| `--white-30` | `rgba(255,255,255,0.3)` | Footer links, outline button borders, scroll indicator |
| `--white-08` | `rgba(255,255,255,0.08)` | Card borders, section dividers, stat separators |
| `--white-04` | `rgba(255,255,255,0.04)` | Card/icon background fills |
| `#1A3A6E` | Flag blue | Used only in the flag icon element (nav + hero) |

Background gradients use `radial-gradient` with `rgba(20, 40, 80, 0.3)` to add subtle blue tints to navy sections.

## Typography

| Role | Family | Weight | Size | Tracking | Transform |
|---|---|---|---|---|---|
| Hero title | Bebas Neue | 400 | `clamp(72px, 10vw, 140px)` | 4px | uppercase (inherent) |
| Section title | Bebas Neue | 400 | `clamp(40px, 5vw, 68px)` | 2px | uppercase (inherent) |
| Card heading | Bebas Neue | 400 | 24-28px | 1-2px | uppercase (inherent) |
| Section label | Barlow Condensed | 600 | 14px | 5px | uppercase |
| Nav links | Barlow Condensed | 600 | 14px | 3px | uppercase |
| Stat number | Bebas Neue | 400 | 52px | 2px | -- |
| Stat label | Barlow Condensed | -- | 13px | 4px | uppercase |
| Body / description | Barlow | 300 | 18px | -- | -- |
| Card body | Barlow | 300 | 15px | -- | -- |
| Form label | Barlow Condensed | 600 | 12px | 3px | uppercase |
| Button text | Barlow Condensed | 700 | 13-14px | 3px | uppercase |

Line heights: display 0.9-1.0, body 1.7, card body 1.5-1.7. Font smoothing: `-webkit-font-smoothing: antialiased`.

**Podcast page** uses Instrument Serif (display) and Outfit 300-700 (body) with the same sizing scale.

## Layout

- **Container:** `max-width: 1280px`, `padding: 0 40px` (24px at 768px, 16px at 480px).
- **Section padding:** 80px vertical (56px at 768px, 40px at 480px).
- **Grid system:** CSS Grid throughout. Primary grids are 3-column at desktop, 2-column at 1024px, 1-column at 768px.
- **Card gap:** 24px universally.
- **Two-column sections** (talent, contact): `1fr 1fr` with 80px gap, collapsing to single column at 1024px.
- **Portfolio feature row:** `1.4fr 1fr` grid, single column on mobile.
- **Nav:** fixed, 72px height, flex between logo and links.
- **Stats bar:** 4-column grid, 2-column on mobile.
- **Breakpoints:** 1024px (tablet), 768px (mobile), 480px (small mobile).
- **`overflow-x: hidden`** on body.

## Elevation & Depth

No box-shadow in default state. Elevation is achieved through:

- **Border:** `1px solid var(--white-08)` on all cards and panels.
- **Hover shadow:** `0 20px 60px rgba(196, 30, 42, 0.1)` (red-tinted) on service cards; `0 20px 50px rgba(0,0,0,0.4)` on portfolio cards.
- **Hover lift:** `translateY(-6px)` on cards, `translateY(-2px)` on buttons.
- **Scrolled nav:** `box-shadow: 0 2px 40px rgba(0,0,0,0.4)` with `backdrop-filter: blur(12px)`.
- **Layering via gradients:** cards use `linear-gradient(165deg, var(--navy) 0%, var(--navy-mid) 100%)` backgrounds. Image overlays use `linear-gradient(to top, var(--navy-deep), transparent)` fades.
- **Decorative stripes:** skewed `var(--red)` rectangles at 3-5% opacity create depth behind sections.

## Shapes

All shapes are angular. **Zero border-radius** across the entire design (except the talent avatar circle at `border-radius: 50%` and mobile button fallback at `border-radius: 4px`).

- **Parallelogram clip-path:** `polygon(8px 0%, 100% 0%, calc(100% - 8px) 100%, 0% 100%)` on buttons (10px offset) and icon containers (6-8px offset).
- **Skew angle:** `--skew: -12deg` used on all decorative stripe elements via `transform: skewX(var(--skew))`.
- **Decorative red stripe (hero):** 30% width, `opacity: 0.6`, gradient from `--red` to `--red-dark`.
- **Section accent stripes:** background elements at 3-4% opacity with the global skew.
- **Dividers:** solid red lines (hero: 80x4px, section-label: 30x2px before pseudo-element).
- **Card top-accent on hover:** `3px` red gradient line (`linear-gradient(to right, var(--red), transparent)`) via `::before`.
- **Stat separator:** `1px` vertical line at `var(--white-08)`.

## Components

### `btn-primary`
Red background (`--red`), white text, Barlow Condensed 700, 14px, 3px tracking, uppercase. Padding `16px 40px`. Parallelogram clip-path. Hover: `--red-bright` background, `translateY(-2px)`.

### `btn-outline`
Transparent background, `2px solid var(--white-30)` border, `--white-90` text. Same typography and clip-path as primary. Hover: border `--white-70`, text `--white`.

### `nav-cta`
Compact primary button variant: `10px 28px` padding, 13px font. Same clip-path (8px offset).

### `service-card` / `service-featured-card`
Navy gradient background, `1px solid var(--white-08)` border. Hover: `translateY(-6px)`, border turns `--red`, red shadow appears, top `::before` line fades in. Featured variant adds a 220px image container with gradient overlay.

### `portfolio-card`
`--navy-mid` background, 280px image height with `object-position: top center`. Hover: lift, red border, dark shadow, image scales to 1.03, skewed red stripe overlay fades in at 12% opacity.

### `service-icon`
52x52px, `rgba(196, 30, 42, 0.08)` background, `rgba(196, 30, 42, 0.2)` border, parallelogram clip-path. SVG icons at 22px, `stroke: var(--red)`, `stroke-width: 1.5`.

### `section-label`
Barlow Condensed 600, 14px, 5px tracking, uppercase, `--red` text. Preceded by a 30x2px red line via `::before`.

### `contact-form`
Navy gradient background, `white-08` border, 48px padding. Red gradient top accent line via `::before`. Inputs: `var(--white-04)` background, `white-08` border, focus border turns `--red`. Select uses `appearance: none`.

### `talent-pillar`
`var(--white-04)` background, `white-08` border, 28x24px padding. Numbered with Bebas Neue `--red` numerals (01-04). Hover: border shifts to `rgba(196, 30, 42, 0.3)`.

### Scroll reveal
`.reveal` elements start at `opacity: 0; translateY(30px)`, transition `0.7s ease`, staggered by sibling index (`0.1s` delay per item). Triggered at `threshold: 0.12` via IntersectionObserver.

## Do's and Don'ts

**Do:**
- Use the parallelogram clip-path on all interactive elements (buttons, icon containers). The angular shape is the brand signature.
- Keep all text uppercase for display and label typography. Sentence case is reserved for body/description copy only.
- Maintain the navy depth scale for layering: `navy-deep` (page) > `navy` (sections) > `navy-mid` (cards) > `navy-light` (nested panels).
- Use the white opacity scale for text hierarchy: 90% primary, 70% secondary, 50% tertiary, 30% quaternary.
- Apply `--skew: -12deg` consistently on all decorative stripe elements.
- Use `var(--red)` for all accent purposes -- borders on hover, labels, dividers, icons, buttons.

**Don't:**
- Do not add `border-radius` to cards, buttons, or containers. The design is deliberately sharp-edged.
- Do not use colors outside the defined palette. No grays, no additional accent colors.
- Do not use Barlow (body weight) for headings or Bebas Neue for body text. The type hierarchy is strict.
- Do not add box-shadow to default card states. Shadow appears only on hover as a reveal.
- Do not use flat red backgrounds on large surface areas. Red is always an accent, never a section background. The decorative stripes use 3-6% opacity for a reason.
- Do not use the podcast page's Instrument Serif / Outfit type stack on the main site. The two type systems are intentionally separated.
