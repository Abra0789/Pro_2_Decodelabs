# Stockwise — Project 2: Responsive Web Layout

DecodeLabs Frontend Development Industrial Training (Batch 2026)
Theme: "The Art of Fluidity" - Building Responsive Architectures from the Content Out

A fully responsive, 4-page marketing site for a fictional inventory-management product (Stockwise) - inspired by the spirit of a StockTrack-style dashboard product, built with an original name and design. Pure HTML5 and CSS3 - no JavaScript, no frameworks.

## Pages

- `index.html` - Home (hero, trust strip, features teaser, How It Works, CTA)
- `features.html` - Features (3 spotlight sections + a compact grid of the rest)
- `pricing.html` - Pricing (3-tier plan grid)
- `contact.html` - Contact (info + message form)

## What it demonstrates

- Mobile-first CSS - base styles are mobile, enhanced with `min-width` media queries at 768px (navigation, spacing) and 1024px (hero, How It Works, spotlights, contact form)
- CSS Grid for macro layout - `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))` on the features grid, pricing grid, dashboard stats, and footer columns, so columns adapt to available space instead of locking to a fixed count
- Flexbox for component-level arrangement - nav bar, buttons, hero content, card internals, spotlight rows
- Fluid typography via `clamp()` throughout (e.g. `font-size: clamp(1rem, 2.5vw, 2rem)` on the dashboard stat numbers)
- Fluid units - %, rem, vw
- Responsive navigation: hamburger on mobile using the native HTML **Popover API** (`popovertarget` / `popover` attributes) - zero JavaScript
- 44×44px minimum touch targets on every interactive control
- No restricted zoom - `initial-scale=1` only, no `maximum-scale` or `user-scalable=no`
- One CSS **Container Query** on the feature cards (forward-looking, per the brief's "Future-Proofing the Web" note)
- Semantic HTML, `aria-current="page"` on the active nav link, visible focus states, `prefers-reduced-motion` respected
- Every dashboard preview is a hand-built HTML/CSS mockup (stat cards, bar chart, product table) — **no images used anywhere in this project**

## Structure

```
project2/
├── index.html
├── features.html
├── pricing.html
├── contact.html
└── css/
    └── style.css
```

## Testing responsiveness

Resize the browser or use DevTools' device toolbar. Worth checking specifically: 320px, 360px, 375px, 480px, 768px, 1024px, and a large desktop width — the layout should never scroll horizontally at any of these.

## Viewing locally

Open `index.html` directly in a browser. No build step, no dependencies.
