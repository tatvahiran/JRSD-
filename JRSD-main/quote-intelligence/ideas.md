# Quote Intelligence — Design Direction

## Approach options

### Theme Name: Deep Current Glass
Very dark teal glassmorphism with luminous cyan accents, soft bloom, and a calm operational feel inspired by the provided reference image. The interface feels like a precision instrument: quiet, focused, and data-first.
**Probability:** 0.07

### Theme Name: Paper Ledger Modernism
A warm editorial procurement workspace using cream paper tones, ink-dark type, and restrained orange markers to make quote history feel like a carefully maintained physical ledger.
**Probability:** 0.03

### Theme Name: Mineral Utility
A cool graphite interface with mineral blue, eucalyptus, and amber status colors, using tactile panels and strong typographic hierarchy for a pragmatic operations console.
**Probability:** 0.08

## Chosen approach: Deep Current Glass

### Design Movement
Contemporary glassmorphism fused with dark-mode enterprise operations UI. The provided visual reference is the ground truth for the navigation treatment: a floating, translucent, pill-shaped control with soft inner light and luminous teal atmosphere.

### Core Principles
1. **Calm precision:** Dense procurement data is organized into quiet, legible surfaces with strong hierarchy rather than visual noise.
2. **Layered depth:** Frosted panels, edge highlights, subtle blur, and atmospheric glow distinguish navigation, content, and detail states.
3. **Selective luminosity:** Cyan and sea-glass accents are reserved for active states, key metrics, and actionable controls.
4. **Operational clarity:** Every interaction must make quote recency, price comparison, and supplier history immediately understandable.

### Color Philosophy
The base is near-black blue-green rather than pure black, creating a deep-water environment that feels premium but less harsh. A signature electric teal provides orientation and momentum, while muted blue-grey glass surfaces keep the content readable. Green confirms freshness or favorable price signals; amber is reserved for missing or attention-needed information. Bright text is cool white, not stark white, to maintain the atmospheric quality of the reference.

### Layout Paradigm
Use a persistent left-side rail with the reference-inspired floating pill navigation near the top. The main content is an asymmetric operational canvas: a spacious page header and KPI strip lead into a dominant data surface, with secondary context cards offset to the side where the viewport allows. Forms use a two-column rhythm on desktop and collapse into a single flow on smaller screens. Avoid a generic centered marketing layout.

### Signature Elements
1. **Floating glass navigation pill:** The three primary tabs use a compact vertical rail on desktop and a horizontal floating pill on smaller screens, with an active inset capsule and icon-led labels.
2. **Teal bloom:** A restrained cyan radial glow anchors the top navigation and active selection, echoing the reference without overwhelming the data.
3. **Quote signal chips:** Price, recency, hazmat, documentation, and lead-time statuses use compact luminous chips with consistent semantics.

### Interaction Philosophy
Interactions should feel like operating a precision console. Hover states brighten the glass edge; active states settle into an inset capsule; expanding quote histories should feel immediate and controlled. Destructive actions require confirmation. Keyboard focus is visible as a teal ring. Motion is short, smooth, and purposeful, never decorative enough to slow repeated quote entry.

### Animation
Use 160–220ms ease-out transitions for hover, active, tab, and chip changes. Expandable histories fade and translate upward by a few pixels rather than changing layout abruptly. Toasts enter from the lower-right with a small opacity/translate transition. The first-load ambient glow may gently drift, but all non-essential motion must be disabled for `prefers-reduced-motion`.

### Typography System
Use **Space Grotesk** for headings, navigation labels, and numeric metrics, paired with **DM Sans** for form labels, table content, and explanatory text. Headings use tight tracking and medium-to-bold weight. Body text uses a relaxed line-height for specifications and remarks. Monospace is reserved for Sr. No. and compact internal identifiers.

### Brand Essence
**Quote Intelligence is a calm command center for procurement teams who need to compare supplier pricing and preserve quote history without losing context.**

Personality adjectives: **precise, composed, discerning**.

### Brand Voice
Headlines should be concise and operational, never salesy. CTAs should describe the next action directly. Microcopy should explain state and recency in plain language.

Example headline: “See the market clearly.”

Example CTA: “Save quotation”.

### Wordmark & Logo
Use a custom abstract mark built from three nested angled quotation brackets forming a subtle Q shape, rendered as a simple luminous line icon. Pair it with the “Quote Intelligence” wordmark in Space Grotesk with a slightly tightened tracking treatment. The mark should work independently as the favicon and rail emblem.

### Signature Brand Color
**Deep Current Teal — #48D9D2.** It is bright enough to own the interface, but softened toward sea-glass rather than neon so the brand feels intelligent and composed.

## Style Decisions

- The provided reference image establishes the navigation language: translucent capsule, rounded glass edges, luminous cyan atmosphere, and icon-first controls.
- The app is an internal operational tool, so the content canvas prioritizes scanability and keyboard-friendly data entry over decorative hero content.
- The implementation uses browser persistence and keeps every quote as an immutable historical record unless the user explicitly edits or deletes it.
