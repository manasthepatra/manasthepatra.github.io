# Field Signal — Design System

## Purpose

This portfolio presents **Manas Ranjan Patra** as a geologist-turned-geospatial data scientist. It is a field notebook translated into a precise digital atlas: evidence-led, calm under pressure, and grounded in places, measurements, and the people affected by them.

The site should make a visitor understand three things quickly:

1. Manas works at the intersection of earth observation, GIS, and data science.
2. His work converts complex spatial data into decisions for climate resilience, infrastructure, and environmental intelligence.
3. Pune Heat Risk is a credible, living example of that practice.

## Identity

**Name:** Field Signal

**Visual idea:** a topographic survey sheet at dusk. Fine latitude/longitude lines establish place; warm thermal contours identify risk; cool blue-green surfaces carry analysis and trust. The visual language comes from maps and raster data rather than a generic technology dashboard.

**Voice:** direct, observant, technical without jargon, and specific about evidence. Prefer verbs such as *map, measure, trace, model,* and *interpret*. Every claim should point to a method, a result, or a source.

## Colour

The default interface is dark. It resembles a night field sheet and lets thermal colour encode urgency without becoming flashy. Light surfaces appear only inside data figures, document previews, and accessible form elements where they improve reading.

| Token | Value | Use |
|---|---:|---|
| `--ink` | `#101916` | Main background |
| `--ink-raised` | `#17241F` | Header, panels, footer |
| `--ink-line` | `#31443D` | Borders, grid lines, dividers |
| `--paper` | `#F2F0E8` | Primary text, light data surface |
| `--paper-muted` | `#B9C2B9` | Secondary text |
| `--lichen` | `#9CC6A2` | Links, positive data, primary action |
| `--river` | `#6EB6C8` | Spatial analysis accent |
| `--heat` | `#F36D4A` | Heat-risk accent and important metrics |
| `--sun` | `#F2BF58` | Highlights, active state, metadata marker |

Text must meet WCAG AA contrast against its immediate surface. `--heat` is an emphasis colour, never the sole carrier of meaning; charts and labels must add shape, text, or pattern.

## Typography

Use locally hosted or self-hosted font files where possible; do not depend on a web-font request for first paint.

- **Display and headings:** `Space Grotesk`, then `Arial`, sans-serif. Geometric but human, for page titles and numerical callouts.
- **Body and interface:** `Inter`, then `Arial`, sans-serif. Designed for dense reading at small sizes.
- **Data and coordinates:** `IBM Plex Mono`, then `Consolas`, monospace. Reserved for labels, tags, code, dates, and numerical evidence.

| Role | Desktop | Mobile | Treatment |
|---|---:|---:|---|
| Display title | clamp(3.5rem, 8vw, 8rem) | 3.25rem | 0.94 line-height, -0.055em tracking |
| Page title | clamp(2.5rem, 5vw, 5.5rem) | 2.75rem | 0.98 line-height |
| Section title | 2rem | 1.75rem | 1.05 line-height |
| Body | 1.05rem | 1rem | 1.65 line-height, 65–72ch max measure |
| Meta / labels | 0.72rem | 0.72rem | Mono, uppercase, 0.12em tracking |

## Layout and spacing

- **Content width:** 1200px maximum with 24px gutters on small screens and 48px from tablet upward.
- **Editorial reading column:** 720px maximum for case-study prose.
- **Grid:** 12 columns on desktop, 6 on tablet, 4 on small screens. Use the grid to align labels, figures, and actions; do not create arbitrary card columns.
- **Spacing unit:** 4px. Use `4, 8, 12, 16, 24, 32, 48, 64, 96, 128, 160` only.
- **Section rhythm:** 128px desktop / 80px mobile. Case-study sections use 96px / 64px.
- **Borders:** 1px `--ink-line`; avoid soft shadows. Raised content is signalled through a surface change and a crisp border.

## Signature motifs

### Coordinate frame

Each major page opens within a small monospace coordinate frame: section index, location, and project status. It lends an atlas structure and doubles as useful metadata.

### Contour field

A low-contrast CSS/SVG contour pattern sits behind the hero and large section breaks. It remains static by default, has no effect on legibility, and is omitted under reduced-motion and high-contrast modes.

### Evidence markers

Key outcomes are rendered as large numbers with a short label, source, and scope. A metric must never be detached from its meaning. Example: `3 STORIES / PUNE HEAT RISK / WARD · CLIMATE · THERMAL`.

### Map annotation

Use fine leader lines, coordinate ticks, and captions around project imagery. Decorative texture must never cover interactive controls or reading text.

## Component conventions

### Navigation

Sticky top bar with the `MP` monogram, four anchor links (`Work`, `Practice`, `About`, `Contact`), and a compact resume action. On narrow screens, it becomes an accessible menu panel. The current section is indicated with text and a 2px rule.

### Buttons and links

Primary action: lichen fill with ink text. Secondary action: transparent with 1px border. Text links carry an animated underline on hover and a persistent visible focus ring. External destinations state that they open a new site through an icon and accessible label.

### Case-study feature

Pune Heat is a wide editorial feature, not a card:

- project index `01`, context `Pune, India · 2026`
- a large thermal/map image or composed raster figure
- a one-sentence outcome statement
- method tags in mono text
- two direct actions: `Read case study` and `Open live project`

The dedicated page follows: **Situation → Questions → Spatial approach → What the evidence shows → Tools and data → Live experience → Reflection**. It must disclose the IITM Climate Lab internship role and list data sources supplied by the project.

### Skills

Skills are a readable capability index, arranged by what Manas can do: `Analyse`, `Observe`, `Model`, `Publish`, and `Operate`. A tool appears once, with grouped technology names rather than icon clouds or proficiency bars.

### Timeline

Experience and education use an anchored vertical survey line. Each entry gives role, organisation, time/place, contribution, then evidence. The IITM Pune Heat role appears first.

### Contact

End on one generous contact panel with email as the primary action and GitHub, LinkedIn, phone, and Pune location as concise supporting details. The resume button must link directly to the provided PDF.

## Motion

Motion conveys progression through evidence:

- Short opacity and translate reveals: 180–300ms, `cubic-bezier(.2,.8,.2,1)`.
- Contour/leader-line drawings may reveal once as their section enters view.
- Hover states: 150ms maximum; no large scaling or layout movement.
- Never hijack scroll, autoplay a video, or make navigation depend on animation.
- Respect `prefers-reduced-motion: reduce`: show final states immediately, stop decorative contour movement, and preserve every interaction.

## Responsive and accessibility rules

- HTML landmarks, a skip link, meaningful heading hierarchy, keyboard-operable navigation, and visible `:focus-visible` states are mandatory.
- Do not place essential copy inside images. Each project visual has specific alt text or a nearby text equivalent.
- Use fluid type and grid collapse; no horizontal scrolling at 320px.
- Tap targets are at least 44 by 44px.
- Images use explicit dimensions, modern compressed formats, and lazy loading below the fold. The hero’s critical visual is optimised and preloaded only when it materially improves perceived load.

## Application across the Pune Heat destination

The portfolio will use a dedicated Pune Heat case-study page as the branded entry point. Its `Open live project` link leads to the existing separately hosted scrollytelling application.

To make the separate application visually continuous in a later shared update, use the same identity tokens there: `#101916`, `#F2F0E8`, `#9CC6A2`, `#6EB6C8`, `#F36D4A`, Space Grotesk, Inter, IBM Plex Mono, coordinate metadata, and reduced-motion behaviour. The implementation will not claim that continuity is complete until the `pune-heat-risk` repository is available in scope for that update.

## Content architecture

1. **Home** — proposition, featured Pune Heat evidence, capabilities, experience signal, contact.
2. **Pune Heat case study** — focused evidence-led project narrative and live-project handoff.
3. **About / CV** — background, education, certifications, complete capabilities, downloadable resume.
4. **Contact** — reachable from every page and the site footer.

The first build may render this as a focused one-page home plus a dedicated `/pune-heat/` case-study route; `About` and `Contact` anchor sections keep initial navigation fast and clear.
