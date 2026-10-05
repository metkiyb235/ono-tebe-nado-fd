# "Оно тебе надо" — Auction Landing Page
(https://github.com/metkiyb235/ono-tebe-nado-fd)
A single-page website for a fictional auction of "things nobody believed in."
Built with pure HTML and CSS as a layout practice project.

## What I built

- **Semantic HTML5 structure**: `header`, `main` (with three `section`s), `footer`.
- **Custom fonts** loaded via a separate `fonts.css`.
- **Split stylesheets**: `global.css` for base/reset, `style.css` for layout.

## Sections

### 1. Header
- Three-column CSS Grid: navigation menu, logo, contacts.
- Navigation list with `list-style-position: inside` markers.
- Right-aligned contacts block via `justify-self: end`.

### 2. Cover (hero)
- Full-height section with a darkened background image (`filter: brightness`).
- The heading "ОНО ТЕБЕ НАДО" is split into three `<span>`s placed with a
  3×3 CSS Grid using named `grid-template-areas`.
- `letter-spacing`, uppercase transform, and small `translate` offsets match
  the Figma mockup.
- Bottom row: tagline + "Сделать ставку" button (flex, `margin-left: auto`).

### 3. Lots
- Three-column Grid of cards.
- Each card = darkened image + underlined title + description.
- Flexbox inside each card pins the description to the bottom.

### 4. About
- Two-column Grid: circular logo badge on the left, text block on the right.
- The badge is a black `border-radius: 50%` container with a white logo.

### 5. Footer
- Three-column Grid: contacts, menu, social icons.
- Icons laid out with flex and `gap`.

## Techniques practiced

- CSS Grid: `grid-template-columns`, `grid-template-rows`,
  `grid-template-areas`, `justify-self`, `align-self`.
- Flexbox: `justify-content`, `align-items`, `gap`, `margin: auto`.
- Positioning: absolute background images under `position: relative` content,
  `z-index` layering.
- Typography: `letter-spacing` (converted from Figma % to `em`),
  `text-transform: uppercase`, custom underlines.
- Pixel-perfect matching of a Figma mockup.

## Known limitations

- Fixed `width: 1100px` on `body` — desktop-only, no responsive layout.
- A few spots rely on `transform: translate(...)` for fine positioning, which
  is brittle; a cleaner grid/flex approach would be better in production.
- Some paddings/margins are hardcoded to match the mockup rather than driven
  by design tokens.
