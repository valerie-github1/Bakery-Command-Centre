# Blessed Bites — Design System

## Overview

**Blessed Bites** is a keto bakery startup founded by Mayah. The Command Centre is an all-in-one **AI-powered business management web app** — a productivity, budgeting, project management, and scheduling tool built specifically for the bakery owner. The product has a premium, warm, handcrafted aesthetic that balances professional SaaS UX with the warmth of an artisan food brand.

### Source Materials
- **Live app:** https://valerie-github1.github.io/Bakery-Command-Centre/
- **GitHub repo:** https://github.com/valerie-github1/Bakery-Command-Centre (HTML/CSS/JS monolithic file)
- No Figma file provided. Design system reverse-engineered from the live product.

---

## Products / Surfaces

| Product | Description |
|---|---|
| **Command Centre** | Web app — dashboard, standup, kanban, scheduler, budget, style guide, roadmap |

### App Sections
1. **Dashboard** — KPI cards, revenue streams, budget health, active tasks, recent transactions
2. **Daily Standup** — 4-question AI-driven standup form; generates briefing via Claude (Sage)
3. **Kanban Board** — Task management with To Do / In Progress / Blocked / Done columns
4. **Scheduler** — Daily timeline + weekly overview
5. **Budget Centre** — Business & personal finance tracking, category budgets, transaction log
6. **Style Guide** — In-app brand reference (colours, type, components)
7. **Roadmap** — 3-phase product roadmap with feature value matrix

### AI Agents
- **Sage** 🍰 — Primary AI business assistant (briefings, intelligence panels, finance analysis)
- **Pixie** 🧚 — Chibi fairy mascot, lives in the bottom-right corner; time-based states (morning gems, daytime float, night sleep)

---

## Content Fundamentals

### Voice & Tone
- **Warm, encouraging, expert** — like a brilliant friend who happens to run a bakery and knows finance
- Uses first-person plural ("we") in product copy, but addresses the user directly as "you"
- Celebratory but grounded: "Good morning! Today is Tuesday — your highest walk-in day."
- Uses **bold** within prose for emphasis, not headers
- Numbers and money are always formatted with £ and commas: `£12,345`
- Percentages shown with ↑↓ arrows and context: "↑ 12% vs last week"
- Concise, action-oriented: "Call SumUp before your first bake."
- AI messages end with a 🍰 emoji for Sage; 💕 for Pixie

### Casing & Labels
- **Navigation labels:** Title case — "Daily Standup", "Budget Centre"
- **KPI labels:** Title case — "Week Revenue", "Net Profit"
- **Badge labels:** ALL CAPS — "ACTIVE", "BLOCKED", "IN PROGRESS"
- **Buttons:** Title case or Sentence case — "Submit — Generate AI Briefing"
- **Dates:** "Tue 22 Apr 2025" format; relative dates "Yesterday", "2 days ago"

### Emoji Usage
- 🍰 — Sage AI marker (used as avatar/icon)
- 🧚 — Pixie marker
- Contextual in AI copy: 🥐 (bake), 🚚 (delivery), 📞 (calls), 📊 (data)
- **Never decorative** — emoji serve a functional role

---

## Visual Foundations

### Colour System
**Sidebar / Navigation — Dark Warm Browns:**
- Mahogany `#1A150D` — sidebar bg (deepest)
- Earth `#3D2B1A` — sidebar hover / secondary panels
- Coffee `#5C3D1E` — active states, elevated elements

**Warm Neutrals — Main Canvas:**
- Cream `#FAF5EE` — page background
- Almond `#F0E4D4` — card backgrounds, subtle sections
- Caramel `#C49A6C` — accent lines, borders, warm highlights

**Pink Accents — Brand Signature:**
- Blush `#F2C4CE` — light accent backgrounds
- Petal `#E8A0B0` — mid-weight accent
- Rose `#C4687E` — primary CTA, active badges, buttons

**Greens — Secondary Accent / Health indicators:**
- Matcha `#A8C090` — light green badges
- Sage `#8CA888` — mid green (AI Sage colour identity)
- Forest `#3D5A38` — deep green, success states

**Semantic:**
- Success: Forest `#3D5A38`
- Warning: Caramel `#C49A6C`
- Danger/Blocker: Rose `#C4687E`
- Active/In Progress: Sage `#8CA888`

### Typography
- **Display / Headings:** Cormorant Garamond — serif, elegant, artisanal. Used for H1–H2, large numerals.
- **Body / UI:** DM Sans — clean, geometric, warm. Used for all body copy, labels, nav items.
- **Mono / Numbers / Data:** DM Mono — tabular figures, transaction amounts, timestamps.
- **Scale:** 11px (metadata) → 13px (labels) → 15px (body) → 18px (subheads) → 24px (H3) → 32px (H2) → 48px+ (display KPIs)
- **Weight range:** 300 (light numerals) → 400 (body) → 500 (medium) → 600 (semibold labels) → 700 (bold)

### Backgrounds
- Main canvas: `#FAF5EE` (Cream) — warm off-white, never pure white
- Cards: `#FFFFFF` or `#F0E4D4` with subtle shadow
- Sidebar: `#1A150D` dark mahogany
- No full-bleed images in app UI; no gradients in backgrounds
- Subtle texture implied through warm colour layering

### Cards
- Border radius: `12px` standard; `8px` for small elements; `20px` for large panels
- Shadow: `0 2px 12px rgba(61,43,26,0.08)` — warm brown shadow, not blue/grey
- Border: `1px solid rgba(196,154,108,0.2)` — Caramel at low opacity
- Background: White or Almond `#F0E4D4`
- Padding: `20–24px`

### Spacing System
- Base unit: `4px`
- Scale: 4 · 8 · 12 · 16 · 20 · 24 · 32 · 40 · 48 · 64px
- Section gaps: `24px`; card inner padding: `20–24px`; label-to-value gap: `8px`

### Borders & Radii
- `4px` — small chips, tiny badges
- `8px` — buttons, input fields, small cards
- `12px` — standard cards, panels
- `20px` — large panels, modals, Pixie bubble
- `9999px` — pill badges, progress bars

### Shadows & Elevation
- Level 0 (flat): no shadow
- Level 1 (card): `0 2px 12px rgba(61,43,26,0.08)`
- Level 2 (panel): `0 4px 24px rgba(61,43,26,0.12)`
- Level 3 (modal/overlay): `0 8px 40px rgba(61,43,26,0.18)`
- Pixie chat: glassmorphism — `backdrop-filter: blur(20px)` + `rgba(250,245,238,0.85)` bg

### Animation
- Transitions: `0.2s ease` for hover states, colour changes
- Sidebar collapse: `0.3s ease`
- AI panel loading: shimmer/fade-in
- Pixie: CSS keyframe float (`translateY -8px`, `2s ease-in-out infinite`)
- Progress bars: width transition `0.6s ease`
- No bounce; easing is smooth and calm
- Reduced motion respected

### Hover States
- Sidebar items: `background rgba(255,255,255,0.08)` + `translateX(2px)`
- Cards: subtle shadow increase + `translateY(-1px)`
- Buttons: `brightness(1.08)` or darkened variant
- Links: colour shift toward Rose

### Icons
- Uses **Unicode symbols** as icons throughout: ◈ ◎ ▦ ◷ ◐ ◆ — decorative glyphs
- Emoji for AI agents: 🍰 🧚
- Contextual emoji in AI copy: 🥐 🚚 📞 📊
- No external icon library used in original; see ICONOGRAPHY section

### Layout
- Sidebar: fixed, `260px` wide, dark mahogany
- Main content: scrollable, fluid, `calc(100% - 260px)`
- Content max-width: `1200px` centred
- Responsive: sidebar collapses on mobile
- Grid: 3-column KPI cards, 2-column budget/tasks panels, full-width chart areas

### Glassmorphism Usage
- **Pixie chat bubble:** `backdrop-filter: blur(20px)`, warm cream bg at 85% opacity
- **Sage AI panels:** light glass treatment on AI message areas
- Applied sparingly — only for floating / overlay elements

### Corner Radii Personality
- Everything is rounded; no sharp corners
- Consistent warmth through rounding

---

## Iconography

**Approach:** The original app uses Unicode glyphs as navigation icons (◈ ◎ ▦ ◷ ◐ ◆) rather than an icon font or SVG set. This is a distinctive brand choice — minimal, elegant, symbol-based.

- Nav: Unicode dingbats — see colors_and_type.css for the full mapping
- AI agents use emoji as identity markers (🍰 Sage, 🧚 Pixie)
- **No external icon library** is used in the original app
- For the UI kit, we use **Lucide Icons** (CDN) as a supplementary icon set where needed, as it matches the clean geometric aesthetic. Flagged as a substitution.

**Logo / Brand Mark:**
- 🍰 cupcake emoji used as the app icon / wordmark in nav header
- No formal SVG logomark exists in the source; using cupcake + wordtype lockup
- Brand assets stored in `assets/`

---

## File Index

```
README.md                        ← This file
SKILL.md                         ← Agent skill definition
colors_and_type.css              ← All CSS variables: colors, type, spacing
assets/
  logo-lockup.svg                ← Blessed Bites wordmark + cupcake
  color-swatches.svg             ← Brand color palette reference
preview/
  colors-sidebar.html            ← Sidebar/dark color swatches
  colors-neutrals.html           ← Neutral warm palette
  colors-pink.html               ← Pink accent palette
  colors-green.html              ← Green palette
  colors-semantic.html           ← Semantic color usage
  type-display.html              ← Cormorant Garamond display specimens
  type-body.html                 ← DM Sans body specimens
  type-mono.html                 ← DM Mono specimens
  type-scale.html                ← Full type scale
  spacing-tokens.html            ← Spacing + radius + shadow tokens
  components-buttons.html        ← Button variants
  components-badges.html         ← Badge/status variants
  components-cards.html          ← Card variants
  components-kpi.html            ← KPI card components
  components-sidebar.html        ← Sidebar navigation component
  components-ai-panel.html       ← Sage AI panel component
  brand-pixie.html               ← Pixie mascot states
  brand-logo.html                ← Logo lockup and usage
ui_kits/
  command_centre/
    README.md                    ← UI kit notes
    index.html                   ← Full interactive prototype
    Sidebar.jsx                  ← Sidebar navigation component
    Dashboard.jsx                ← Dashboard screen
    Kanban.jsx                   ← Kanban board screen
    Budget.jsx                   ← Budget centre screen
    Standup.jsx                  ← Daily standup screen
    Scheduler.jsx                ← Scheduler screen
```
