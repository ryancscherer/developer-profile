---
name: Scherer Developer
description: A Brisbane, Australia developer's landing page — proof by demonstration, not by claim.
colors:
  paper: "#F6F7FA"
  surface: "#FFFFFF"
  line: "#E1E5EE"
  ink: "#14181F"
  ink-dim: "#4C5468"
  ink-faint: "#626C83"
  primary: "#2C864D"
  primary-deep: "#216C3C"
  primary-wash: "#E7F3EC"
  secondary: "#16B4D6"
  secondary-deep: "#0B7E99"
  secondary-wash: "#E5F7FB"
  tertiary: "#E8465F"
  tertiary-deep: "#B32E43"
  accent-gold: "#C98A2A"
  accent-violet: "#7C5CE0"
typography:
  display:
    fontFamily: "Cascadia Mono, SFMono-Regular, Consolas, Liberation Mono, Courier New, ui-monospace, monospace"
    fontSize: "clamp(2rem, 5vw, 3.7rem)"
    fontWeight: 700
    lineHeight: 1.08
    letterSpacing: "-0.01em"
  headline:
    fontFamily: "Cascadia Mono, SFMono-Regular, Consolas, Liberation Mono, Courier New, ui-monospace, monospace"
    fontSize: "clamp(1.6rem, 3vw, 2.3rem)"
    fontWeight: 700
    lineHeight: 1.15
    letterSpacing: "-0.01em"
  title:
    fontFamily: "Cascadia Mono, SFMono-Regular, Consolas, Liberation Mono, Courier New, ui-monospace, monospace"
    fontSize: "clamp(1.4rem, 2.4vw, 1.95rem)"
    fontWeight: 700
    lineHeight: 1.2
    letterSpacing: "-0.01em"
  body:
    fontFamily: "Segoe UI, -apple-system, BlinkMacSystemFont, Helvetica Neue, ui-sans-serif, sans-serif"
    fontSize: "1.05rem"
    fontWeight: 400
    lineHeight: 1.6
    letterSpacing: "normal"
  label:
    fontFamily: "Cascadia Mono, SFMono-Regular, Consolas, Liberation Mono, Courier New, ui-monospace, monospace"
    fontSize: "0.75rem"
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "0.12em"
rounded:
  xs: "4px"
  sm: "10px"
  md: "12px"
  lg: "16px"
  pill: "999px"
spacing:
  xs: "8px"
  sm: "16px"
  md: "24px"
  lg: "40px"
  xl: "64px"
  2xl: "100px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.surface}"
    typography: "{typography.body}"
    rounded: "{rounded.sm}"
    padding: "14px 26px"
  button-primary-hover:
    backgroundColor: "{colors.primary-deep}"
  button-ghost:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink-dim}"
    typography: "{typography.body}"
    rounded: "{rounded.sm}"
    padding: "14px 26px"
  chip-tag:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.ink-dim}"
    typography: "{typography.label}"
    rounded: "{rounded.pill}"
    padding: "10px 16px"
  card-feature:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: "14px"
---

# Design System: Scherer Developer

## 1. Overview

**Creative North Star: "The Shipped Build"**

This system is not a mockup pretending to be a product — it's a landing page built from pieces of two products that actually run. Every color on the page is a color that already exists somewhere in Vicki the Manager or Pop Shot; every headline is set in the same typographic register as the code that built them. The page's job is to feel like scrolling through working software, not a sales brochure about working software.

It explicitly rejects the small-studio agency default: client-logo strips, stats/metrics bars, numbered "our process" sections, and "book a call now" urgency. A solo developer with no client roster has no honest way to back those signals up, so this system replaces manufactured trust with inspectable proof — real screenshots, real feature detail, and a light, paper-white ground that never has to hide behind mood lighting.

**Key Characteristics:**
- Light, paper-and-ink ground — never dark, never a gradient hero
- Monospace display type for every headline — the subject's own material
- Three accents, each traceable to a literal pixel in a real shipped app
- Soft, ambient-only shadows; no hard drop shadows, no glassmorphism
- Calm, singular CTA — no urgency language, no repeated mid-scroll asks

## 2. Colors

The palette reads as quiet and neutral until an accent is needed — restrained, not colorful for its own sake.

### Primary
- **Pitch Green** (#2C864D): pulled directly from Vicki the Manager's real in-app primary color. Used for the single primary CTA and small accent marks — the site's rarest, most deliberate color.

### Secondary
- **Arcade Cyan** (#16B4D6): Pop Shot's real player-jet color, deepened from its in-game value so it holds contrast on a white ground. Used across the Pop Shot showcase and as a secondary interactive accent.

### Tertiary
- **Signal Coral** (#E8465F): Pop Shot's real "pop" energy color, deepened the same way. Reserved for sparing emphasis inside the Pop Shot illustration — never used for body text at small sizes.

### Neutral
- **Paper** (#F6F7FA): the page ground — a soft gray-blue, not stark white, matching Vicki the Manager's own screen background so the marketing page and the real product feel like one family.
- **Surface** (#FFFFFF): card and component ground, floating just above Paper.
- **Line** (#E1E5EE): hairline borders and dividers only.
- **Ink** (#14181F): primary text — a cool near-black, never pure `#000`.
- **Ink Dim** (#4C5468): body copy and secondary text.
- **Ink Faint** (#626C83): eyebrows, captions, placeholder-level text.

### Named Rules
**The Real Color Rule.** Every accent traces to a pixel that actually exists in one of the two real apps. Pitch Green is Vicki the Manager's literal primary; Arcade Cyan and Signal Coral are Pop Shot's literal jet and bubble colors. No color is chosen for generic connotation ("blue for trust," "green for eco") — if a new accent is ever needed, it must come from a real product, not a mood board.

**The One-CTA Rule.** Primary Green appears on exactly one interactive element per viewport at a time. It is never used as a background fill or a large surface color.

**Accessibility note.** Pitch Green and Ink Faint were each darkened a few percent in lightness from their first-pass values (originally #2F8F52 and #8891A6) after a contrast audit found white-on-green (4.06:1) and Ink Faint on Paper (2.95:1) both failed WCAG AA's 4.5:1 threshold for the small text they're used on. The adjustment preserves the same hue/saturation — same named color, same source pixel family — just enough darker to pass.

## 3. Typography

**Display Font:** Cascadia Mono (with SFMono-Regular, Consolas, monospace fallback)
**Body Font:** Segoe UI (with -apple-system, system sans-serif fallback)
**Label/Mono Font:** same family as Display, set smaller and looser

**Character:** monospace-as-display is a deliberate break from the humanist-grotesk look every competitor small-studio site converges on. The subject is software, so its own material — a fixed-width code face — carries the headlines; the body face stays a plain, comfortable system sans so paragraphs stay easy to read.

### Hierarchy
- **Display** (700, `clamp(2rem, 5vw, 3.7rem)`, 1.08 line-height): the hero headline only, tight negative tracking (-0.01em).
- **Headline** (700, `clamp(1.6rem, 3vw, 2.3rem)`, 1.15): section-level headlines ("Also builds for the web.", "Have something in mind?").
- **Title** (700, `clamp(1.4rem, 2.4vw, 1.95rem)`, 1.2): feature-row and assembly-caption headlines ("Set up in one screen.", "Stick three, they pop.").
- **Body** (400, 1.05rem, 1.6 line-height): paragraph copy; capped near 46–52ch for readability.
- **Label** (500, 0.72–0.8rem, 1.4 line-height, 0.12em tracking, uppercase): eyebrows, chip/tag text, nav wordmark.

### Named Rules
**The Code-Face Rule.** Anything the visitor is meant to remember (headlines, captions, tags) is set in the monospace display family. Anything the visitor is meant to read at length (paragraphs) is set in the body sans. Never mix the two roles.

## 4. Elevation

The system is flat by default; shadows appear only on the handful of elements that are meant to visually float above the page — the phone-stage mockups, cards, and the primary button. No hard drop shadows anywhere, no glassmorphism, no inner glows.

### Shadow Vocabulary
- **Ambient card** (`box-shadow: 0 14px 32px -18px rgba(20,24,31,0.18)`): feature-row visual cards.
- **Ambient piece** (`box-shadow: 0 6px 16px -8px rgba(20,24,31,0.28)`): individual screenshot fragments inside a phone-stage mockup.
- **Ambient device** (`filter: drop-shadow(0 24px 46px rgba(20,24,31,0.18))`): the phone-bezel stage frames.
- **Ambient CTA** (`box-shadow: 0 10px 24px -10px rgba(47,143,82,0.55)`): the primary button, using the primary color's own hue so the glow reads as "this button," not generic depth.

### Named Rules
**The Ambient-Only Rule.** Shadows are always soft, low-opacity, and colored toward what they're shadowing (neutral ink for cards, primary green for the CTA). They exist to lift an element off the page, never to fake depth on a flat section.

## 5. Components

Buttons, chips, and cards share one shape language: gently rounded corners, hairline borders on anything not filled, and a small upward lift on hover rather than a color-only change.

### Buttons
- **Shape:** gently rounded, 10px radius (`{rounded.sm}`).
- **Primary:** Pitch Green fill (#2C864D), white text, 14px/26px padding, ambient CTA shadow.
- **Hover / Focus:** lifts 2px, background deepens to #216C3C, shadow grows slightly. Focus-visible gets a 2px Pitch Green outline, 3px offset.
- **Ghost (secondary):** white fill, 1px Line border, Ink Dim text; hover darkens text to Ink and border to Ink Faint.

### Chips (tags)
- **Style:** white background, 1px Line border, pill radius (999px), Label typography, Ink Dim text.
- **State:** hover border turns Pitch Green, text turns Ink, small upward lift.

### Cards / Containers
- **Corner Style:** 16px radius for feature-visual cards; 12px for stacked screenshot pieces inside a phone stage.
- **Background:** Surface (#FFFFFF) on Paper (#F6F7FA).
- **Shadow Strategy:** Ambient card / Ambient piece per the Elevation section — never a border-and-shadow combo, pick one per component.
- **Border:** 1px Line, only on cards that don't already carry a shadow (feature-visual cards use both a hairline border and a soft shadow, deliberately, since they sit directly on Paper with low contrast otherwise).

### Navigation
- **Style:** fixed top bar, transparent over the hero, gaining a blurred Paper background (`rgba(246,247,250,0.86)` + `backdrop-filter: blur(14px)`) and a 1px Line bottom border once scrolled.
- **Typography:** Label face for the wordmark (700 weight, small green dot marker) and for the single "Contact" link, styled as a pill-bordered chip.
- **States:** the Contact link's border turns Pitch Green on hover; no active/pressed state needed since it's a same-page anchor.
- **Mobile treatment:** wordmark drops to a smaller Label size below 840px; horizontal padding tightens.

### Phone-Stage Mockup (signature component)
A recurring device frame — a CSS-drawn phone bezel (rounded rect, dark Ink stroke, small notch) wrapping either real cropped screenshots (Vicki the Manager) or original SVG illustration (Pop Shot). Pieces sit at their natural rest position at all times (never invisible) and only slide/settle a short distance as the page scrolls — see PRODUCT.md's accessibility note: this must degrade to a static, fully-assembled view under `prefers-reduced-motion`.

## 6. Do's and Don'ts

### Do:
- **Do** trace every accent color to a real pixel from one of the two real apps — Pitch Green, Arcade Cyan, and Signal Coral are not free choices.
- **Do** keep Primary Green rare: one CTA, small marks, never a large fill or background.
- **Do** set every headline and label in the monospace display family; never fall back to a generic humanist sans for hero type.
- **Do** keep phone-stage pieces visible at rest (opacity 1) at all times — only position/rotation animate, so the mockup can never render as a blank device.
- **Do** respect `prefers-reduced-motion` by showing the fully-assembled, static layout immediately, per PRODUCT.md's accessibility requirement.

### Don't:
- **Don't** add client-logo strips, stats/metrics bars, numbered "our process" sections, or "book a call now" urgency CTAs — PRODUCT.md names these directly as anti-references.
- **Don't** use a dark theme or a gradient-blob hero.
- **Don't** add decorative numbered markers (01/02/03). The only sequence labels in this system are the apps' own real workflow order — Setup → Squad → Live → History, Aim → Pop → Progress — never an invented sequence.
- **Don't** use stock "team high-fiving" or generic handshake/laptop photography.
- **Don't** use Inter, Poppins, or Montserrat as the display face — the monospace-as-display choice is deliberate and should not drift back to a generic startup grotesk.
- **Don't** stack a border and a heavy shadow on the same element without reason (see Cards: only feature-visual cards get both, and only because they sit on low-contrast Paper).
