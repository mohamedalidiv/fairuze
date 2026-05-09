# Fairuz Foods — فيروز
### The Botanical Archivist · Premium Egyptian Spice Brand

---

## Overview

**Fairuz Foods** is a high-end Egyptian artisanal food brand — a premium e-commerce frontend built without frameworks, treating every product as a botanical specimen with editorial precision. The project blends heritage Egyptian botanical aesthetics with a modern apothecary visual identity.

> *"Every spice a specimen. Every harvest an archive."*

---

## Pages

| File | Page | Direction |
|------|------|-----------|
| `index.html` | Homepage — Botanical Archive | LTR |
| `our-story.html` | Our Story — قصتنا | LTR |
| `recipes.html` | Recipes — وصفات فيروز | RTL (Arabic) |
| `shop.html` | Cart — سلة التسوق | LTR |

---

## Tech Stack

- **HTML5** — semantic, no frameworks
- **Tailwind CSS** (CDN) — with a fully custom design token config
- **Google Fonts** — Newsreader (serif headlines) + Manrope (body/labels)
- **Material Symbols Outlined** — iconography
- **Vanilla JavaScript** — cart logic, dark mode, localStorage
- **No backend dependencies** — API-hook ready structure

---

## Design System — "The Botanical Archivist"

The full design philosophy lives in [`DESIGN.md`](./DESIGN.md). Key principles:

### Color Palette
| Token | Hex | Role |
|-------|-----|------|
| `primary` | `#00450d` | Deep Forest Green — brand authority |
| `secondary` | `#b6171e` | Vibrant Red — "heartbeat" color, CTAs |
| `surface` | `#fbfaee` | Warm Cream — canvas base |
| `on-surface` | `#1b1c15` | Warm Black — never pure #000 |
| `surface-container-highest` | `#e4e3d7` | Card backgrounds |

### Typography
- **Headlines:** Newsreader (serif) — editorial, artisanal heritage voice
- **Body / Labels:** Manrope (sans-serif) — modern functional voice
- **Signature pairing:** Large serif headline + small all-caps sans-serif label with 5–10% letter-spacing → "Modern Apothecary" aesthetic

### Core Rules
- **No 1px borders** for sectioning — use background tonal shifts instead
- **No pure black (#000000)** — always `on-surface` (#1b1c15)
- **Glassmorphism nav** — surface colors at 80% opacity + `backdrop-blur`
- **Ghost borders only** — `outline-variant` at 15% opacity max
- **Generous whitespace** — when in doubt, add 16px more
- **Ambient shadows** — blur ≥ 40px, opacity 4–6%, never a standard drop shadow

---

## Features

- **Multi-page** Arabic/English bilingual layout (RTL/LTR support)
- **Cart system** — add/remove items, quantity control, order summary
- **Dark mode** — via Tailwind `darkMode: "class"`
- **Product badges** — "Limited Harvest", "Artisanal", "New", "Organic"
- **Bottom navigation** — fixed mobile nav (Atelier / Specimens / Cart / Journal)
- **Newsletter signup section**
- **Promo codes** — backend-ready hooks
- **WhatsApp integration** — contact/order support ready
- **Responsive** — mobile-first design

---

## Project Structure

```
fairuz-foods/
├── index.html          # Homepage
├── our-story.html      # Brand story page
├── recipes.html        # Recipes archive (Arabic RTL)
├── shop.html           # Shopping cart
└── DESIGN.md           # Full design system documentation
```

---

## Brand Identity

**Fairuz Foods** sources premium Egyptian botanical ingredients — spices, oils, garlic, honey — directly from small-batch producers across the Nile Delta and Siwa Oasis. The brand positions itself as a **curator of Egyptian culinary heritage**, not a grocery store.

Product naming follows the "Specimen Archive" system:
- Products have catalogue numbers (e.g. *Saffron Specimen N°04*)
- Categories are called "Archives" (Meat Dishes, Bakery, Quick Spices...)
- The cart is the *"Cart Archive"*, checkout is *"Complete Archive Acquisition"*

---

## Setup

No build step required. Open any `.html` file directly in a browser.

For development:
```bash
# Any local server works, e.g.:
npx serve .
# or
python3 -m http.server 8080
```

---

## Credits

Designed & developed under the **Botanical Archivist** design system.  
Brand: **Fairuz Foods — فيروز** · Alexandria, Egypt.

---

*"ولدنا من طمي النيل الأسود."*  
*Born from the Black Silt of the Nile.*
