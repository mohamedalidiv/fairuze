# Design System Strategy: The Botanical Archivist

## 1. Overview & Creative North Star
The creative North Star for this design system is **"The Botanical Archivist."** 

We are moving away from the "grocery app" template and toward a high-end editorial experience. This system treats every food product as a specimen of artisanal craft. By blending the heritage of Egyptian botanical history with modern apothecary precision, we create an interface that feels curated, not just populated.

To achieve this, we break the traditional rigid grid. We utilize **intentional asymmetry**, where images may bleed off-center or overlap with typography, and we rely on **tonal depth** rather than structural lines to guide the eye. This creates a digital environment that feels as tactile and premium as a linen-bound book.

---

## 2. Color Philosophy: Tonal Atmosphere
Our palette is rooted in the earth. The interaction between the Deep Forest Green and the Warm Cream creates a high-contrast, prestigious foundation, while the Vibrant Red is used sparingly as a "heartbeat" color for critical actions.

### The "No-Line" Rule
To maintain an artisanal feel, **1px solid borders are strictly prohibited** for sectioning or containment. Boundaries must be defined through:
*   **Background Shifts:** Use `surface-container-low` sections sitting on a `surface` background.
*   **Soft Transitions:** Utilize subtle tonal shifts between container tiers to imply structure.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of fine paper. 
*   **Base:** `surface` (#fbfaee) is your canvas.
*   **Nesting:** Place a `surface-container-low` (#f5f4e8) section to group content. Inside that, use `surface-container-highest` (#e4e3d7) for interactive cards. This "stacking" creates natural depth.

### The "Glass & Gradient" Rule
For floating elements (like navigation bars or hovering price tags), use **Glassmorphism**. Apply `surface` colors at 80% opacity with a `backdrop-blur` of 12px-16px. 
*   **Signature Polish:** Main CTAs or Hero sections should use a subtle linear gradient from `primary` (#00450d) to `primary_container` (#1b5e20) at a 135-degree angle to provide a sense of "visual soul."

---

## 3. Typography: The Editorial Voice
The typography scale is designed to mimic a premium food journal. 

*   **Display & Headlines (Newsreader):** This serif font is our heritage voice. Use `display-lg` (3.5rem) for hero titles to create an authoritative, artisanal presence. In Arabic, ensure the typeface matches the weight and elegance of Newsreader’s high-contrast strokes.
*   **Body & Labels (Manrope):** Our modern functional voice. `body-lg` (1rem) is the workhorse for descriptions. 
*   **Hierarchy as Identity:** Always pair a large `headline-md` Serif with a small, all-caps `label-md` Sans-serif (tracked out 5-10%) to create that "Modern Apothecary" label aesthetic.

---

## 4. Elevation & Depth: Tonal Layering
We do not use shadows to create "pop"; we use them to create "atmosphere."

*   **The Layering Principle:** Avoid elevation shadows where possible. Instead, achieve lift by placing a `surface-container-lowest` (#ffffff) card on top of a `surface-container` (#efeee3) background.
*   **Ambient Shadows:** When an element must float (e.g., a modal), use a shadow with a blur radius of at least 40px and an opacity of 4%-6%. The shadow color must be a tinted version of `on-surface` (#1b1c15) to mimic natural light.
*   **The "Ghost Border" Fallback:** If a border is required for accessibility, use `outline_variant` (#c0c9bb) at **15% opacity**. Never use 100% opaque strokes.

---

## 5. Signature Components

### Buttons
*   **Primary:** Rounded `xl` (1.5rem/24px). Background: `primary` gradient. Text: `on_primary`.
*   **Secondary:** Rounded `xl`. Background: `secondary` (#b6171e). Used for "Add to Cart" or "Buy Now" to provide a vibrant, appetizing contrast.
*   **States:** On hover, increase the container saturation slightly. Avoid harsh color swaps.

### Cards & Product Specimen
*   **Style:** No borders. Use `surface-container-highest` with `xl` (24px) corner radius.
*   **Content:** Images should be high-quality, top-down or "macro" shots. Forbid the use of divider lines inside cards; use vertical whitespace (24px - 32px) to separate the title from the price.

### Inputs & Search
*   **Style:** Use `surface-variant` (#e4e3d7) backgrounds. 
*   **Focus State:** Instead of a thick border, use a subtle 1px "Ghost Border" of `primary` at 40% opacity and a slight tonal shift of the background.

### Bilingual Navigation
*   **RTL/LTR Balance:** Mirror all layouts for Arabic support. Ensure that the serif headings in Arabic maintain the same optical scale as the English Newsreader. The "Modern Apothecary" feel is maintained by ensuring the Arabic calligraphy feels as "ink-on-paper" as the English serif.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use organic, asymmetrical image masks (e.g., a "leaf" or "pebble" shape) for decorative imagery.
*   **Do** utilize generous whitespace. If you think there is enough space, add 16px more.
*   **Do** use `secondary` (#b6171e) as a highlight for badges (e.g., "New," "Organic") to draw the eye with high-end urgency.

### Don't:
*   **Don't** use pure black (#000000) for text. Always use `on_surface` (#1b1c15) to maintain the "warm paper" feel.
*   **Don't** use 1px dividers to separate list items. Use a 1px height shift in background color or simply 16px of clear space.
*   **Don't** use "standard" box shadows. If the shadow looks like a "drop shadow," it is too heavy. It should look like a "glow of absence."
*   **Don't** crowd the logo. The Fairuz Foods logo needs a "safety zone" of at least 48px to breathe within the layout.