# Handoff: Founder's +1 — Coming Soon page

## Overview
A single-page "coming soon" holding site for foundersplusone.com. Its purpose is basic online presence while the full website is built: brand logo, a clear "new website coming soon" message, a short positioning line, and a contact email.

## About the Design Files
`index.html` in this folder is a **design reference created in HTML**. For a page this simple it is close to production-ready and can be deployed as-is (static file, no build, no JS). If the site lives in an existing codebase/framework (Next.js, Astro, etc.), recreate it there using its conventions; otherwise shipping the static `index.html` is the recommended approach.

## Fidelity
**High-fidelity.** Final colors, typography, spacing and copy. Recreate pixel-for-pixel.

## Screen: Coming Soon (single page)
**Layout:** full-viewport column (`min-height: 100vh`, flex column). Three stacked regions:
1. **Header** — centered, padding `40px 24px 0`.
2. **Main** — `flex: 1`, content centered horizontally and vertically, `text-align: center`, padding `64px 24px`.
3. **Footer** — centered, padding `0 24px 32px`.

Background: flat `#0A1124` (no gradient, no glow — intentionally, to avoid a SaaS look). Text default `#FFFFFF`.

### Components
**Logo (wordmark, header)** — text, not an image: `FOUNDER'S` + `+1`.
- Inter Tight 800, 24px, letter-spacing −0.02em, line-height 1, color `#FFFFFF`
- `+1` in `#C58CFF`, margin-left 3px
- (PNG versions also exist in the project `logo-png/` folder if an image is preferred.)

**Status pill ("New website coming soon")**
- Copy: `New website coming soon` (uppercase via CSS)
- JetBrains Mono 500, 14px, letter-spacing 0.18em, `text-transform: uppercase`, color `#FFFFFF`
- Inline-flex, gap 12px, padding `10px 20px`, border `1px solid rgba(197,140,255,0.45)`, radius 999px, margin-bottom 32px
- Leading dot: 7×7px circle, `#C58CFF`, pulsing: `@keyframes pulse` over 2s ease-in-out infinite — opacity 1 → 0.45 → 1, with a ring `box-shadow: 0 0 0 0 rgba(197,140,255,0.6)` expanding to `0 0 0 6px rgba(197,140,255,0)` at 50%. Disabled under `prefers-reduced-motion: reduce`.

**Headline (h1)**
- Copy: `Your strategic plus-one.`
- Inter Tight 600, `font-size: clamp(36px, 5.5vw, 60px)`, letter-spacing −0.025em, line-height 1.05, margin-bottom 28px, `text-wrap: balance`

**Intro paragraph**
- Copy: `I help founders and commercial teams sharpen positioning, improve go-to-market execution, and move faster. The full website is on its way; until then, get in touch directly.`
- Inter Tight 400, `clamp(17px, 2vw, 19px)`, line-height 1.55, color `rgba(255,255,255,0.72)`, max-width 520px, margin-bottom 44px, `text-wrap: pretty`

**Contact line**
- Copy: `Reach me at ` + link `johan@foundersplusone.com` (`mailto:johan@foundersplusone.com`)
- Same size/color as intro paragraph
- Link: weight 600, color `#C58CFF`, no underline, `border-bottom: 1px solid rgba(197,140,255,0.5)`, padding-bottom 2px
- Hover: color `#FFFFFF`, border-color `#FFFFFF`
- Focus-visible: `outline: 2px solid #C58CFF; outline-offset: 4px`

**Footer**
- Copy: `© 2026 Founder's +1`
- JetBrains Mono 500, 12px, letter-spacing 0.08em, color `rgba(255,255,255,0.5)`

## Interactions & Behavior
- Interactions: email link (mailto) with hover/focus states as above, and the pulsing status dot (CSS only). No JS.
- Responsive: fully fluid via `clamp()` sizes and 24px side padding; no breakpoints needed. Verify at 360px wide that the pill and email fit on one line each.

## State Management
None.

## Design Tokens
- Background: `#0A1124`
- Purple (brand primary, not used on this page but part of the system): `#8A2BE2`
- Purple deep: `#5B16B0`
- Purple light (on dark): `#C58CFF`
- Text: `#FFFFFF`; muted `rgba(255,255,255,0.72)`; subtle `rgba(255,255,255,0.5)`
- Fonts: Inter Tight (400/600/800), JetBrains Mono (500) — Google Fonts
- Radius: 999px (pill)

## SEO / meta
- `<title>Founder's +1 · GTM Advisory</title>`
- `<meta name="description" content="Founder's +1: go-to-market advisory for founders and commercial teams. New website coming soon.">`
- Recommended additions for production: Open Graph title/description/image.
- Favicon: `favicon.png` (1024×1024, F+1 on ink, rounded corners), linked as `rel="icon"` and `rel="apple-touch-icon"`. Keep it next to `index.html` when deploying.

## Assets
No images other than `favicon.png`. Fonts load from Google Fonts.

## Files
- `index.html` — the complete page (self-contained HTML + CSS).
- `favicon.png` — browser tab / home-screen icon.
