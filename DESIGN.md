---
name: Imperial Street Auto Repair
description: Neighbourhood auto repair landing page — converts local search into phone calls and walk-in visits
colors:
  ink: "#0a1736"
  ink-mid: "#142348"
  ink-deep: "#2a3768"
  accent: "#1f53d6"
  accent-deep: "#143ea7"
  accent-light: "#5d8df7"
  surface: "#c2d6f5"
  surface-2: "#adc6f0"
  surface-3: "#95b3e8"
  muted: "#5a6385"
  muted-light: "#8a93b3"
  near-black: "#050608"
  ink-footer: "#06102b"
  ink-active: "#1a3a8f"
  white: "#ffffff"
  black: "#000000"
  specials: "#c82020"
  specials-deep: "#b01a1a"
  specials-darker: "#a01616"
  specials-text: "#ffb4a8"
  specials-light: "rgba(255,160,160,0.9)"
  status-open: "#4adf86"
  status-closed: "#ff6666"
  star: "#e6a521"
  section-4: "#9bbae8"
typography:
  display:
    fontFamily: "'Big Shoulders Display', 'Arial Narrow', sans-serif"
    fontSize: "clamp(36px, 6vw, 80px)"
    fontWeight: 800
    lineHeight: 0.92
    letterSpacing: "-0.01em"
    textWrap: "balance"
  headline:
    fontFamily: "'Big Shoulders Display', 'Arial Narrow', sans-serif"
    fontSize: "clamp(56px, 9vw, 96px)"
    fontWeight: 800
    lineHeight: 0.88
    letterSpacing: "-0.02em"
    textWrap: "balance"
  title:
    fontFamily: "'Manrope', 'Helvetica Neue', sans-serif"
    fontSize: "22px"
    fontWeight: 700
    lineHeight: 1.25
    letterSpacing: "-0.005em"
  body:
    fontFamily: "'Manrope', 'Helvetica Neue', sans-serif"
    fontSize: "16px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "'JetBrains Mono', ui-monospace, monospace"
    fontSize: "11px"
    fontWeight: 500
    letterSpacing: "0.22em"
rounded:
  sharp: "2px"
  sm: "3px"
  md: "4px"
  lg: "10px"
  xl: "12px"
  pill: "999px"
spacing:
  xs: "8px"
  sm: "14px"
  md: "22px"
  lg: "32px"
  xl: "40px"
  section: "clamp(72px, 9vw, 128px)"
  container: "min(1240px, calc(100% - 40px))"
components:
  button-primary:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.surface}"
    rounded: "{rounded.sharp}"
    padding: "0 22px"
    height: "52px"
  button-primary-hover:
    backgroundColor: "{colors.accent}"
    textColor: "#ffffff"
    rounded: "{rounded.sharp}"
    padding: "0 22px"
    height: "52px"
  button-ghost:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.sharp}"
    padding: "0 22px"
    height: "52px"
  button-on-dark:
    backgroundColor: "{colors.accent}"
    textColor: "#ffffff"
    rounded: "{rounded.sharp}"
    padding: "0 22px"
    height: "52px"
  button-on-dark-hover:
    backgroundColor: "#ffffff"
    textColor: "{colors.ink}"
    rounded: "{rounded.sharp}"
  pricing-card:
    backgroundColor: "rgba(255,255,255,.05)"
    textColor: "#ffffff"
    rounded: "{rounded.lg}"
    padding: "24px 20px"
---

# Design System: Imperial Street Auto Repair

## 1. Overview

**Creative North Star: "The Mechanic's Reference"**

Imperial Street Auto Repair's visual language is drawn from the aesthetic of a professional service manual — the kind of Bosch or Haynes technical reference that mechanics actually use. Compressed industrial type, structured information hierarchies, and a palette that says "we have been doing this for fifteen years and we know what we are doing." The design is confident without showmanship, precise without coldness.

The palette is a committed range of steel-blue tones stepped across sections — not a neutral background colour but the brand's own atmospheric hue. Deep corporate navy anchors structural elements. Electric blue fires as the sole accent: call-to-action buttons, kicker lines, the glow on active states. Mono type appears on labels, phone numbers, and data — not as a developer aesthetic but as precision-instrument reading, like the markings on a diagnostic gauge.

This system explicitly rejects the franchise auto-chain aesthetic (Jiffy Lube's red-and-white corporate sameness), the greasy-garage cliché (clip-art wrenches, racing flags), and the cold SaaS dark-dashboard look. It also rejects the cream/warm-neutral landing-page default: the background is blue, not beige. "Warmth" comes from the industrial type personality and the directness of the copy, not from the background colour.

**Key Characteristics:**
- Industrial compressed display type (Big Shoulders Display) — uppercase, tight leading, significant negative letter-spacing
- Steel-blue tonal sections stepping through a single hue family to create section rhythm without changing the palette
- Electric blue as the one accent colour: rare and purposeful, never decorative
- Mono type for all data-adjacent labels: kickers, phone numbers, timestamps, navigation counters
- Near-square button corners (2px radius) matching the architectural, no-nonsense personality
- Glassmorphic nav: the one justified use of blur in the system — it separates structure from content without an opaque band

## 2. Colors: The Steel-Blue Palette

A full-palette strategy built on a single hue family. Navy anchors structure; stepped blue tones surface sections; electric blue fires on the one action.

### Primary
- **Electric Blue** (`#1f53d6`): The sole accent. Used on CTAs, kicker lines, active state borders, the marquee strip background, section-number markers, and the FAQ open-state indicator. Never decorative; always structural or action-triggering.
- **Accent Deep** (`#143ea7`): Hover state and pressed state for the electric blue accent. Button hover, link hover.
- **Accent Light** (`#5d8df7`): The on-dark version of the accent — used over the deep navy where the full electric blue would be too heavy. Appears in `--brass` contexts (visit section contact info, dark-surface highlights).

### Secondary
- **Surface Blue** (`#c2d6f5`): The body background and the default section background. Not cream, not grey — the brand's own steel blue. Light enough to read dark ink clearly, saturated enough to identify immediately as this brand.
- **Surface Blue 2** (`#adc6f0`): Alternate section background — services section gradients, step 2 in the section rhythm.
- **Surface Blue 3** (`#95b3e8`): Deeper alternate — review section, creates contrast steps across the page.

### Tertiary
- **Section Blues** (`#a8c2ee`, `#bdd3f7`, `#c8daf8`, `#b0c8f2`, `#9bbae8`): The tonal section rhythm. Each section of the page uses one step in this ramp to create visual separation without a palette change. These are not random; they follow a lightness-stepping logic that gives the scroll a sense of atmospheric depth.

### Neutral
- **Deep Navy** (`#0a1736`): Primary structural colour. Dark section backgrounds, button fill, service column headers, footer overlay. The ink the whole system writes in.
- **Navy Mid** (`#142348`): Secondary structural surface — pricing cards dark bg, visit section dark panel.
- **Navy Deep** (`#2a3768`): Tertiary structural — nav dark variant, deep layers.
- **Muted** (`#5a6385`): Secondary body text, card descriptions, FAQ answers. Mid-navy-blue that reads clearly on the steel-blue backgrounds.
- **Muted Light** (`#8a93b3`): Tertiary text, disabled-like contexts, subdued metadata.
- **Near-Black** (`#050608`): Footer background only. Darker than the navy to clearly close the page.

### Named Rules
**The One Accent Rule.** Electric blue (`#1f53d6`) appears on ≤15% of any given section's surface. Its rarity creates the hierarchy. When everything is blue, nothing is.

**The Tonal Rhythm Rule.** Section backgrounds step through the steel-blue ramp, not alternate between unrelated hues. Every background colour on the page is a tint of the same family. New sections must use a value from the ramp, never an outside hue.

**The On-Dark Swap Rule.** On navy backgrounds, accent becomes `--brass` (`#5d8df7`), not the full electric blue. Full electric blue on navy lacks sufficient contrast; the lighter value reads clearly and still feels active.

## 3. Typography: Industrial Compressed

**Display Font:** Big Shoulders Display (Google Fonts, weights 600–900)
**Body Font:** Manrope (Google Fonts, weights 400–800)
**Label/Mono Font:** JetBrains Mono (Google Fonts, weights 500–700)

**Character:** Big Shoulders Display is a Chicago-industrial compressed sans — the font of transit signage and workshop inventory labels. It pairs with Manrope's humanist warmth to avoid reading cold. JetBrains Mono appears on all precision-data contexts: phone numbers, kicker lines, timestamps, navigation labels. The three families speak three registers: commanding, approachable, precise.

### Hierarchy
- **Hero Display** (800, `clamp(56px, 9vw, 132px)`, lh 0.88, ls -0.02em, uppercase): Page title only. Intentionally oversized at large viewports — the industrial oversized-headline tradition. Text-transform uppercase always.
- **Display / H2** (800, `clamp(40px, 6vw, 84px)`, lh 0.92, ls -0.01em, uppercase): Section headings. Same compressed family, same uppercase rule. Tight leading makes it a structural band, not a sentence.
- **Title / H3** (700, 22px, lh 1.25, ls -0.005em): Card headings, component titles, sub-section names. Uses Manrope, not Big Shoulders — this is readable prose hierarchy, not industrial signage.
- **Body** (400–500, 16px, lh 1.55): All running copy. Manrope at comfortable weight. Max line length 65–75ch on content areas.
- **Label / Eyebrow** (500–700, 11px, ls 0.22em, uppercase, JetBrains Mono): Kicker lines, category markers, technical metadata. The mono precision register. Used sparingly — one per section maximum, not as scaffolding on every heading.
- **Data / Price** (800–900, 22–56px, Big Shoulders Display): Pricing figures, trust stats. Number weight in the display family — the "amount" reads like a stamp.

### Named Rules
**The Uppercase Ceiling Rule.** Big Shoulders Display appears uppercase only. It is a display face, not a body face. Sentences in Big Shoulders at normal weight and mixed case lose their industrial character and read as a wrong font choice.

**The Mono Precision Rule.** JetBrains Mono earns its place by context, not decoration. Use it for: phone numbers, technical kicker labels, category counters, timestamp metadata. Do not use it for body copy, navigation links, or headings — that is "technical cosplay" and explicitly prohibited.

## 4. Elevation

The system uses a minimal shadow vocabulary — structure is created primarily through background colour steps, not layered shadows. Flat by default; shadows appear only as functional signals of interactivity or floating layer status.

### Shadow Vocabulary
- **Subtle rule** (`0 1px 0 rgba(13,14,16,.06), 0 1px 2px rgba(13,14,16,.04)`): Ambient separation. Applied to elements that need to read above their background without announcing themselves.
- **Card lift** (`0 18px 40px -20px rgba(13,14,16,.28)`): Hover or floating card state. Appears only on hover — cards are flat at rest.
- **Table structural** (`0 30px 80px -50px rgba(10,23,54,.25)`): The services table — a structural shadow that roots the full-width grid. One use only.
- **Nav scrolled** (`0 1px 0 rgba(10,23,54,.08), 0 8px 28px rgba(0,0,0,.10)`): The sticky nav acquires this shadow only after scroll begins. Before scroll, no shadow; the glassmorphic blur is the separator.

### Named Rules
**The Flat-By-Default Rule.** Cards and pricing panels are flat at rest. The shadow appears only on `:hover` with a `translateY(-2px)` micro-lift. A resting shadow reads as the whole page floating; that is not the intent.

**The Tonal-First Rule.** Before reaching for a shadow to create separation, reach for a background colour step. The section rhythm exists so that borders and shadows are not needed between sections. The services table's white-on-blue-background contrast already separates it; the structural shadow is a reinforcement, not the separator.

## 5. Components

### Buttons
Sharp-cornered (2px radius), industrial. The button shape matches the display typography's compressed, architectural personality. No rounded corners here — 10px radius on a navy button would look lifted from a SaaS app.

- **Shape:** Near-square (2px radius)
- **Primary (light surface):** Navy fill (`#0a1736`), cornflower text (`#c2d6f5`), 52px tall, 0 22px padding. Letter-spacing 0.04em, uppercase, 14px Manrope 700.
- **Hover:** Background shifts to electric blue (`#1f53d6`), border-color matches. `translateY(-1px)` micro-lift. Transition 0.18s ease.
- **Ghost (light surface):** Transparent fill, navy border, navy text. Hover fills to navy.
- **On-dark primary:** Electric blue fill, white text. Hover inverts to white fill, navy text.
- **On-dark ghost:** Transparent, rgba(255,255,255,.32) border, light text. Hover fills to `--paper`.
- **Arrow icon:** 14px SVG, animates `translateX(3px)` on hover. Arrow only on primary CTA buttons.

### Navigation
Sticky glassmorphic header. The blur is functional: the sticky position means content scrolls under it, and the translucent treatment shows movement without an opaque band breaking the visual continuity.

- **Default:** `rgba(245,247,252,0.72)` background, `blur(20px) saturate(160%)` backdrop-filter, `rgba(10,23,54,.08)` bottom border.
- **Scrolled:** Background shifts to `rgba(240,244,252,0.92)`, acquires nav-scrolled shadow.
- **Logo:** 72px tall, natural colours on the light nav background.
- **Links:** 14px Manrope 600, `rgba(10,23,54,.78)` default. Hover to full ink with 2px electric-blue underline (scaleX from 0).
- **Mobile ≤1080px:** Hamburger (44px × 44px, 2px radius border, animated 3-bar → X), nav links become absolute dropdown on `body.menu-open`.

### Pricing Cards (pcat)
Floating panels within the dark pricing section. Semi-transparent fill to let the navy background breathe through.

- **Corner Style:** 10px radius
- **Default Background:** `rgba(255,255,255,.05)`, border `rgba(255,255,255,.09)`
- **Hover:** Background to `.09`, border to `rgba(31,83,214,.45)`, `translateY(-2px)`. Transition 0.2s.
- **Header strip:** Deep navy fill `rgba(10,23,54 gradient)`, 2px bottom accent border. Big Shoulders Display 800 14px uppercase.
- **Price figures:** Big Shoulders Display 900 22px for standard prices, 26–28px for highlighted prices.
- **Specials variant:** Red-family header band (`#b01a1a → #c82020`), `rgba(140,18,18,.12)` background, animated glow pulse every 3.5s.
- **Internal Padding:** 24px 20px

### Service Sphere Tags
Pill-shaped floating labels in the 3D service sphere. Glassmorphic by necessity — they orbit on a transparent stage and need to read against the blue gradient background.

- **Style:** `border-radius: 999px`, white/80 background, subtle border, 700 weight body font, 6px 14px padding
- **Hover:** Background shifts to electric blue 88%, white text, stronger shadow
- **Active:** Full navy background, white text

### Trust Cells
The four-column stats strip on the dark navy band. No shadows, no borders — pure tonal separation within the navy background. Cells divided by `rgba(255,255,255,.08)` right borders.

### Eyebrow / Section Kicker
`.eyebrow` and `.section-num` — JetBrains Mono 11px, 0.22em tracking, uppercase. The `.eyebrow` leads with a 6px electric-blue dot; `.section-num` leads with a 24px horizontal rule in electric blue.

**These exist as a brand system, not reflexive scaffolding.** The system uses them; future additions should audit whether a given section genuinely needs a kicker or whether the h2 heading alone is sufficient.

### Linklike
Underline-style text link for body contexts: `border-bottom: 1px solid currentColor`, 0.04em tracking, uppercase, 14px JetBrains Mono 600. Hover shifts color to electric blue. Used for "in-text" CTAs, not navigation.

## 6. Do's and Don'ts

### Do:
- **Do** use Big Shoulders Display at 800+ weight, uppercase, with tight leading (0.88–0.92) for all h1 and h2 headings.
- **Do** use electric blue (`#1f53d6`) sparingly — on CTAs, kicker accents, and active states only. Its rarity creates the hierarchy.
- **Do** step through the steel-blue tonal ramp for section backgrounds. New sections must use a value from the `#9bbae8`–`#c2d6f5` family.
- **Do** use `border-radius: 2px` on buttons and sharp UI elements. The near-square corner is a deliberate personality choice for this industrial identity.
- **Do** use JetBrains Mono for precision-data contexts: kicker labels, phone numbers, pricing metadata, category counters.
- **Do** place the phone number `(604) 434-1120` within reach on every section — it is the primary conversion mechanism.
- **Do** keep body copy at a maximum of 65–75ch line length.
- **Do** ensure dark-section text (`rgba(255,255,255,.78)` or higher) maintains ≥4.5:1 contrast against the navy background.

### Don't:
- **Don't** use warm-neutral backgrounds (cream, sand, beige, paper). The body background is steel blue. "Warmth" comes from the typography and copy tone, not the background colour.
- **Don't** make the site look like a franchise chain (Jiffy Lube, Midas). That means: no red/white corporate palette, no template-feel card grids, no stock imagery of strangers in uniform.
- **Don't** use the greasy-garage aesthetic — clip-art wrenches, racing stripes, checkered flags. This shop is professional, not a caricature.
- **Don't** drift into SaaS/startup territory — gradient hero backgrounds with floating blobs, big-number metric strips, "glassmorphism everywhere" decoration. The one glassmorphic element in the system is the nav, and it is justified by the sticky-layer context.
- **Don't** use JetBrains Mono for navigation links, headings, or body paragraphs. It is the precision-data register, not the brand voice.
- **Don't** add rounded corners larger than 10px to structural containers. 20px+ radius on a button or header reads as a consumer app, not a neighbourhood workshop.
- **Don't** introduce an eyebrow/kicker label above every new section heading by reflex. The `.section-num` and `.eyebrow` patterns exist; use them only when the section genuinely needs orientation context, not as automatic scaffolding.
- **Don't** use side-stripe borders (`border-left` > 1px as a colour accent) on cards, alerts, or callouts. Use full borders, background tints, or no border at all.
- **Don't** use gradient text (`background-clip: text`). All text is solid colour.
- **Don't** add a second accent colour. This is a full-palette system built on one hue family; a second accent hue (orange, green, teal) breaks the identity.
