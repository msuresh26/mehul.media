# Design System Strategy: The Cinematic Auteur

## 1. Overview & Creative North Star
**Creative North Star: The Architectural Frame**

This design system is not a template; it is a filmic experience. Inspired by the precision of a master director, the system rejects the "busy" aesthetics of modern SaaS in favor of architectural grandness, atmospheric depth, and a relentless focus on the "subject." 

We break the standard digital mold through **Intentional Asymmetry** and **Grand Proportions**. Instead of centering everything, we use the "Rule of Thirds" to anchor content, leaving vast amounts of `surface` as negative space to create a sense of scale. The interface should feel like a high-resolution 70mm frame: stable, authoritative, and timeless.

---

## 2. Colors & Atmospheric Depth
Our palette is rooted in the "Midnight" spectrum—deep charcoals and desaturated blues that evoke the feeling of a cold, high-stakes thriller.

*   **Primary (`#c3c7cd`):** A cold, metallic grey used for high-signal actions and primary information.
*   **Secondary (`#8da0b5`):** A muted, atmospheric blue for supporting elements and interactive states.
*   **Tertiary (`#faf9fe`):** A stark, paper-white used exclusively for high-contrast accents or "flash" moments in the UI.

### The "No-Line" Rule
Traditional 1px borders are strictly prohibited for sectioning. They feel "digital" and small. In this system, boundaries are defined by **Tonal Shifts**. 
*   Transition from `surface` to `surface-container-low` to define a sidebar.
*   Use `surface-container-highest` only for the most critical interactive focal points.
*   If a container requires a boundary, use a `1px` stroke of `outline-variant` at **15% opacity** (The Ghost Border).

### Signature Textures
To escape the sterile "flat" look, all primary surfaces should feature a global **film grain overlay** (approx. 3% opacity). Use a subtle radial gradient transitioning from `surface` at the center to `surface-container-lowest` at the edges to mimic the vignetting of a vintage camera lens.

---

## 3. Typography: The Editorial Voice
The typography is a dialogue between the modern (`Inter`) and the classical (`Noto Serif`).

*   **The Command (Sans-Serif):** Use `display-lg` and `headline` scales in `Inter` for data and titles. It represents the "precision" of the auteur. 
*   **The Narrative (Serif):** Use `title-lg` and `body-md` in `Noto Serif`. This adds "class" and warmth, making long-form text feel like a screenplay or a luxury publication.
*   **Scale as Hierarchy:** We utilize extreme contrast. A `display-lg` headline should often be paired with a very small `label-sm` to create a "Grand Proportion" effect.

---

## 4. Elevation & Tonal Layering
We do not use shadows to lift objects; we use **Tonal Stacking** and **Light Simulation**.

*   **The Layering Principle:** 
    *   Base: `surface`
    *   Subtle Inset: `surface-container-low`
    *   Active Component: `surface-bright`
*   **Glassmorphism:** For floating menus or modals, use `surface-variant` at 60% opacity with a `24px` backdrop blur. This ensures the atmospheric "grain" of the background still bleeds through, maintaining a sense of place.
*   **Ambient Glow:** In place of drop shadows, use a `120px` blur "glow" of `primary-container` at 5% opacity behind key elements to simulate a soft spotlight on a dark set.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary` with `on-primary` text. No rounded corners (`0px`). The button should feel like a physical slab.
*   **Secondary:** An "Outline" variant using the Ghost Border (`outline-variant` at 20%). On hover, the background fills to `surface-container-high`.
*   **Tertiary:** All-caps `label-md` text with a `2px` underline that expands from the center on hover.

### Cards & Lists
*   **Cards:** No borders. Use `surface-container-low`. Increase `spacing-8` (2.75rem) between cards to allow the "architecture" of the page to breathe.
*   **Lists:** Forbid divider lines. Separate list items using a `surface-container-low` background on hover, or simply use `spacing-4` (1.4rem) of vertical white space.

### Input Fields
*   **Field Style:** Minimalist bottom-stroke only using `outline`.
*   **Focus State:** The stroke transitions to `primary` with a subtle `surface-bright` glow.
*   **Error State:** Use `error` text, but keep the stroke `outline` to maintain visual composure.

### The "Auteur" Scrollbar
Custom-styled scrollbars are required. Width: `4px`. Track: `transparent`. Thumb: `outline-variant` with 50% opacity. It should be barely visible, like a frame edge.

---

## 6. Do’s and Don’ts

### Do:
*   **Use extreme negative space.** If a section feels "empty," it’s likely working.
*   **Mix your type.** Use `Noto Serif` for a quote or a caption immediately following an `Inter` headline.
*   **Embrace the Dark.** Ensure `surface` (#0e0e10) dominates at least 70% of any view.
*   **Hard Edges.** Every corner must be `0px` (Square). It conveys architectural permanence.

### Don't:
*   **No Rounded Corners.** Do not use `8px` or even `2px` radii. It breaks the "Architectural" rule.
*   **No Vibrant Colors.** Avoid any color not in the palette. High-saturation "Safety Oranges" or "Success Greens" should be muted to match the filmic tone (use `secondary` or `error_dim`).
*   **No Crowding.** Do not try to fit everything "above the fold." Let the user travel through the interface like a camera moving through a scene.
*   **No standard "Drop Shadows."** If an element doesn't have a backdrop-blur or a tonal shift, it shouldn't be floating.