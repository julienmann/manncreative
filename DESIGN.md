---
name: Mann Photography
description: Editorial photography portfolio for a Montréal-based photographer — precise, candid, dark by design.
colors:
  darkroom-amber: "#c4922a"
  accent-sport: "#b8552e"
  accent-events: "#6b3a44"
  accent-people: "#5f7a5e"
  accent-commercial: "#4c6478"
  void-black: "#000000"
  paper-white: "#ffffff"
  silver-gelatin: "#b0aba0"
  press-gray: "#888888"
  contact-shadow: "#111111"
  ivory-ground: "#eeeeee"
typography:
  display:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(7rem, 21vw, 22rem)"
    fontWeight: 400
    lineHeight: 0.82
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(3rem, 6vw, 6rem)"
    fontWeight: 400
    lineHeight: 0.95
  title:
    fontFamily: "Bebas Neue, sans-serif"
    fontSize: "clamp(2rem, 4vw, 3.5rem)"
    fontWeight: 400
    lineHeight: 1
  body:
    fontFamily: "IBM Plex Mono, monospace"
    fontSize: "0.88rem"
    fontWeight: 300
    lineHeight: 1.9
  label:
    fontFamily: "IBM Plex Mono, monospace"
    fontSize: "0.65rem"
    fontWeight: 400
    letterSpacing: "0.2em"
  serif-accent:
    fontFamily: "Playfair Display, Georgia, serif"
    fontWeight: 400
rounded:
  none: "0px"
  circle: "50%"
spacing:
  xs: "0.5rem"
  sm: "1.5rem"
  md: "2rem"
  lg: "3rem"
components:
  button-primary:
    backgroundColor: "{colors.paper-white}"
    textColor: "{colors.void-black}"
    rounded: "{rounded.none}"
    padding: "0.8rem 2.5rem"
  button-primary-hover:
    backgroundColor: "transparent"
    textColor: "{colors.paper-white}"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.paper-white}"
    rounded: "{rounded.none}"
    padding: "0.45rem 1.2rem"
  button-ghost-hover:
    backgroundColor: "{colors.paper-white}"
    textColor: "{colors.void-black}"
  tab-indicator:
    backgroundColor: "transparent"
    textColor: "{colors.silver-gelatin}"
    rounded: "{rounded.none}"
    padding: "1rem 2rem"
  tab-indicator-active:
    backgroundColor: "transparent"
    textColor: "{colors.paper-white}"
---

# Design System: Mann Photography

## 1. Overview

**Creative North Star: "The Darkroom"**

Everything in this system originates from the same physical logic as a film darkroom: a dark field is the correct surface for photographic work. The amber accent is the safelight — functional warmth, not decoration, present precisely where it needs to be and nowhere else. Typography is the enlarger: massive, compressed, controlled. The system is not dark because dark looks cool. It is dark because photographs read on dark surfaces, and a photographer who makes his livelihood from visual precision should build the container to match.

The aesthetic register is editorial-magazine crossed with photojournalism process. Think a working photographer's portfolio printed in a serious publication — not a lifestyle brand, not a tech startup, not a commercial agency showreel. The layout is grid-rigid, the voice is direct, and the visual language earns its confidence through restraint rather than assertion.

Three typefaces carry three entirely distinct roles: Bebas Neue is the wall voice — compressed headlines at near-zero line-height, structural, commanding. IBM Plex Mono is the workbench voice — every label, caption, body copy, and UI element. Playfair Display italic is the human voice — quotes, signatures, editorial asides where warmth needs to surface. These registers do not mix. Bebas does not appear small. Playfair does not appear upright. Mono does not try to be expressive.

**Key Characteristics:**
- Dark by function — the default theme is dark; photographs read better against it
- Compressed display typography at sub-1 line-height
- IBM Plex Mono as the system typeface for all functional text
- Playfair Display italic reserved strictly for human moments
- Zero border radius throughout the component layer — sharp cuts only
- Hierarchy through 1px hairline rules, never through shadow depth
- Five accent colors — one structural (Darkroom Amber) plus one per service vertical (Sport, Events, People, Commercial) — each individually capped at ≤10% of any screen, collectively still a minority of any view
- Example photography shown in full color at all times — no grayscale-at-rest treatment — so the work itself supplies the system's richest color
- Bilingual EN/FR with equal treatment of both languages

## 2. Colors: The Darkroom Palette

An achromatic field — deep blacks, warm near-whites, and mid-tones that read as silver gelatin prints — pierced by a single amber note.

### Primary
- **Darkroom Amber** (`#c4922a`): The structural, global accent. Used on section label underlines (2px), nav shadow (`rgba(196,146,42,0.25)`), manifesto border, and hero rule — wherever the accent isn't scoped to a specific service vertical. Never a background, never a fill, never used decoratively.
- **Vertical Accents**: Each service vertical carries one dedicated accent, used only within that vertical's own tab/gallery context (active tab indicator, tab-top border, gallery label underline) — never crossing into another vertical's markup, never used as fill:
  - **Sport — Rust** (`#b8552e`)
  - **Events — Wine** (`#6b3a44`)
  - **People — Sage** (`#5f7a5e`)
  - **Commercial — Slate** (`#4c6478`)

### Neutral
- **Void Black** (`#000000`): The primary background in dark mode. True black — photographs sit against it without a competing surface.
- **Paper White** (`#ffffff`): Primary foreground in dark mode; primary background in light mode. Used for all large typography, button fills, and primary interactive states.
- **Silver Gelatin** (`#b0aba0`): The working mid-tone in dark mode. Supporting text, metadata, labels, navigation links at rest, body copy. Warm-tinted toward amber — not neutral gray, not cool gray.
- **Press Gray** (`#888888`): The working mid-tone in light mode. Same role as Silver Gelatin but cooler.
- **Contact Shadow** (`#111111`): Secondary surface in dark mode — the interior of stat boxes, secondary containers. Provides surface depth without shadows.
- **Ivory Ground** (`#eeeeee`): Secondary surface in light mode. Mirrors Contact Shadow's structural role.

### Named Rules
**The Vertical Accent Rule.** Darkroom Amber remains the system's structural/global accent. Each service vertical additionally carries one dedicated accent, scoped strictly to that vertical's own DOM (its tab indicator, its tab-top border, its gallery label) — never mixed with another vertical's accent, never used as a fill, hover background, or gradient component. Collectively, all five accents still appear on ≤10% of any given screen; individually, each is rarer still.

**The Two-Mode Rule.** The system has a dark default and a light mode. Dark is primary. The amber accent does not change between modes; everything else inverts. Never introduce a third mode or a mode-specific accent variant.

## 3. Typography

**Display Font:** Bebas Neue (fallback: sans-serif)
**Body Font:** IBM Plex Mono (fallback: monospace)
**Accent Font:** Playfair Display (fallback: Georgia, serif)

**Character:** Three voices, three distinct registers, no overlap. Bebas compresses information into physical mass — it fills space the way a large-format print fills a wall. Mono makes everything feel precise, measured, and accountable. Playfair italic introduces the one moment of warmth and humanity the system allows itself.

### Hierarchy
- **Display** (400, `clamp(7rem, 21vw, 22rem)`, line-height 0.82, letter-spacing -0.02em): The hero title only. Bebas Neue. The name "MANN" at this scale is the visual anchor of the entire page.
- **Headline** (400, `clamp(3rem, 6vw, 6rem)`, line-height 0.95): Section headings ("JUST ME, A CAMERA, AND YOUR BRIEF"), contact headline. Bebas Neue. Structural, commanding.
- **Title** (400, `clamp(2rem, 4vw, 3.5rem)`, line-height 1): Service titles, work list items, process steps. Bebas Neue. Still large, but interactive — these expand, these react.
- **Body** (IBM Plex Mono, 300 weight, 0.88rem, line-height 1.9): All descriptive text — service descriptions, process explanations, about copy. Max line length 70ch.
- **Label** (IBM Plex Mono, 400 weight, 0.62–0.72rem, letter-spacing 0.2em, uppercase): Navigation links, tab buttons, "What's included" headers, contact detail labels, all UI metadata. The typeface for anything that organizes or names.
- **Serif Accent** (Playfair Display, italic, 1rem–1.6rem): The about signature ("— Julien Mann"), the manifesto quote, the hero typewriter phrases. Always italic. Never used for headings or labels.

### Named Rules
**The Three-Register Rule.** Bebas for wall text. Mono for functional text. Playfair for human moments. Each register has a job and stays in it. No Bebas below title scale. No Playfair upright. No Mono in display positions.

**The Compression Rule.** Bebas Neue headlines run at sub-1 line-height (0.82–0.95). Resist the urge to breathe them out. The compressed stack is intentional — it reads as a film contact sheet, not a layout with generous margins.

## 4. Elevation

This system is flat by default, with one deliberate exception.

All surface hierarchy is expressed through 1px hairline rules (`border: 1px solid rgba(--fg, 0.15)`) and background tonal steps (Void Black → Contact Shadow). No box-shadow for structural depth, no z-axis layering for content. A stat box is distinguished from its container by a shared hairline grid, not by a raised surface.

The hover preview card (`.work-item:hover` floating thumbnail) floats at z-index 400, implying depth through position alone with no shadow. Two further exceptions exist, both scoped to a single editorial moment rather than general UI: the **About accent photo** (a small overlapping print, rotated and shadowed, breaking out of the stats grid) and the **Featured Strip** middle image (elevated above its neighbors in the three-image spread between About and Services). In all three cases the lift is contextual and ephemeral — it marks a deliberate "photograph as object" moment, not a permanent UI surface state.

### Shadow Vocabulary
- **Amber Nav Underlighting** (`box-shadow: 0 1px 0 0 rgba(196,146,42,0.25)`): Applied to the fixed navigation only. Not a depth signal — a structural accent that grounds the nav against the page surface.
- **Lightbox Image Outline** (`box-shadow: 0 0 60px rgba(0,0,0,0.6)` + `outline: 2px solid rgba(255,255,255,0.8)`): Isolates the lightbox photograph in the overlay. Functional, not decorative.
- **Photo-Object Lift** (`box-shadow: 0 14px 32px rgba(0,0,0,0.35)` on the About accent image; `0 18px 40px rgba(0,0,0,0.4)` on the Featured Strip's middle image): Used only on photographs presented as physical, overlapping prints — never on cards, containers, or UI chrome.

### Named Rules
**The Hairline Rule.** Hierarchy comes from 1px rule lines and typographic scale — never from elevated surfaces or drop shadows on UI elements. The Photo-Object Lift exceptions above are the only places a photograph itself is allowed to cast a shadow; depth is earned, not decorative, and remains rare.

## 5. Components

### Buttons

Sharp-cornered, typographically-forward, two variants only.

- **Shape:** Zero radius (0px) — hard cuts throughout
- **Primary** (form submit, tab CTA): Filled with Paper White (`#ffffff`), text in Void Black (`#000000`), 1px solid border matching fill. IBM Plex Mono, 0.7rem, 400 weight, letter-spacing 0.2em, uppercase. Padding 0.8rem 2.5rem.
- **Primary Hover:** Transparent background, Paper White text, border remains. The fill inverts — the button opens up.
- **Ghost** (nav CTA, gallery toggle, lang toggle): Transparent background, Paper White border (1px solid), Paper White text. Padding 0.45rem 1.2rem. Fills on hover (reverse of primary).
- **Focus:** 2px outline in Darkroom Amber (`#c4922a`), 2px offset. The one place amber appears on interactive elements.
- **Transition:** `background 0.25s ease, color 0.25s ease` — no scale transforms, no positional shifts. The magnetic offset (`.magnetic`) is a micro-interaction layer, not a CSS state.

### Tab Indicators

Not filled states — indicator lines only.

- **Rest:** IBM Plex Mono, 0.7rem, letter-spacing 0.22em, uppercase. Silver Gelatin text. No background. Border-bottom: 2px solid transparent (reserving the space).
- **Active:** Paper White text. Border-bottom: 2px solid Darkroom Amber.
- **Hover:** Paper White text, border-bottom: 2px solid `rgba(196,146,42,0.35)` — the amber previewed at low opacity.

### Cards / Containers

The system avoids lifted cards. Content is organized through ruled grids.

- **Stat Box:** No radius, no shadow, no background distinction. Hierarchy comes from the shared hairline grid (`border: 1px solid var(--rule)` on all sides, nested grid with shared borders removed). Padding 2.5rem 2rem.
- **About Manifesto:** Double-border treatment — `border: 1px solid rgba(196,146,42,0.45)` (amber) plus `outline: 1px solid var(--rule)` at 5px offset. The only element in the system with an outline. Signals a quoted artifact, not a UI surface.
- **Work List Items:** No background, no card. Content delimited by 1px border-bottom rule. The item expands in place.

### Inputs / Fields

Open, newspaper-style. No box, no fill, no radius.

- **Style:** Transparent background. Bottom border only (`border-bottom: 1px solid var(--rule)`). No top, left, or right border.
- **Focus:** Bottom border shifts to Paper White (`border-bottom-color: var(--fg)`). Label floats upward (0.58rem, Paper White, letter-spacing 0.2em) via CSS transition.
- **Label:** Floating label pattern — starts at field top, moves to -1rem above on focus or fill. IBM Plex Mono, 0.65rem, uppercase, letter-spacing 0.2em.
- **Textarea:** Same treatment. Fixed height 5rem, no resize handle.
- **Select:** Appearance reset, monospace, 0.68rem, letter-spacing 0.12em. Silver Gelatin at rest.

### Navigation

Fixed header, auto-hides on scroll-down (returns on scroll-up).

- **Structure:** Full-width, max-width 1600px centered. Padding 0.9rem 3rem. Border-bottom 1px rule. Amber nav underlighting (shadow).
- **Logo:** Bebas Neue, 1.6rem, letter-spacing 0.08em. Text scramble on hover.
- **Links:** IBM Plex Mono, 0.7rem, letter-spacing 0.2em, uppercase. Silver Gelatin at rest, Paper White on hover.
- **CTA:** Ghost button (see Buttons). "Book Now" / "Réserver".
- **Mobile:** Nav links hidden. Controls (lang toggle + theme toggle + CTA) distributed across remaining width.

### Gallery Grid

A masonry layout on a 6-column track (`grid-auto-rows: 90px`, `grid-auto-flow: dense`), not a uniform 1:1 grid. Each thumbnail takes one of four spans:
- **Default:** 1 column × 4 rows.
- **`.is-wide`:** 2 columns × 4 rows.
- **`.is-tall`:** 1 column × 6 rows.
- **`.is-feature`:** 3 columns × 7 rows — one per gallery, the lead image.
- **Tablet (≤900px):** 3-column track; `.is-feature` spans all 3 columns.
- **Mobile (≤480px):** 2-column track; `.is-wide`/`.is-feature` span both columns.
- **Image treatment:** Full color at all times — no grayscale filter. 5% scale-up on hover (`transform: scale(1.05)`). Transition 0.4s ease.
- **Lightbox:** Black overlay (`rgba(0,0,0,0.92)`), full keyboard navigation (arrows, escape). Image outline: `outline: 2px solid rgba(255,255,255,0.8)`.

### Hover Preview Card

The system's one lifted element.

- **Size:** 220px wide, 3:4 aspect ratio.
- **Behavior:** Follows cursor position (lagged 10% per frame). Appears when hovering a `.work-item[data-preview]`. Scales from 0.9 to 1.0 with slight derotation on entry.
- **Style:** No border, no shadow — lift implied by fixed positioning and z-index alone.

## 6. Do's and Don'ts

### Do:
- **Do** use Bebas Neue only at title scale and above. The minimum meaningful use is the service tab title (`clamp(2rem, 4vw, 3.5rem)`).
- **Do** use IBM Plex Mono at 300 weight for all body copy and at 400 weight for all labels and UI text.
- **Do** reserve Playfair Display italic for quotes, signatures, and editorial asides — never for headings.
- **Do** let the dark background carry the photographs. Every layout choice should step back from the images, not compete with them.
- **Do** express hierarchy through 1px hairline rules and typographic scale. Use border-bottom / border-top, not box-shadow.
- **Do** use Darkroom Amber and the four vertical accents on ≤10% of any screen, collectively: rule lines, indicators, the nav underlighting, the manifesto border. No more.
- **Do** scope each vertical accent strictly to that vertical's own tab/gallery DOM — never mix accents within one tab-content block.
- **Do** let example photography render in full color at all times — the photographs are the system's color source; the chrome around them stays achromatic.
- **Do** maintain zero border-radius on all interactive components — buttons, inputs, tabs, cards, form selects.
- **Do** match letter-spacing to functional role: 0.2em or more for uppercase labels; near-zero or negative for Bebas headlines.
- **Do** apply `prefers-reduced-motion` media query to all entrance animations and transitions.
- **Do** run both EN and FR through any new copy — the site is bilingual with full parity.

### Don't:
- **Don't** use any accent color — amber or vertical — as a fill, a hover background, or a gradient component. The moment one fills a surface, the system loses its precision.
- **Don't** introduce rounded corners on components. Not `4px`, not `border-radius: 4px "for friendliness"`. Zero radius is a load-bearing decision.
- **Don't** add shadows to content cards, stat boxes, or section containers. Hairlines, not elevation — the only shadows in the system land on the three named Photo-Object Lift exceptions, never on UI chrome.
- **Don't** use this site's visual language to reference soft stock-photo photography aesthetics — no script fonts, no warm pastel backgrounds, no "capturing your precious moments" energy.
- **Don't** bring in SaaS/startup patterns: Inter or Geist fonts, blue or purple primary CTAs, white card grids with icon-heading-text repeated, metric highlight boxes. This is a photography portfolio.
- **Don't** use dark neon, purple gradients, cyan glows, or glassmorphism — wrong register entirely.
- **Don't** animate CSS layout properties (height, width, padding, margin). Use max-height transitions with cubic-bezier(.16,1,.3,1) for accordions; use opacity + transform for reveals.
- **Don't** use gradient text (`background-clip: text`). Typography uses a single solid color.
- **Don't** use side-stripe left borders as accent treatments on any list item, card, or callout. The accent appears as bottom-border on tabs and as rule lines — never as a left-side stripe.
- **Don't** add Bebas Neue below title scale. Using it at 12px or 14px destroys the typeface's character and looks like fallback font styling.
