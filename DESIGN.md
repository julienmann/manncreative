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
- Photographs recur throughout the page, not only inside the service galleries: a contact sheet under the hero, two full-bleed moving bands, a quote plate, a staggered featured spread
- Every frame carries a 1px inset hairline so dark photographs keep their edges against the black field
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

The hover preview card (`.work-item:hover` floating thumbnail) floats at z-index 400, implying depth through position alone with no shadow. Two further exceptions exist, both scoped to a single editorial moment rather than general UI: the **About accent photos** (two small overlapping prints, rotated and shadowed — one breaking over the column rule above the stats grid, one over the bottom-left corner of the About figure) and the **Featured Strip** middle image (elevated above its neighbours in the five-image spread between About and Services). In all three cases the lift is contextual and ephemeral — it marks a deliberate "photograph as object" moment, not a permanent UI surface state.

Both About prints anchor to a real element — a grid, a figure — never to the bottom of a stretched column. A print floating in leftover space reads as a layout accident, not an object.

### Shadow Vocabulary
- **Amber Nav Underlighting** (`box-shadow: 0 1px 0 0 rgba(196,146,42,0.25)`): Applied to the fixed navigation only. Not a depth signal — a structural accent that grounds the nav against the page surface.
- **Lightbox Image Outline** (`box-shadow: 0 0 60px rgba(0,0,0,0.6)` + `outline: 2px solid rgba(255,255,255,0.8)`): Isolates the lightbox photograph in the overlay. Functional, not decorative.
- **Photo-Object Lift** (`box-shadow: 0 14px 32px rgba(0,0,0,0.35)` on the About accent images; `0 18px 40px rgba(0,0,0,0.4)` on the Featured Strip's middle image): Used only on photographs presented as physical, overlapping prints — never on cards, containers, or UI chrome.
- **Frame Edge** (`outline: 1px solid var(--rule); outline-offset: -1px`): Not a shadow at all — the hairline every photographic frame carries on its inside edge, so a dark photograph doesn't dissolve into the black field. Applied to gallery thumbs, band frames, hero sheet frames, contact strip frames, featured frames, and the About figure. It replaces elevation entirely for photographs that are not Photo-Object Lifts.

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

### Section Numeral

The `NN / 04` marker in each section header is Bebas Neue at `clamp(2.5rem, 6vw, 6rem)`, drawn as an outline — `color: transparent` with `-webkit-text-stroke: 1px var(--rule)`, guarded by an `@supports` query that leaves it solid Silver Gelatin where text-stroke is unavailable. It is a structural watermark, not a label: never filled, never colored, never below Bebas title scale.

### Navigation

Fixed header, auto-hides on scroll-down (returns on scroll-up).

- **Structure:** Full-width, max-width 1600px centered. Padding 0.9rem 3rem. Border-bottom 1px rule. Amber nav underlighting (shadow).
- **Logo:** Bebas Neue, 1.6rem, letter-spacing 0.08em. Text scramble on hover.
- **Links:** IBM Plex Mono, 0.7rem, letter-spacing 0.2em, uppercase. Silver Gelatin at rest, Paper White on hover.
- **CTA:** Ghost button (see Buttons). "Book Now" / "Réserver".
- **Mobile:** Nav links hidden. Controls (lang toggle + theme toggle + CTA) distributed across remaining width.

### Gallery Grid

A composed spread on a 6-column track, not a uniform grid and not a masonry flow. Six frames per vertical resolve into an exact rectangle — no ragged edge, no holes:
- **`.is-feature`:** `grid-column: 1/5; grid-row: 1/3` — the lead frame, spanning both rows of the upper block. No aspect-ratio of its own; it takes its height from the pair beside it.
- **`.is-stack`:** `grid-column: 5/7`, aspect-ratio 4:3 — two of them, stacked in the right two columns beside the lead.
- **`.is-third`:** `span 2`, aspect-ratio 3:2 — three of them across the row underneath.
- **Tablet/mobile (≤900px):** two columns. The lead goes full width at 4:3, the middle four sit two-up at 4:3, and the last frame closes full width at 2:1.
- **Image treatment:** Full color at all times — no grayscale filter. `object-fit: cover` inside the frame; 5% scale-up on hover. Frame Edge hairline on every thumb.
- **Frame metadata** (`.frame-meta`): a contact-sheet annotation, not a caption card. Bottom-anchored, IBM Plex Mono 0.55rem / 0.22em uppercase over a black-to-transparent scrim (functional legibility, never an accent fill). Left slot is a three-letter vertical code and frame number — `SPT · 03`, `EVT · 01`, `PPL · 05`, `SEL · 02` — deliberately language-neutral so it needs no translation. Right slot is the localized "View +". Fades in on hover; always visible on `hover: none` devices.
- **Lightbox:** Black overlay (`rgba(0,0,0,0.92)`), full keyboard navigation (arrows, escape). Image outline: `outline: 2px solid rgba(255,255,255,0.8)`.

### Photo Band

A full-bleed contact sheet in motion — the one component that breaks the 1600px measure. One runs after the hero, one before Contact, in opposite directions.

- **Structure:** A hairline header row (label + frame count, both mono 0.58rem / 0.28em uppercase in Silver Gelatin) over an `overflow: hidden` viewport holding the track. The label lives in the header, never floated over a photograph.
- **Motion:** `translateX(0 → -50%)` over 75s linear, infinite. The track's children are cloned once in JS so the loop is seamless; clones carry `aria-hidden` and `data-clone`, take no tab stop, and resolve to the original frame's index when clicked.
- **Direction:** `data-dir="reverse"` flips the second band.
- **Pause:** on hover and on focus-within.
- **Frames:** height `clamp(140px, 17vw, 240px)`; landscape frames run 1.45× that height wide, `.is-portrait` frames 0.72×.
- **Reduced motion:** animation off, band becomes `overflow-x: auto` — a contact sheet you scroll by hand.

### Interstitial

A full-bleed photographic plate carrying one line of Playfair italic, placed between Services and Process.

- **Height:** `clamp(380px, 62vh, 640px)`; `clamp(320px, 52vh, 460px)` under 900px.
- **Scrim:** `linear-gradient(to top, rgba(0,0,0,0.85), rgba(0,0,0,0.45) 48%, rgba(0,0,0,0.15))` — the minimum needed to hold white text at AA over any frame.
- **Type:** Playfair Display italic, `clamp(1.5rem, 3.6vw, 3rem)`, max 22ch, white in both modes. This is a photographic plate, not a page surface — it does not invert with the theme.
- **Parallax:** the image sits in a `inset: -12% 0` box and translates ±8% on scroll, rAF-throttled. Disabled outright under `prefers-reduced-motion`.

### Hero Contact Sheet

Six frames in a 6-column row directly under the hero's bottom rule — evidence before a single line of body copy. Frame height `clamp(72px, 7.5vw, 116px)`, mono index (`01`–`06`) in the top-left corner at `mix-blend-mode: difference`. Under 900px it drops to three frames. The hero photograph's bottom edge is pinned to the top of this row (`bottom: calc(3.5rem + var(--sheet-h))`) so the image never bleeds past it.

### Featured Strip

Five frames between About and Services, bottom-aligned in layout and knocked off that line with `transform: translateY()` — never with margins, which would only inflate the row. The middle frame is the anchor: widest column, tallest ratio, and the one Photo-Object Lift. Captions sit under each frame in the same three-letter contact-sheet code as the galleries. Below 900px the offsets are removed and the strip becomes a plain two-up sheet.

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
- **Do** give every photographic frame the Frame Edge hairline. A dark photograph without one has no boundary on a black field.
- **Do** keep frame annotations language-neutral where a three-letter code will do (`SPT`, `EVT`, `PPL`, `SEL`) — it reads as a photographer's shorthand and spares the translation table.
- **Do** anchor overlapping prints to a real element — a grid, a figure, a frame edge. Never to the bottom of a stretched column.
- **Do** offset editorial frames with `transform: translateY()`, and give the section the padding to absorb it.

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
- **Don't** float a band or plate label over a photograph and hope blend modes save it. Labels belong on a hairline header row.
- **Don't** let a photo band animate under `prefers-reduced-motion` — it becomes a hand-scrolled sheet, not a paused one.
- **Don't** present work from one vertical as another's. The Commercial tab shows selected frames under an explicit "full commercial portfolio on request" line rather than relabelling event or sport work.
