# Event Listing

A small static website that lists upcoming events. Designed for youth-oriented events with an Energetic Coral theme.

## Files

- `index.html` — main page markup
- `style.css` — styling, color variables, layout, and animations
- `Images/` — place hero and event images here (e.g., `Images/hero.jpg`)

## Preview

Open `index.html` in your browser. 

Or use VS Code Live Server extension to preview and auto-reload.

## Customization

- Hero image
- Colors: edit variables at the top of `style.css` (`:root`) — `--p`, `--s`, `--a`, `--bg`, `--text`, `--muted`.
- Buttons: `.btn.primary` and `.btn.secondary` provide primary and accent styles.
- Events: each event is an `<article class="event-item">`.I have Use `<time datetime="YYYY-MM-DD">` for machine-readable dates and `figure`/`figcaption` for images.

## Accessibility & Notes

- Headings follow a logical order (h1 → h2 → h3). Ensure you keep that structure when adding content.
- Buttons and links have visible focus styles. Test with keyboard navigation.
- Animations are subtle; if you need to disable them for reduced-motion users, add `@media (prefers-reduced-motion: reduce)` rules in `style.css`.

## Design choices (brief)

- Layout
	- Fixed header with a centered brand and navigation. This keeps the main navigation always available.
	- Hero section uses a full-bleed background image with a centered content container (flexbox) and a subtle gradient overlay for legibility.
	- Events are laid out using CSS Grid (`.event-list` uses `auto-fit`/`minmax`) so cards adapt to available width.
	- Contact form is a two-column grid on desktop and stacks to a single column on small screens for easy input on phones.

- Color scheme
	- "Energetic Coral" palette: primary coral (`--p: #FF6B6B`), accent teal (`--a: #4ECDC4`), sunny yellow (`--s: #FFE66D`) with neutral background and charcoal text.
	- Colors are defined as CSS variables in `:root` to make theme adjustments straightforward.
	- Contrast and accessibility: CTAs use high-contrast text (white on coral) and focus outlines are visible for keyboard users.

- Responsive approach
	- Mobile-first responsive rules with media queries at 720px and a small tweak at 420px for touch targets.
	- Header switches to a hamburger toggle on small screens; the menu expands/collapses smoothly via a small JS toggle.
	- Grid layout uses `repeat(auto-fit, minmax(...))` so event cards flow naturally without manual breakpoints.
	- `prefers-reduced-motion` is respected; animations are disabled for users who opt out.

These choices prioritize clarity, accessibility, and a bright, youthful visual language that scales well between phones and large displays.