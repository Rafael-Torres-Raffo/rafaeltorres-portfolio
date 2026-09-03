# Rafael Torres Portfolio — Design & Content Rules

## Design system (already established — extend it, don't reinvent it)

**Palette**
- Background: `#F7F9FC`, panels: `#FFFFFF` / `#EEF2F8`
- Accent (single, consistent): `#3D6BFF` (bright) / `#2E55D9` (mid) — used for links, active nav state, borders, chart lines, connector diagrams
- Text: `#111826` (primary), `#4B5567` (secondary), `#8993A6` (tertiary/labels)
- Borders: `rgba(17,24,38,0.10)` default, `rgba(61,107,255,0.40)` accent-bright

**Typography**
- Headings/display: Space Grotesk
- Body: IBM Plex Sans
- Labels, nav, captions, code, stats: IBM Plex Mono (uppercase, letter-spacing ~0.03–0.04em for labels)

**Component patterns already in use — reuse these, don't invent new ones for the same job**
- `.card.featured` — project grid cards (status pill, pin/date line, title, description, tags, CTA)
- `.annotation` — callout box with a `→ LABEL` arrow-header, used for "here's the interesting technical detail" moments
- `.stat-grid` — 3-column quick stats (number + label)
- `.component-legend` / `.cl-item` — labeled definition cards (used for requirement mappings, part lists)
- `.video-links` / `.video-link` — row-style link items (papers, GitHub repos, videos) with a title/description/action-label layout
- `.quote-block` — pulled-quote styling for a single standout line
- `.video-slot` — dashed placeholder box for pending video content

## Content rules

- **No fabricated content.** Every claim, number, and story on this site comes from what Rafael has actually told me. Never invent achievements, quotes, team members, or results to fill space.
- **Em-dash discipline.** Do not use em-dashes as a repeated sentence-interruption device ("X — which does Y — Z"). Vary sentence structure: periods for two full thoughts, colons for definitions/lists, parentheses for asides. Em-dashes are fine in titles/headings ("ASCEND — A-150") since that's a distinct, idiomatic convention, not a prose tic.
- **No overclaiming.** If something is uncertain (a label on a photo, a technical detail I'm inferring), say so plainly rather than asserting it as fact.
- **Match the person's voice**, especially on the About page — preserve Rafael's own phrasing over "portfolio voice" wherever both are viable.

## Architecture

- Single-page app: one `index.html`, `showView(name)` JS function toggles `.view` sections, no routing library, no build step.
- Assets are real files under `assets/<project>/`, not embedded base64 — keep it that way for load performance.
- Nav should stay short. Individual project pages live behind a "Projects" hub, not directly in top nav.

## Before making visual changes

Read the installed frontend-design plugin's skill principles first: avoid generic AI-default layouts, choose a specific aesthetic direction deliberately, and check that any new component doesn't fight the CSS specificity of existing .card, .annotation, or .stat-grid rules.
