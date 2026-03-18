# MASTER WEB DESIGN SKILL — v1.0
## The Complete Reference for Building Production-Grade Websites

> **Read this entire file before writing a single line of code.**  
> Every section is active. Rules labeled HARD/NEVER/MUST are non-negotiable.  
> Everything else is a strong default — override only with explicit user intent.

---

## RULE PRIORITY ORDER

When rules conflict, resolve in this order:
1. **Real product feel** — ship-ready, not a demo or prototype
2. **Clarity + usability** — all interaction states wired, nothing dead
3. **Correctness** — no dead UI, no console errors, no broken state
4. **Theme consistency** — tokenized palette; no one-off hex values
5. **Features last** — do less, do it right

---

## 0 — PRIME DIRECTIVE: HUMAN-GRADE DELIVERY

Before finalizing any page/component, run all four passes:

### PASS A — CRITIC ("Kill AI Smell")
- Remove: artificial glows, heavy drop shadows on content, gratuitous card borders, neon gradients, generic hero+features+CTA section stacks.
- Kill **card soup**: if a view has more than ~6 panel cards simultaneously, you have failed. Replace with whitespace, dividers, and typography.
- Kill decorative icons that add no meaning.
- Remove anything that looks like a Figma community template or ThemeForest theme.
- NEVER use: Inter, Roboto, Arial, or system-ui as your primary design font. These are invisible defaults — invisible = forgettable.
- NEVER use: purple gradients on white, generic blue CTAs, cookie-cutter hero layouts.

### PASS B — FUNCTIONAL QA ("No Dead UI")
- Every clickable element MUST do something visible.
- Nav items must route somewhere real or be removed.
- Filters, toggles, modals, drawers, carousels, form validation, close behaviors — all must be wired.
- If something isn't implemented yet: remove it, hide it, or label it "Coming soon" — never leave a dead button.

### PASS C — ACCESSIBILITY + POLISH
- Keyboard-only pass: focus visible, logical tab order, ESC closes overlays, Enter activates buttons.
- `prefers-reduced-motion`: all non-essential animations must be suppressed.
- Contrast: body text meets AA (4.5:1), large text meets AA (3:1).
- Touch targets: minimum 24×24 CSS px; primary controls prefer ~44px on mobile.
- Semantic HTML: `nav`, `main`, `header`, `footer`, `section`, `article`, `aside`.
- ARIA only where native HTML is insufficient.
- Meaningful images have descriptive `alt` text; decorative images use `alt=""`.
- `<meta name="viewport" content="width=device-width, initial-scale=1">` is required.
- Skip-to-content link on content-heavy pages.

### PASS D — "No Box Check"
- Count visible rounded-rectangle panels in the viewport.
- If more than ~6: FAIL. Remove until below the threshold.
- Replace boxes with: spacing, hairline dividers, typography hierarchy.
- This pass is NEVER optional, even on portfolio or dark-mode sites.

---

## 1 — DESIGN THINKING PROCESS

Before coding, commit to a **BOLD aesthetic direction**:

1. **Purpose** — What problem does this interface solve? Who uses it?
2. **Tone** — Pick an extreme and commit. Options: brutally minimal, maximalist, retro-futuristic, organic/natural, luxury/refined, playful/toy-like, editorial/magazine, brutalist/raw, art deco/geometric, industrial/utilitarian, gothic, Y2K, Swiss International, etc.
3. **Differentiation** — What makes this UNFORGETTABLE? What is the one thing a user will remember?
4. **Archetype** — Match to one of the 28 archetypes in Section 3.

> **CRITICAL**: Maximalism and minimalism both work. The key is intentionality, not intensity. A bold serif on a flat black page can be more striking than a full-bleed gradient with particles.

---

## 2 — PAGE ARCHETYPES — COMMIT TO ONE

Pick exactly ONE archetype per page. Do not blend.

| Code | Archetype | Core Pattern |
|------|-----------|--------------|
| **A** | TOOL / DASHBOARD | Sidebar + list/table + detail panel |
| **B** | CATALOG / STORE / MEDIA | Rails + grid/list + filters + detail |
| **C** | CONTENT / DOCS / NEWS | Readable column (680–820px) + optional aside |
| **D** | LANDING / MARKETING | Hero + single-purpose CTA only |
| **E** | PORTFOLIO / CREATIVE | Visual spectacle + scroll storytelling |
| **F** | SOCIAL / FEED | Infinite scroll + engagement controls |
| **G** | MESSAGING / CHAT | Sidebar list + live chat panel |
| **H** | AUTH / ONBOARDING | Linear multi-step form with progress |
| **I** | ANALYTICS / BI | Dense chart grid + filter controls |
| **J** | ADMIN / SETTINGS | Form-heavy with action confirmation |
| **K** | MUSIC / MEDIA PLAYER | Persistent bottom player + library view |
| **L** | VIDEO STREAMING | Dark carousel-first + immersive player |
| **M** | FORUM / COMMUNITY | Threaded lists + voting + reputation |
| **N** | WIKI / REFERENCE | Content-first + inline links + TOC |
| **O** | EDUCATION / LMS | Progress tree + video + quiz flow |
| **P** | TRAVEL / BOOKING | Search form + compare flow + checkout |
| **Q** | FOOD DELIVERY | Visual menu + location filter + checkout |
| **R** | FINANCE / BANKING | Balance overview + transaction list + trust cues |
| **S** | TRADING / MARKET | Dense data + real-time charts + order book |
| **T** | DEVELOPER PLATFORM | Docs + API console + code snippets |
| **U** | BLOG / CREATOR | Single column + author voice + comments |
| **V** | MAGAZINE / EDITORIAL | Full-bleed imagery + longform + pull quotes |
| **W** | NEWS / NEWSPAPER | Multi-column + dense headlines + section labels |
| **X** | APP MARKETPLACE | Search + card grid + rating + install CTA |
| **Y** | E-COMMERCE RETAIL | Product grid + filter sidebar + cart flow |
| **Z** | NOTES / WRITING APP | Distraction-free editor + notebook sidebar |
| **AA** | TASK / KANBAN | Drag-and-drop board + column stages |
| **AB** | CALENDAR | Grid date views + event creation + scheduling |

---

## 3 — ARCHETYPE REFERENCE SITES & DESIGN PRESETS

### Reference Sites per Archetype

**News/Newspaper**: NYTimes, Guardian, BBC News, Washington Post, Reuters  
**Magazine/Editorial**: The Atlantic, Wired, National Geographic, Vanity Fair, Vox  
**Documentation**: MDN Web Docs, Stripe API Docs, GitHub Docs, ReadTheDocs  
**Wiki/Reference**: Wikipedia, Britannica, IMDb, Investopedia, Stack Overflow  
**Blog/Creator**: Medium, Substack, Dev.to, Ghost  
**E-commerce**: Apple Store, Etsy, IKEA, Zara  
**Streaming Video**: Netflix, YouTube, Disney+, Twitch  
**Music Player**: Spotify, Apple Music, SoundCloud, Tidal  
**Email Client**: Gmail, Hey, ProtonMail, Superhuman  
**Chat/Messaging**: Slack, Discord, WhatsApp Web, Telegram  
**Social Feed**: Twitter/X, Instagram, Pinterest, LinkedIn  
**Analytics**: Mixpanel, Grafana, Amplitude, Datadog  
**Admin Console**: Shopify Admin, AWS Console, Google Cloud Console  
**Banking/Finance**: Revolut, N26, Monzo, Stripe Dashboard  
**Trading**: TradingView, Robinhood, Binance Pro  
**Travel**: Airbnb, Skyscanner, Google Travel  
**Food Delivery**: Deliveroo, Uber Eats, OpenTable  
**Education/LMS**: Duolingo, Khan Academy, Notion, Canvas  
**Developer Platform**: Stripe Dashboard+Docs, Vercel, Postman  
**Portfolio**: Behance, Dribbble, awwwards.com examples  
**Landing Page**: Stripe Homepage, Linear.app, Vercel, Notion  
**Auth/Onboarding**: Notion, Duolingo, Slack workspace setup

### Design Preset: News/Newspaper
- Layout: Multi-column desktop (primary + aside), single column mobile
- Typography: **Serif for headlines and body** (Merriweather, Libre Baskerville, or Playfair)
- Color: White background, near-black text, 1 accent (dark blue or red)
- Interaction: Hover underline on headlines; no card boxes — use whitespace + hairlines
- Motion: Near-zero. Subtle dropdown fade (150ms max)

### Design Preset: Documentation
- Layout: Left nav sidebar (collapsible on mobile) + content column ~720px max
- Typography: Clear **sans-serif body**, monospace for code (JetBrains Mono, Fira Code)
- Color: Light mode default; code blocks on soft gray; dark mode toggle required
- Components: Copy button on all code blocks; collapsible sections; sticky in-page TOC
- Motion: None except smooth anchor scrolling

### Design Preset: Landing Page
- Layout: Single page, sections scroll vertically. Hero is the first viewport.
- Typography: Bold display font for hero. One primary CTA above fold.
- Color: Strong dominant + 1 accent. White space is a feature, not an accident.
- Rules: One true primary CTA per section max. No nav items leading nowhere.
- Motion: Scroll-triggered reveals (opacity/translateY, 400ms ease-out). No auto-play.

### Design Preset: Dashboard/Analytics
- Layout: Fixed sidebar (collapsible) + main canvas. No floating card stacks.
- Typography: System-native or IBM Plex Sans. Dense but readable (13–14px for data).
- Color: Dark default (Family A or B below). Charts use distinct categorical palette.
- Components: Sticky table headers, right-aligned numbers, row hover fill.
- Motion: Skeleton loaders on data fetch. Chart draws on mount.

### Design Preset: Portfolio/Creative
- Layout: Full-viewport hero, scroll-driven sections, generous negative space OR controlled chaos.
- Typography: **Serif display + sans body** (Playfair/Cormorant + Work Sans/Manrope).
- Color: Family D (dark luxe) or bespoke. Accent color is the personality.
- Special: Unlocks animated backgrounds (see Section 9), custom cursor, parallax.
- Motion: GSAP scroll triggers, staggered reveals, mouse parallax.

### Design Preset: E-commerce
- Layout: Grid product listings with filter sidebar. Header: logo + search + cart.
- Typography: Clean sans-serif. Product names semi-bold. Prices bold.
- Color: White background, brand accent for CTAs. Red/strike for sale prices.
- Components: Product card (image + name + rating + price + quick-add). Sticky filter.
- Motion: Cart icon feedback on add. Image swap on color selection.

### Design Preset: Streaming/Video
- Layout: Dark background, horizontal carousels by category. Persistent player bar.
- Typography: White sans-serif on dark. Short text only — titles + metadata.
- Color: **Dark is default and primary.** Brand accent for active/selected states.
- Components: Hover preview on thumbnails. Progress bar on video player.
- Motion: Thumbnail scale on hover (150ms). Smooth carousel scroll.

---

## 4 — ANTI-BOX SYSTEM (THE CORE LOOK)

**Problem**: Boxes/cards everywhere = template/AI smell.  
**Solution**: Real products use whitespace, typography hierarchy, dividers, and rhythm.

### 4.1 Card Quota (HARD RULE)
If a view shows more than ~6 panel cards simultaneously: FAIL.

Cards are ONLY allowed for:
1. Clickable entity tiles (products, articles, project thumbnails)
2. Raised overlays (modals, menus, toasts)
3. Truly distinct "object" components (pricing table, promo unit)

### 4.2 Forbidden Box Traits (HARD)
DO NOT:
- Wrap every section in a rounded-rectangle background
- Stack multiple right-rail cards with shadows
- Add visible borders around every container
- Add glow shadows in dark mode
- Put a panel background behind long-form text

### 4.3 Replacements (Use These Instead)
Instead of a card, use:
- Section heading + hairline divider + unboxed content block
- Row list with hover fill (no outer border)
- Inset callout: left border line + very subtle tint (not a rounded card)
- Two-column layout with a thin vertical divider
- Sticky text-only aside separated by spacing, not a card stack
- Inline chips/tags (minimal — never chip soup)

### 4.4 Sidebar Rules (HARD)
Sidebar modules MUST be: heading + short list, separated by whitespace and a top divider.  
NO rounded rectangles. NO shadow. NO panel background.

### 4.5 What Top Sites Do Instead of Boxes
- **Whitespace as separator** — generous margins between items, no borders needed
- **Thin divider lines** — 1px hairlines for section separation, not frames
- **Grouping by headings** — section headers create visual groups without containers
- **Hover highlights** — backgrounds appear on interaction only, not permanently
- **Background shading sparingly** — only for truly special content (one element per page)
- **No heavy shadows** — shadows only on modals and dropdowns, never on content

---

## 5 — DESIGN TOKEN SYSTEM

**MANDATORY**: Use CSS custom properties for ALL colors, spacing, and typography. Never hardcode values in components.

### 5.1 Core CSS Token Scaffold

```css
:root {
  /* === SURFACES === */
  --bg:           ;   /* page background */
  --surface-1:    ;   /* nav, sidebar */
  --surface-2:    ;   /* menus, modals */
  --surface-3:    ;   /* popovers, tooltips */
  --stroke:       ;   /* borders/dividers */

  /* === TEXT === */
  --text:         ;   /* primary text */
  --muted:        ;   /* secondary text */
  --text-inverse: ;   /* text on accent backgrounds */

  /* === ACCENT === */
  --accent:       ;   /* primary CTA, active state, links */
  --accent-hover: ;   /* darken/lighten on hover */
  --accent-weak:  ;   /* accent at ~15% opacity for badges/backgrounds */

  /* === SEMANTIC === */
  --success:      oklch(65% 0.15 145);
  --warning:      oklch(75% 0.15 85);
  --danger:       oklch(60% 0.20 25);
  --info:         oklch(65% 0.15 230);

  /* === SPACING (8px base system) === */
  --sp-0:  0;
  --sp-1:  4px;
  --sp-2:  8px;
  --sp-3:  12px;
  --sp-4:  16px;
  --sp-5:  20px;
  --sp-6:  24px;
  --sp-8:  32px;
  --sp-10: 40px;
  --sp-12: 48px;
  --sp-16: 64px;
  --sp-20: 80px;
  --sp-24: 96px;

  /* === RADIUS === */
  --radius-xs:   2px;   /* badges, tags */
  --radius-sm:   4px;   /* buttons, inputs */
  --radius-md:   6px;   /* cards */
  --radius-lg:   8px;   /* large cards */
  --radius-xl:  12px;   /* modals, panels */
  --radius-full: 9999px; /* pills, avatars */

  /* === SHADOWS === */
  --shadow-sm:  0 1px 2px rgba(0,0,0,0.12);
  --shadow-md:  0 4px 12px rgba(0,0,0,0.15);
  --shadow-lg:  0 8px 32px rgba(0,0,0,0.20);
  --shadow-xl:  0 16px 48px rgba(0,0,0,0.25);
  /* Shadows on dark mode: cut all values in half or remove entirely */

  /* === TYPOGRAPHY === */
  --font-display: ;   /* heading/display font */
  --font-body:    ;   /* body copy */
  --font-mono:    ;   /* code */

  --text-xs:   clamp(0.75rem, 0.7rem + 0.2vw, 0.875rem);
  --text-sm:   clamp(0.875rem, 0.82rem + 0.25vw, 1rem);
  --text-base: clamp(1rem, 0.95rem + 0.25vw, 1.125rem);
  --text-lg:   clamp(1.125rem, 1.05rem + 0.35vw, 1.375rem);
  --text-xl:   clamp(1.25rem, 1.15rem + 0.4vw, 1.5rem);
  --text-2xl:  clamp(1.5rem, 1.35rem + 0.75vw, 2rem);
  --text-3xl:  clamp(1.875rem, 1.65rem + 0.9vw, 2.5rem);
  --text-4xl:  clamp(2.25rem, 1.95rem + 1.4vw, 3.5rem);
  --text-display: clamp(3rem, 2.4rem + 2.5vw, 4.5rem);

  /* === MOTION === */
  --duration-fast:   150ms;
  --duration-base:   220ms;
  --duration-slow:   350ms;
  --duration-slower: 500ms;
  --ease-out:    cubic-bezier(0.0, 0.0, 0.2, 1);
  --ease-in:     cubic-bezier(0.4, 0.0, 1, 1);
  --ease-inout:  cubic-bezier(0.4, 0.0, 0.2, 1);
  --ease-bounce: cubic-bezier(0.34, 1.56, 0.64, 1);

  /* === Z-INDEX LADDER === */
  --z-base:    0;
  --z-sticky:  10;
  --z-dropdown: 100;
  --z-tooltip:  200;
  --z-drawer:   300;
  --z-modal:    400;
  --z-toast:    500;
}
```

### 5.2 Semantic Color Slots (Light / Dark)

| Token | Light Mode | Dark Mode |
|-------|-----------|-----------|
| `--background` | `oklch(99% 0 0)` | `oklch(15% 0.01 250)` |
| `--surface` | `oklch(100% 0 0)` | `oklch(20% 0.015 250)` |
| `--text` | `oklch(20% 0.01 250)` | `oklch(95% 0.01 250)` |
| `--primary` | `oklch(55% 0.18 250)` | `oklch(65% 0.18 250)` |
| `--accent` | `oklch(55% 0.18 250)` | `oklch(65% 0.18 250)` |
| `--success` | `oklch(65% 0.15 145)` | `oklch(70% 0.15 145)` |
| `--danger` | `oklch(60% 0.20 25)` | `oklch(65% 0.20 25)` |

---

## 6 — COLOR FAMILIES (PICK ONE — DO NOT MIX)

### Family A — Cool Neutral (Apps, Tools, Dashboards)
```css
--bg:        #1e1f22;
--surface-1: #2b2d31;
--surface-2: #313338;
--hover:     #383a40;
--text:      #dbdee1;
--muted:     #b5bac1;
--stroke:    rgba(255,255,255,0.06);
/* Accent options: #5865f2 (indigo), #00b0f4 (blue), #57f287 (green) */
```

### Family B — Deep Dark (Content-Forward)
```css
--bg:        #0f0f0f;
--surface-1: #181818;
--surface-2: #212121;
--stroke:    #2a2a2a;
--text:      #ededed;
--muted:     #aaaaaa;
/* Accent options: #ff0000 (YouTube-red), #1db954 (Spotify-green), #ff6b35 (warm orange) */
```

### Family C — Warm Neutral (Cozy/Human/Community)
```css
--bg:        #2c2b29;
--surface-1: #343231;
--surface-2: #3c3a39;
--text:      #f0f0ee;
--muted:     #bcb8b0;
/* Accent: #c8a98a (warm tan), #7c9a92 (sage), #d4956a (terracotta) */
```

### Family D — Portfolio Dark Luxe (Creative Sites)
```css
--bg:        #0a0a0a;
--surface-1: #141414;
--surface-2: #1a1a1a;
--stroke:    rgba(255,255,255,0.08);
--text:      #e8e8e8;
--muted:     #a0a0a0;
--accent:    #d4a574;   /* warm gold */
--accent-weak: rgba(212,165,116,0.15);
/* Swap accent: #06b6d4 (ocean), #10b981 (forest), #f97316 (sunset), #a78bfa (violet) */
```

### Family E — Clean Light (Apps, Stores, Dashboards)
```css
--bg:        #f6f7f8;
--surface-1: #ffffff;
--surface-2: #f1f3f5;
--stroke:    rgba(10,12,16,0.10);
--text:      #0f1216;
--muted:     rgba(15,18,22,0.70);
--accent:    #1a73e8;
--accent-weak: rgba(26,115,232,0.16);
```

### Family F — Pure White Editorial (News, Docs, Blogs)
```css
--bg:        #ffffff;
--surface-1: #f8f8f8;
--surface-2: #f0f0f0;
--stroke:    #e8e8e8;
--text:      #1a1a1a;
--muted:     #666666;
--accent:    #1a1a9e;   /* deep blue — or brand red */
```

---

## 7 — TYPOGRAPHY PACKS (PICK ONE — DO NOT MIX FAMILIES)

### Pack A — System Native (Tools, Internal Apps)
```
UI:   system-ui / -apple-system / Segoe UI / Helvetica Neue / sans-serif
Code: ui-monospace / Menlo / Consolas / monospace
```

### Pack B — Dev Tool (Editors, CLIs, Consoles)
```
UI:   Geist, IBM Plex Sans, or Source Sans 3
Code: JetBrains Mono or IBM Plex Mono
Google Fonts: https://fonts.googleapis.com/css2?family=IBM+Plex+Sans:wght@400;500;600&family=JetBrains+Mono:wght@400;500&display=swap
```

### Pack C — Modern Grotesque (SaaS, Clean Products)
```
UI:   Manrope, Work Sans, or DM Sans
Accent/Display: Space Grotesk or Plus Jakarta Sans (headings only)
Google Fonts: https://fonts.googleapis.com/css2?family=Manrope:wght@400;500;600;700;800&display=swap
```

### Pack D — Warm/Cozy (Community, Lifestyle, Hobby)
```
UI:   Atkinson Hyperlegible, Nunito, or Noto Sans
Code: Fira Code (if needed)
```

### Pack E — Portfolio Editorial (Personal Sites, Creative)
```
Display: Playfair Display, Cormorant Garamond, or DM Serif Display
Body:    Work Sans, Manrope, or Plus Jakarta Sans
Google Fonts: https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,400&family=Work+Sans:wght@300;400;500;600&display=swap
```

### Pack F — News / Editorial (Publications, Magazines)
```
Body:    Merriweather, Libre Baskerville, or Lora (serif, screen-optimized)
UI:      Libre Franklin, Source Sans 3, or Barlow
Free analogue to NYT Cheltenham: Della Respira (Google Fonts)
Google Fonts: https://fonts.googleapis.com/css2?family=Merriweather:ital,wght@0,400;0,700;1,400&family=Libre+Franklin:wght@400;500;600&display=swap
```

### Pack G — Brutalist/Industrial (Bold Creative)
```
Display: Anton, Black Han Sans, or Bebas Neue (headline impact)
Body:    Barlow Condensed, Space Mono, or Source Code Pro
```

### Pack H — Luxury/High-Fashion
```
Display: Cormorant (ultra-light tracking), IM Fell English
Body:    Raleway Light or Jost Light
```

### Typography Rules
- Body: 14–16px, line-height 1.45–1.7 (content) or 1.3–1.45 (UI)
- Labels: 12–13px, weight 500–600
- UI headings: 18–28px
- Editorial/hero headings: 36–72px+
- NEVER all-caps except small data labels (e.g., "YRS EXP", "BETA")
- Use weight contrast: regular body → semibold headings → bold display
- `font-display: swap` on all web fonts
- Preload at most ONE primary font file

---

## 8 — COMPONENT BEHAVIOR (REAL APP FEEL)

### 8.1 Navigation
- Active states always visible
- Empty sections: provide empty state content, never blank pages
- Never show a nav item that leads to a blank or placeholder page

### 8.2 Buttons / Links
- Buttons = actions. Links = navigation. Never swap semantics.
- Icon-only buttons: `aria-label` + tooltip always.
- One true primary CTA per view maximum.
- States required: default, hover, active, focus, disabled, loading

### 8.3 Filters / Sorting
- Must update results statefully — no "apply" button unless complex multi-filter
- Provide "Clear all filters"
- Show result count and applied filter chips

### 8.4 Tables / Lists
- Row hover fill (no permanent borders)
- Selected state stronger than hover
- Secondary actions on hover only, not permanently visible
- Header row sticky when body scrolls
- Text: left-aligned. Numbers: right-aligned (tabular figures). Actions: right.
- Active sort clearly indicated (icon + direction)
- Truncate long cells with ellipsis + tooltip on hover

### 8.5 Modals / Drawers
- MUST: trap focus, close on ESC, visible close button, backdrop closes modal
- MUST NOT: overflow viewport
- Closed overlays: `display: none` or `inert` — never `opacity: 0` alone

### 8.6 Toasts / Notices
- Short, dismissible or auto-dismiss (3–5s)
- Respect `prefers-reduced-motion`
- Position: bottom-right or top-center — pick one and be consistent

### 8.7 Empty / Loading / Error States (ALL THREE REQUIRED)
- **Loading**: skeleton screen or labeled spinner
- **Empty**: one calm line of copy + one primary action
- **Error**: clear message + retry option

### 8.8 Forms
- Inline validation (not only on submit)
- Clear error states on individual fields
- Success confirmation after submission
- No placeholder text as the only label
- Logical tab order

### 8.9 Carousels / Rails
- NEVER auto-play. Arrow controls on desktop (keyboard-focusable).
- Show partial next item to hint scrollability.
- Dot or number indicators for finite carousels.

---

## 9 — ANIMATED BACKGROUNDS (THREE.JS SYSTEM)

Use animated backgrounds for: portfolios, creative sites, landing pages, hero sections.  
**Do NOT** use on dashboards, documentation, or content-heavy text pages.

### 9.1 HTML Structure
Place at the top of `<body>`:

```html
<!-- Optional: CSS texture layer (see patterns in 9.5) -->
<div id="bg-pattern"></div>

<!-- 3D canvas -->
<canvas id="bg-canvas"></canvas>

<!-- All page content -->
<div class="page-wrapper">...</div>
```

### 9.2 Base CSS
```css
#bg-pattern {
    position: fixed;
    inset: 0;
    z-index: 0;
    pointer-events: none;
}

#bg-canvas {
    position: fixed;
    inset: 0;
    width: 100%;
    height: 100%;
    z-index: 1;
    pointer-events: none; /* CRITICAL — never blocks page clicks */
}

.page-wrapper {
    position: relative;
    z-index: 2;
}
```

### 9.3 CDN Dependency
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
```

### 9.4 Complete three-bg.js Engine

```javascript
document.addEventListener('DOMContentLoaded', () => { initThreeBackground(); });

function initThreeBackground() {
    if (typeof THREE === 'undefined') return;
    if (window.matchMedia('(prefers-reduced-motion: reduce)').matches) return;

    const canvas = document.getElementById('bg-canvas');
    if (!canvas) return;

    // ============================================================
    // PASTE YOUR CHOSEN CONFIG HERE (see Section 9.6 for presets)
    // ============================================================
    const CONFIG = {
        colors:      [0xd4a574],
        shapeTypes:  ['torus', 'octahedron', 'icosahedron', 'tetrahedron'],
        shapeCount:  15,
        spread:      100,
        opacity:     0.15,
        cameraZ:     30,
        mouseFactor: 5,
        lerpFactor:  0.05,
        scrollDepth: 20,
        rotSpeed:    0.01,
        wireframe:   true
    };
    // ============================================================

    const scene  = new THREE.Scene();
    const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
    camera.position.setZ(CONFIG.cameraZ);

    const renderer = new THREE.WebGLRenderer({ canvas, alpha: true, antialias: true });
    renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
    renderer.setSize(window.innerWidth, window.innerHeight);

    // Shape geometry library
    const GEO = {
        torus:         () => new THREE.TorusGeometry(10, 3, 16, 100),
        octahedron:    () => new THREE.OctahedronGeometry(8),
        icosahedron:   () => new THREE.IcosahedronGeometry(7),
        tetrahedron:   () => new THREE.TetrahedronGeometry(8),
        cube:          () => new THREE.BoxGeometry(10, 10, 10),
        lowPolySphere: () => new THREE.SphereGeometry(8, 8, 6),
        cone:          () => new THREE.ConeGeometry(7, 14, 8),
        cylinder:      () => new THREE.CylinderGeometry(5, 5, 14, 8),
        flatRing:      () => new THREE.RingGeometry(5, 9, 6),
        dodecahedron:  () => new THREE.DodecahedronGeometry(7),
        torusKnot:     () => new THREE.TorusKnotGeometry(6, 1.5, 80, 10),
        pyramid:       () => new THREE.ConeGeometry(8, 10, 4),
        hexPrism:      () => new THREE.CylinderGeometry(7, 7, 10, 6),
        thinRing:      () => new THREE.TorusGeometry(9, 0.8, 8, 60),
    };

    const shapes = [];
    const isMobile = window.innerWidth < 768 || (navigator.hardwareConcurrency || 4) < 4;
    const count = isMobile ? Math.floor(CONFIG.shapeCount / 2) : CONFIG.shapeCount;

    function findOpenPosition(existing, spread, minDist = 18, maxTries = 30) {
        for (let i = 0; i < maxTries; i++) {
            const c = new THREE.Vector3(
                THREE.MathUtils.randFloatSpread(spread),
                THREE.MathUtils.randFloatSpread(spread),
                THREE.MathUtils.randFloatSpread(spread)
            );
            if (!existing.some(s => s.position.distanceTo(c) < minDist)) return c;
        }
        return null;
    }

    for (let i = 0; i < count; i++) {
        const type = CONFIG.shapeTypes[Math.floor(Math.random() * CONFIG.shapeTypes.length)];
        const color = CONFIG.colors[Math.floor(Math.random() * CONFIG.colors.length)];
        const geo = GEO[type]();
        const mat = new THREE.MeshStandardMaterial({
            color, wireframe: CONFIG.wireframe, transparent: true, opacity: CONFIG.opacity
        });
        const mesh = new THREE.Mesh(geo, mat);
        const pos = findOpenPosition(shapes, CONFIG.spread);
        if (!pos) continue;
        mesh.position.copy(pos);
        mesh.rotation.x = Math.random() * Math.PI;
        mesh.rotation.y = Math.random() * Math.PI;
        mesh.userData.rotSpeed = {
            x: (Math.random() - 0.5) * CONFIG.rotSpeed,
            y: (Math.random() - 0.5) * CONFIG.rotSpeed
        };
        mesh.userData.baseOpacity = CONFIG.opacity;
        scene.add(mesh);
        shapes.push(mesh);
    }

    scene.add(new THREE.PointLight(CONFIG.colors[0], 1.2, 0, 2));
    scene.add(new THREE.AmbientLight(0xffffff, 0.3));

    let mouseX = 0, mouseY = 0, targetX = 0, targetY = 0;
    document.addEventListener('mousemove', e => {
        mouseX = (e.clientX / window.innerWidth) * 2 - 1;
        mouseY = -(e.clientY / window.innerHeight) * 2 + 1;
    });

    window.addEventListener('scroll', () => {
        const t = window.pageYOffset / Math.max(1, document.documentElement.scrollHeight - window.innerHeight);
        camera.position.z = CONFIG.cameraZ + t * CONFIG.scrollDepth;
    });

    (function animate() {
        requestAnimationFrame(animate);
        targetX += (mouseX - targetX) * CONFIG.lerpFactor;
        targetY += (mouseY - targetY) * CONFIG.lerpFactor;
        camera.position.x = targetX * CONFIG.mouseFactor;
        camera.position.y = targetY * CONFIG.mouseFactor;
        camera.lookAt(scene.position);
        shapes.forEach(s => {
            s.rotation.x += s.userData.rotSpeed.x;
            s.rotation.y += s.userData.rotSpeed.y;
        });
        renderer.render(scene, camera);
    })();

    window.addEventListener('resize', () => {
        camera.aspect = window.innerWidth / window.innerHeight;
        camera.updateProjectionMatrix();
        renderer.setSize(window.innerWidth, window.innerHeight);
    });

    // Section pulse on scroll-into-view
    new IntersectionObserver(entries => {
        entries.forEach(e => {
            if (!e.isIntersecting) return;
            shapes.forEach((shape, i) => {
                setTimeout(() => {
                    let t = 0;
                    const base = shape.userData.baseOpacity;
                    const id = setInterval(() => {
                        t += 0.06;
                        shape.material.opacity = base + Math.sin(t * Math.PI) * (base * 0.6);
                        if (t >= 1) { clearInterval(id); shape.material.opacity = base; }
                    }, 16);
                }, i * 50);
            });
        });
    }, { threshold: 0.2 }).observe(document.body);

    // Public API for theme switching
    window.updateBgColors = hexArray => {
        shapes.forEach(s => s.material.color.setHex(hexArray[Math.floor(Math.random() * hexArray.length)]));
    };
}
```

### 9.5 Background Variation Configs (Paste into CONFIG)

**Variation A — Gold Classic** (dark luxury portfolios)
```javascript
const CONFIG = {
    colors: [0xd4a574],
    shapeTypes: ['torus','octahedron','icosahedron','tetrahedron','cube','dodecahedron','thinRing'],
    shapeCount: 15, spread: 100, opacity: 0.15, cameraZ: 30,
    mouseFactor: 5, lerpFactor: 0.05, scrollDepth: 20, rotSpeed: 0.01, wireframe: true
};
/* body { background: #0a0a0a; } */
```

**Variation B — Pearl White** (clean/editorial/minimal portfolios)
```javascript
const CONFIG = {
    colors: [0xf0ede8, 0xe8e4de, 0xd8d4ce],
    shapeTypes: ['icosahedron','dodecahedron','lowPolySphere','thinRing','flatRing','octahedron'],
    shapeCount: 12, spread: 110, opacity: 0.12, cameraZ: 30,
    mouseFactor: 4, lerpFactor: 0.04, scrollDepth: 15, rotSpeed: 0.007, wireframe: true
};
/* body { background: #0d0d0d; } */
```

**Variation C — Tri-Color Scatter** (layered depth, rich scene)
```javascript
const CONFIG = {
    colors: [0xd4a574, 0xf0ede8, 0x3a3632],
    shapeTypes: ['torus','cube','tetrahedron','icosahedron','octahedron','cone','thinRing','pyramid'],
    shapeCount: 20, spread: 120, opacity: 0.18, cameraZ: 35,
    mouseFactor: 6, lerpFactor: 0.05, scrollDepth: 25, rotSpeed: 0.012, wireframe: true
};
/* body { background: #080808; } */
```

**Variation D — Sparse/Architectural** (hero sections, big shapes)
```javascript
const CONFIG = {
    colors: [0xd4a574, 0xc49060],
    shapeTypes: ['torusKnot','icosahedron','thinRing','dodecahedron'],
    shapeCount: 6, spread: 80, opacity: 0.20, cameraZ: 25,
    mouseFactor: 8, lerpFactor: 0.03, scrollDepth: 30, rotSpeed: 0.005, wireframe: true
};
/* body { background: #0a0a0a; } */
```

**Variation E — Charcoal Grid** (technical/drafting aesthetic)
```javascript
const CONFIG = {
    colors: [0xd4a574, 0xe0b882],
    shapeTypes: ['cube','octahedron','tetrahedron','pyramid','hexPrism','cylinder'],
    shapeCount: 14, spread: 100, opacity: 0.18, cameraZ: 30,
    mouseFactor: 5, lerpFactor: 0.05, scrollDepth: 20, rotSpeed: 0.009, wireframe: true
};
/* body { background: #1a1917; }
   #bg-pattern {
     background-image:
       linear-gradient(rgba(212,165,116,0.05) 1px, transparent 1px),
       linear-gradient(90deg, rgba(212,165,116,0.05) 1px, transparent 1px);
     background-size: 40px 40px;
   } */
```

**Variation F — Dot Matrix** (organic/perforated aesthetic)
```javascript
const CONFIG = {
    colors: [0xf0ede8, 0xe0dcd6],
    shapeTypes: ['lowPolySphere','icosahedron','thinRing','flatRing','dodecahedron','torus'],
    shapeCount: 13, spread: 100, opacity: 0.13, cameraZ: 30,
    mouseFactor: 4.5, lerpFactor: 0.04, scrollDepth: 18, rotSpeed: 0.008, wireframe: true
};
/* body { background: #171717; }
   #bg-pattern {
     background-image: radial-gradient(circle, rgba(240,237,232,0.12) 1px, transparent 1px);
     background-size: 28px 28px;
   } */
```

**Variation G — Diagonal Hatch** (architectural/directional)
```javascript
const CONFIG = {
    colors: [0xd4a574, 0xf0ede8, 0xc49060],
    shapeTypes: ['cone','pyramid','tetrahedron','octahedron','cube','cylinder','thinRing'],
    shapeCount: 16, spread: 105, opacity: 0.16, cameraZ: 30,
    mouseFactor: 5, lerpFactor: 0.05, scrollDepth: 20, rotSpeed: 0.010, wireframe: true
};
/* body { background: #141412; }
   #bg-pattern {
     background-image: repeating-linear-gradient(
       45deg,
       rgba(212,165,116,0.04) 0px, rgba(212,165,116,0.04) 1px,
       transparent 1px, transparent 18px
     );
   } */
```

**Variation H — Solid Shadow** (mysterious/understated)
```javascript
const CONFIG = {
    colors: [0xd4a574, 0xb8924e, 0x1a1612],
    shapeTypes: ['icosahedron','dodecahedron','lowPolySphere','cube','octahedron'],
    shapeCount: 12, spread: 90, opacity: 0.07, cameraZ: 28,
    mouseFactor: 4, lerpFactor: 0.04, scrollDepth: 15, rotSpeed: 0.006, wireframe: false
};
/* body { background: #080808; }
   #bg-canvas { filter: blur(0.5px); } */
```

### 9.6 CSS Pattern Reference Library

Fine grid (technical, blueprint feel):
```css
background-image:
  linear-gradient(rgba(212,165,116,0.05) 1px, transparent 1px),
  linear-gradient(90deg, rgba(212,165,116,0.05) 1px, transparent 1px);
background-size: 40px 40px;
```

Small dots (soft, organic):
```css
background-image: radial-gradient(circle, rgba(240,237,232,0.12) 1px, transparent 1px);
background-size: 28px 28px;
```

Large dots (sparse, refined):
```css
background-image: radial-gradient(circle, rgba(212,165,116,0.08) 1.5px, transparent 1.5px);
background-size: 48px 48px;
```

Diagonal lines:
```css
background-image: repeating-linear-gradient(
  45deg,
  rgba(212,165,116,0.04) 0px, rgba(212,165,116,0.04) 1px,
  transparent 1px, transparent 18px
);
```

Crosshatch:
```css
background-image:
  repeating-linear-gradient(45deg, rgba(212,165,116,0.03) 0px, rgba(212,165,116,0.03) 1px, transparent 1px, transparent 18px),
  repeating-linear-gradient(-45deg, rgba(212,165,116,0.03) 0px, rgba(212,165,116,0.03) 1px, transparent 1px, transparent 18px);
```

Hex dots:
```css
background-image:
  radial-gradient(circle, rgba(212,165,116,0.09) 1px, transparent 1px),
  radial-gradient(circle, rgba(212,165,116,0.09) 1px, transparent 1px);
background-size: 24px 42px;
background-position: 0 0, 12px 21px;
```

**Pattern opacity guide**: 0.03 = barely there | 0.06 = felt on inspection | 0.10 = clearly visible | 0.15+ = intentional graphic element

### 9.7 Shape Personality Guide

| Shape | Personality | Best For |
|-------|-------------|----------|
| `torus` | Iconic donut ring, satisfying | Anchor shape, familiar |
| `octahedron` | Clean diamond, symmetrical | Very geometric, sharp |
| `icosahedron` | Faceted "near-sphere" | Sophisticated, mineral |
| `tetrahedron` | Simple triangle pyramid | Most minimal 3D shape |
| `cube` | Instantly readable | Good contrast to curved shapes |
| `lowPolySphere` | Rough gem/geode | Organic but geometric |
| `cone` | Directional, asymmetric | Movement, pointing energy |
| `cylinder` | Architectural column | Stable, structural |
| `flatRing` | Tumbling coin, portal | Very dynamic |
| `dodecahedron` | Rounder, more organic | Fuller than icosahedron |
| `torusKnot` | Statement pretzel knot | Use 1–2 max — very striking |
| `pyramid` | Egyptian, angular | Different silhouette |
| `hexPrism` | Honeycomb column | Natural, structured |
| `thinRing` | Delicate halo | Counterpoint to bulkier shapes |

**Good combos**: Bold mix: `torus + cube + tetrahedron + cone` | Organic: `icosahedron + dodecahedron + lowPolySphere` | Architectural: `cube + cylinder + pyramid + hexPrism` | Minimal: `torusKnot + thinRing + icosahedron`

### 9.8 Custom Cursor (Portfolio-Specific)
```javascript
// Two DOM elements: .cursor-dot (4px, accent circle) and .cursor-ring (40px, accent border)
document.addEventListener('mousemove', e => {
    dot.style.transform = `translate(${e.clientX - 2}px, ${e.clientY - 2}px)`;
    // Ring uses lerp for trailing effect
    ringX += (e.clientX - 40 - ringX) * 0.15;
    ringY += (e.clientY - 40 - ringY) * 0.15;
    ring.style.transform = `translate(${ringX}px, ${ringY}px)`;
});
// On hover of interactive elements: ring.style.transform += ' scale(2)'
// Hide both on mobile: @media (pointer: coarse) { .cursor-dot, .cursor-ring { display: none; } }
```

### 9.9 Performance Guardrails
- On mobile or `navigator.hardwareConcurrency < 4`: reduce shape count to 6–8, disable particles
- Always `pointer-events: none` on the canvas
- Stop animation loop on `prefers-reduced-motion` — show static CSS gradient instead
- Use `renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2))` — never full DPR on retina

---

## 10 — MOTION & ANIMATION

### General Apps and Tools
- Short fades and small slides: 120–220ms
- No bouncy springs unless product is explicitly playful
- Animate `transform` and `opacity` only — never layout properties
- Stagger animations: no more than 3–4 sequential steps visible at once

### Editorial / Portfolio
- GSAP CDN: `https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js`
- ScrollTrigger: `https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js`
- Use `gsap.from(el, { opacity: 0, y: 40, duration: 0.6, ease: 'power2.out' })` for reveals
- Stagger sibling reveals: `gsap.from('.card', { opacity: 0, y: 30, stagger: 0.1 })`

### Reduced Motion (MANDATORY)
```css
@media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
        animation-duration: 0.01ms !important;
        transition-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
    }
}
```

---

## 11 — REACT COMPONENTS (Type-Safe)

### Button Component
```tsx
interface ButtonProps extends ButtonHTMLAttributes<HTMLButtonElement> {
    variant?: 'primary' | 'secondary' | 'outline' | 'ghost' | 'danger';
    size?: 'sm' | 'md' | 'lg';
    isLoading?: boolean;
    leftIcon?: React.ReactNode;
    rightIcon?: React.ReactNode;
}

export const Button = forwardRef<HTMLButtonElement, ButtonProps>(
    ({ variant = 'primary', size = 'md', isLoading, leftIcon, rightIcon, children, disabled, ...props }, ref) => (
        <button
            ref={ref}
            className={cn(baseClasses, variantClasses[variant], sizeClasses[size])}
            disabled={disabled || isLoading}
            {...props}
        >
            {leftIcon && <span className="btn-icon-left">{leftIcon}</span>}
            <span className={isLoading ? 'opacity-0' : ''}>{children}</span>
            {isLoading && <span className="btn-spinner" aria-hidden="true" />}
            {rightIcon && <span className="btn-icon-right">{rightIcon}</span>}
        </button>
    )
);
```

### Skeleton Loading
```tsx
export function Skeleton({ variant = 'text', width, height }: SkeletonProps) {
    const variants = { text: 'h-4 rounded w-full', title: 'h-7 rounded w-3/4', avatar: 'h-10 w-10 rounded-full', card: 'h-48 rounded-lg' };
    return <div className={cn('animate-pulse bg-[var(--surface-2)]', variants[variant])} style={{ width, height }} aria-label="Loading" />;
}
```

### Tailwind Config Additions
```javascript
module.exports = {
    darkMode: ['class'],
    theme: {
        extend: {
            colors: {
                background: 'var(--bg)',
                surface: 'var(--surface-1)',
                border: 'var(--stroke)',
                foreground: 'var(--text)',
                muted: 'var(--muted)',
                accent: 'var(--accent)',
            },
            fontFamily: {
                display: 'var(--font-display)',
                body: 'var(--font-body)',
                mono: 'var(--font-mono)',
            },
            keyframes: {
                shimmer: { '0%': { backgroundPosition: '200% 0' }, '100%': { backgroundPosition: '-200% 0' } },
                'fade-in': { '0%': { opacity: '0', transform: 'translateY(8px)' }, '100%': { opacity: '1', transform: 'translateY(0)' } },
            },
            animation: {
                shimmer: 'shimmer 2s linear infinite',
                'fade-in': 'fade-in 0.3s ease-out',
            },
        },
    },
};
```

---

## 12 — ACCESSIBILITY (NON-NEGOTIABLE MINIMUM)

- Semantic HTML: `nav`, `main`, `aside`, `header`, `footer`, `section`
- Skip-to-content link on content-heavy pages
- Focus outlines: NEVER remove without replacing with an equivalent custom style
- Touch targets: minimum 24×24 CSS px; prefer ~44px on mobile
- ARIA: only where native HTML is insufficient
- Alt text: meaningful images described; decorative images `alt=""`
- Keyboard-friendly: filters, carousels, modals all reachable via keyboard
- `role="dialog"` + `aria-modal="true"` on modals
- `aria-label` on all icon-only buttons
- Color is never the ONLY way to convey information

---

## 13 — ENGINEERING HYGIENE

- No console errors in shipped product
- No dead code, no placeholder copy, no "TODO" visible to users
- Set real `<title>`, `<meta description>`, and favicon
- Z-index ladder defined via tokens — never ad-hoc values
- Closed overlays: `display:none` or `inert` — never `opacity:0` alone
- Scroll containment: only content panes scroll; shell is fixed
- Reserve image space (`width`/`height` or `aspect-ratio`) to prevent layout shift
- Lazy-load below-fold images — DO NOT lazy-load the hero/LCP image
- Avoid `backdrop-filter: blur()` by default — heavy on GPU
- Paginate or virtualise lists over ~200 rows
- `localStorage` for theme + sidebar state persistence when useful

---

## 14 — CDN DEPENDENCIES REFERENCE

```
Three.js r128:   https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js
GSAP:            https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js
ScrollTrigger:   https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js
Chart.js:        https://cdn.jsdelivr.net/npm/chart.js
Particles.js:    https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js
Lucide Icons:    https://cdn.jsdelivr.net/npm/lucide@latest/dist/umd/lucide.min.js
Alpine.js:       https://cdn.jsdelivr.net/npm/alpinejs@3.x.x/dist/cdn.min.js
Google Fonts:    https://fonts.googleapis.com
```

---

## 15 — DELIVERY CHECKLIST

Before delivering any website or component:

```
□ No console errors
□ All nav items route to real, populated views
□ All buttons and controls are wired and functional
□ Theme toggle works and persists (if applicable)
□ Mobile responsive: hamburger menu, single column, no overflow
□ Smooth scroll working
□ prefers-reduced-motion respected
□ All modals trap focus and close on ESC + backdrop
□ Empty, loading, and error states exist for all data views
□ Focus indicators visible on all interactive elements
□ No card soup: ≤6 panel cards in any viewport
□ No one-off hex values: all colors via CSS custom properties
□ No AI-smell fonts (Inter, Arial, Roboto) unless Pack A intentionally chosen
□ Skip-to-content link on content-heavy pages
□ Images have alt text
□ <title>, favicon, and meta description set
□ Custom cursor hidden on mobile (if used)
□ 3D canvas: pointer-events: none (if used)
□ Animated background stops on prefers-reduced-motion (if used)
```

---

## 16 — ANTI-TEMPLATE CHECKLIST ("Does it smell like AI?")

If any of these are true, fix them before delivery:

- [ ] Every section is inside a rounded card with a shadow
- [ ] Color scheme is purple gradient on white, or "startup blue" on dark
- [ ] Font is Inter, Roboto, or system-ui as the primary display font
- [ ] Hero section has: big headline + subheadline + two CTA buttons + feature grid
- [ ] Icons are decorative and carry no information
- [ ] There are more than 4 different font sizes in use without clear hierarchy
- [ ] Background is flat black or flat white with no atmosphere
- [ ] All spacing is identical regardless of section importance
- [ ] Hover states are the same as default states (nothing changes)
- [ ] The page could belong to any company/product in any industry

---

*Version 1.0 — Synthesized from: WIGLO Web_Key (Claude Edition), WIGLO 3D Background Guide v2, Frontend Design Skill (Z.ai Toolkit), Website Archetype Research, and Anthropic Frontend Design Skill.*
