# Style Guide — Matteus da Costa Portfolio

> **For Claude Code:** Before editing any CSS or HTML, read this file in full.
> Replace every hard-coded color value in `index.html` with the CSS variable from
> the token table below. Never introduce a color not listed in this guide.
> Never introduce a new spacing value outside the spacing scale.
> When in doubt, ask before adding new patterns.

---

## 1. Brand Mark

The logotype is a stylised **tt** stacked ligature.

| Property | Value |
|---|---|
| Default fill | `--color-text` (#1E4D35 on Bone) |
| Minimum size | 20 px |
| Usage | Nav, footer — always `currentColor` so it inherits the surface text |

---

## 2. Color Palette

### 2.1 Bone — Active palette (portfolio)

All colors are sourced exclusively from `index.html`. No new colors may be added.

| Token | Hex | Usage |
|---|---|---|
| `--color-bg` | `#F4F1EA` | Page background, hero, about, experience outer, footer |
| `--color-text` | `#1E4D35` | All primary text, icons, nav links, headings |
| `--color-text-muted` | `rgba(30,77,53,.65)` | Secondary text, card labels, group titles, client names |
| `--color-text-soft` | `rgba(30,77,53,.3)` | Timeline line, meta dots, dividers |
| `--color-surface` | `#FFFFFF` | Experience card background |
| `--color-surface-hover` | `#EAE5D7` | Card hover fill + box-shadow spread |
| `--color-surface-placeholder` | `#E2DDD0` | Image placeholders, empty tiles |
| `--color-accent` | `#BFE3C8` | CTA pill on content cards |
| `--color-accent-icon` | `#F4683D` | About section accent icon (brand mark variant) |

#### New colors — all tokens are new

`index.html` currently has **no CSS variables** — every color is hard-coded as a hex or rgba value.
Claude Code's first task is to add a `:root {}` block with all tokens below and replace every
hard-coded instance in the file.

| Token | Hex | Hard-coded as |
|---|---|---|
| `--color-bg` | `#F4F1EA` | `#F4F1EA` — page bg, hero, about, footer |
| `--color-text` | `#1E4D35` | `#1E4D35` — all primary text and icons |
| `--color-text-muted` | `rgba(30,77,53,.65)` | `rgba(30,77,53,.65)` — secondary text |
| `--color-text-soft` | `rgba(30,77,53,.3)` | `rgba(30,77,53,.3)` — timeline line, dots |
| `--color-surface` | `#FFFFFF` | `#FFFFFF` — experience card bg |
| `--color-surface-hover` | `#EAE5D7` | `#EAE5D7` — card hover fill + shadow |
| `--color-surface-placeholder` | `#E2DDD0` | `#E2DDD0` and `#ddd` — image tiles |
| `--color-accent` | `#BFE3C8` | `#BFE3C8` — CTA pill on content cards |
| `--color-accent-icon` | `#F4683D` | `#F4683D` — about section accent icon |

---

### 2.2 Brand secondaries (reference only — not in portfolio palette)

Available for future use. Do not introduce into `index.html` without explicit instruction.

| Name | Hex |
|---|---|
| Deep Blue | `#09245B` |
| Celestial Blue | `#569FD6` |
| Harmony Green | `#AFDDB6` |
| Vibrant Orange | `#F4683D` |
| Solar Yellow | `#F5E961` |

---

### 2.3 Neutrals & Gray scale (reference only)

| Stop | Hex |
|---|---|
| 25 | `#FDFDFD` |
| 50 | `#FAFAFA` |
| 100 | `#F5F5F5` |
| 200 | `#E9EAEB` |
| 300 | `#D5D7DA` |
| 400 | `#A4A7AE` |
| 500 | `#717680` |
| 600 | `#535862` |
| 700 | `#414651` |
| 800 | `#252B37` |
| 900 | `#181D27` |
| White | `#FFFFFF` |
| Black | `#000000` |

---

## 3. Typography

### 3.1 Font family

| Token | Value |
|---|---|
| `--font-sans` | `"Work Sans", system-ui, sans-serif` |

Work Sans is the single typeface. No secondary typeface is active in the portfolio.

### 3.2 Heading scale

| Level | Size / Line-height | Weight | Usage |
|---|---|---|---|
| H1 | 50px / 60px | 700 | Reserved — not currently used |
| H2 | 38px / 48px | 550 (600) | Hero lines |
| H3 | 28px / 34px | 550 (600) | Section headings (Experience h2, About h2) |
| H4 | 20px / 28px | 550 (600) | Job titles, card titles |

### 3.3 Content scale

| Role | Size / Line-height | Weight | Token usage |
|---|---|---|---|
| Body | 16–17px / 26px | 400 | Hero body, about paragraphs |
| Label | 16px / 16px | 550 (600) | Nav links, section labels |
| Tag | 14px / 20px | 550 (600) | Card labels, clients-label, meta dates |
| Info | 12–13px / 18px | 400–550 | Footer group titles, about location |

### 3.4 Active type decisions in index.html

```
Hero line 1:   38px / 400 / ls 0      — "Call me Matteus"
Hero line 2:   38px / 600 / ls 0      — "& I'm a Senior Product Designer"
Hero body:     17px / 400 / lh 1.6
About h2:      26px / 700 / ls -0.01em
Card title:    24px / 500 / ls -0.005em
Job title:     20px / 600 / ls -0.005em
Exp h2:        32px / 600 / ls -0.005em
Section label: 16px / 600 / uppercase
```

---

## 4. Spacing Scale

Based on a **×2 doubling system** anchored at 4px.

| Token | Value | Usage in portfolio |
|---|---|---|
| `space-1` | 4px | Micro gaps, dot sizes |
| `space-2` | 8px | Photo grid gap, card inner gaps |
| `space-3` | 14px | Group title margin, link list gap |
| `space-4` | 28px | Hero body margin-top, grid gaps |
| `space-5` | 56px | Page horizontal padding, section column gaps |
| `space-6` | 112px | Section vertical padding, contributed margin-top |
| `space-7` | 224px | Photo tile width, max layout reference |

---

## 5. Elevation

### Soft (ambient, low contrast)

| Level | Shadow value |
|---|---|
| soft / light | `0 1px 3px 0 rgba(24,29,39,.06)` |
| soft / medium | `0 2px 4px 0 rgba(24,29,39,.10)` |
| soft / dark | `0 5px 10px 0 rgba(24,29,39,.10)` |

### Emphasis (intentional lift)

| Level | Shadow value |
|---|---|
| emphasis / light | `0 12px 20px -2px rgba(24,29,39,.15)` |
| emphasis / medium | `0 32px 48px -12px rgba(24,29,39,.20)` |
| emphasis / dark | `0 48px 80px -12px rgba(24,29,39,.25)` |

**Current portfolio usage:** `.exp-card` uses no explicit shadow (white card on bone bg — contrast is sufficient). Card hovers use `box-shadow: 0 0 0 16px var(--color-surface-hover)` — a spread-only shadow, not elevation.

---

## 6. Border Radius

| Token | Value | Usage |
|---|---|---|
| `radius-xs` | 2px | — |
| `radius-sm` | 4px | Cards, swatches |
| `radius-md` | 8px | — |
| `radius-lg` | 16px | `.exp-card` top corners, hover media |
| `radius-pill` | 9999px | CTA chips |

**Current portfolio usage:** `.exp-card` → `16px 16px 0 0`. Hover cards animate to `border-radius: 14px`. Content media animate to `14px` on hover.

---

## 7. Motion

| Property | Value |
|---|---|
| Default duration | `0.25s` |
| Default easing | `ease` |
| Spatial easing | `cubic-bezier(.4,.2,.2,1)` (arrows) |
| Image scale easing | `cubic-bezier(.2,.7,.2,1)` (mockup hover) |

**Rules:**
- Transitions on color/bg: `0.25s ease`
- Arrow translate on hover: `translate(2px, -2px)` / `0.25s cubic-bezier(.4,.2,.2,1)`
- Card hover (bg + shadow + radius): `0.25s ease`
- Logo marquee: `40s linear infinite`, paused on hover
- Never add motion that wasn't explicitly requested

---

## 8. Layout principles

- Page horizontal padding: **56px** (`space-5`)
- Section vertical rhythm: **80–120px** (`space-5` to `space-6`)
- Max content width: **1200px** (experience card), **971px** (content section)
- No dark mode, no theme switching — Bone palette only
- No borders except `box-shadow: inset` for image placeholders
- No new shadows beyond the elevation scale above

---

## 9. Backlog (do not implement yet)

- Semantic token layer (map raw values to roles: `--color-bg-page`, `--color-fg-default`, etc.)
- CSS custom property consolidation across all sections into a single `:root` block
- Dark mode / alternate palette support

---

## 10. Claude Code instructions

1. **Read this file and `index.html` before any edit.**
2. Replace all hard-coded hex/rgba color values in `index.html` with the CSS variable from §2.1.
3. Do not add any color not listed in §2.1 for the active Bone palette.
4. Do not add spacing values outside §4.
5. Do not add new animation patterns — match existing timing/easing values.
6. Do not add new border-radius values — use tokens from §6.
7. If a change requires a new pattern, flag it and ask before proceeding.
