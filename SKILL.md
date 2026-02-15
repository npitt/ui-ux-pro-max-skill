---
name: ui-ux-pro-max
description: UI/UX design intelligence. 50 styles, 21 palettes, 50 font pairings, 20 charts, 9 stacks.
---

# UI/UX Pro Max

Comprehensive design guide for web and mobile applications. Contains 67 styles, 96 color palettes, 57 font pairings, 99 UX guidelines, and 25 chart types across 13 technology stacks. Searchable database with priority-based recommendations.

## Prerequisites

Check if Python is installed:

```bash
python3 --version || python --version
```

---

## How to Use This Skill

When user requests UI/UX work (design, build, create, implement, review, fix, improve), follow this workflow:

### Step 1: Analyze User Requirements

Extract key information from user request:
- **Product type**: SaaS, e-commerce, portfolio, dashboard, landing page, etc.
- **Style keywords**: minimal, playful,  - **Concept**: ESG-First / Sustainability Hero / Eco-Hero
  - **Palette**: Emerald-600 (Eco-Hero), Slate-900 (Text), Emerald-50 (Surface)
  - **Principle**: Energy-saving aesthetic, clear metrics, branded watermarks, power-efficient aesthetics.
- **Industry**: healthcare, fintech, gaming, education, etc.
- **Stack**: React, Vue, Next.js, or default to `html-tailwind`

### Step 2: Generate Design System (REQUIRED)

**Always start with `--design-system`** to get comprehensive recommendations with reasoning:

```bash
python3 .agent/skills/ui-ux-pro-max/src/ui-ux-pro-max/scripts/search.py "<product_type> <industry> <keywords>" --design-system [-p "Project Name"]
```

This command:
1. Searches 5 domains in parallel (product, style, color, landing, typography)
2. Applies reasoning rules from `ui-reasoning.csv` to select best matches
3. Returns complete design system: pattern, style, colors, typography, effects
4. Includes anti-patterns to avoid

**Example:**
```bash
python3 .agent/skills/ui-ux-pro-max/src/ui-ux-pro-max/scripts/search.py "beauty spa wellness service" --design-system -p "Serenity Spa"
```

### Step 3: Supplement with Detailed Searches (as needed)

After getting the design system, use domain searches to get additional details:

```bash
python3 .agent/skills/ui-ux-pro-max/src/ui-ux-pro-max/scripts/search.py "<keyword>" --domain <domain> [-n <max_results>]
```

**Domains**: `style`, `chart`, `ux`, `typography`, `landing`, `product`, `color`.

### Step 4: Stack Guidelines (Default: html-tailwind)

Get implementation-specific best practices. If user doesn't specify a stack, **default to `html-tailwind`**.

```bash
python3 .agent/skills/ui-ux-pro-max/src/ui-ux-pro-max/scripts/search.py "<keyword>" --stack html-tailwind
```

---

## Pre-Delivery Checklist (MANDATORY)

- [ ] No emojis as icons (use SVG)
- [ ] `cursor-pointer` on all interactables
- [ ] Smooth transitions (150-300ms)
- [ ] Light/Dark mode contrast checks
- [ ] Responsive design (mobile/tablet/desktop)
- [ ] **ESG Visual Rule**: ESG/Sustainability elements are ALWAYS Green, NEVER Brand-Red.
- [ ] **Eco-Hero PageHeader**: All main list views MUST apply `:eco="true"` to `PageHeader`.
- [ ] **Sidebar Consistency**: All menu levels (including sub-menus) MUST have expressive SVG icons for navigation clarity.

