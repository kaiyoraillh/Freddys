# Design
# Design System Document: The Animated Diner Aesthetic

## 1. Overview & Creative North Star
**Creative North Star: "The Technicolor Inkwell"**

This design system rejects the "safe" corporate flatness of modern SaaS. Instead, it leans into the high-energy, high-contrast world of 1930s rubber-hose animation fused with the chrome-and-neon optimism of a 1950s American diner. We achieve a "premium" feel not through muted tones, but through **extreme intentionality**.

By limiting our palette to a high-voltage Electric Blue and a sophisticated Cream, we create a visual rhythm that feels editorial and curated. The experience should feel like a vintage comic book come to life—breaking the grid with bold outlines, asymmetrical layouts, and "elastic" interactions that mimic the squash-and-stretch of early animation.

---

## 2. Colors & Tonal Logic

The palette is deceptive in its simplicity. We rely on the tension between the clinical `primary` (#0028d0) and the warmth of the `surface` (#fcf9f2).

* **Primary (#0028d0):** Use for high-impact brand moments and primary actions. It is our "ink."
* **Surface/Background (#fcf9f2):** Our "paper." It provides a warm, retro counter-balance to the electric blue.
* **Tertiary/Error (#891b00):** Reserved exclusively for "ketchup" moments—errors, deletions, or high-alert status.

### The Rules of Engagement
* **The "No-Line" Rule:** Standard 1px grey borders are strictly prohibited. Sectioning is achieved through the **Checkerboard Divider** (alternating `primary` and `surface_container`) or a hard shift to `surface_container_high`.
* **Surface Hierarchy:** Use `surface_container_lowest` (#ffffff) for card-level depth on a `surface` background. This creates a "sticker" effect, as if elements are pasted onto the page.
* **The "Ink-Trap" Rule:** In this system, we avoid complex gradients. To add "soul," use solid blocks of `primary_container` (#1b3fff) behind text to create a high-contrast, "highlighted" editorial look.

---

## 3. Typography: The Retro Headline

Our typography is the loudest voice in the room. We use a "Double-Impact" strategy: massive, condensed display type paired with highly legible, modern sans-serif body copy.

* **Display (Epilogue - Bold/Uppercase):** These are your "billboard" moments. Use `display-lg` (3.5rem) for hero sections. It should feel heavy, condensed, and architectural.
* **Body (Work Sans):** To ensure the system remains functional and premium, body text stays clean. Use `body-lg` (1rem) for most descriptions to maintain an airy, sophisticated feel against the heavy headlines.
* **Label (Work Sans - Uppercase):** All labels and small metadata should be uppercase with a +5% letter-spacing to mimic vintage menu typography.

---

## 4. Elevation & Depth: The "Celluloid" Stack

We do not use soft, blurry shadows to mimic reality. We mimic **animation layers**.

* **The Layering Principle:** Depth is created by stacking. A `surface_container_lowest` card sits on a `surface` background. To emphasize it, we use a **Hard Kickout**: a solid 4px or 8px offset shadow using `primary` at 20% opacity—never a blurry grey shadow.
* **The Checkerboard Divide:** When transitioning between major content themes (e.g., from a Product Feed to a Footer), use a 40px tall checkerboard pattern using `primary` and `surface_container`. This acts as a "hard stop" for the eye.
* **Ghost Borders:** If an element needs definition (like an input field), use `outline_variant` at 20% opacity. It should feel like a faint pencil sketch, not a digital box.

---

## 5. Components

### Buttons
* **Primary:** Solid `primary` background, `on_primary` (white) text. Shape: `md` (1.5rem) roundedness.
* **Secondary:** Solid `surface_container_highest` with a `primary` 2px "Ghost Border."
* **Interaction:** On hover, the button should "grow" (scale 1.05) and gain a solid `primary` offset shadow, mimicking the "squash and stretch" of a cartoon.

### Cards & Containers
* **Forbid Dividers:** Never use a horizontal line to separate content within a card. Use `Spacing 6` (2rem) of vertical white space or a subtle background shift to `surface_container_low`.
* **Illustrations:** All icons and imagery must feature a consistent "Ink Outline"—a 2px solid stroke in `primary` or `on_surface`.

### Input Fields
* **Style:** Background `surface_container_lowest`, no border.
* **Focus State:** A thick 3px solid `primary` border appears instantly. No soft glows. It should feel "snappy."

### The "Diner Menu" List
* **Style:** Instead of standard rows, use alternating background tints (`surface` to `surface_container`). Use `display-sm` for numbers or prices to give it a high-end editorial menu vibe.

---

## 6. Do’s and Don’ts

### Do:
* **Embrace Asymmetry:** Align text to the left but allow illustrations to "break" the container edges.
* **Use the Checkerboard:** Use it for headers, footers, or as a decorative "tape" to hold elements down.
* **Go Big:** If a headline feels too large, it’s probably just right for this system.

### Don’t:
* **Don't use Gradients:** This system relies on flat, "inked" colors. Gradients kill the rubber-hose aesthetic.
* **Don't use Rounded-Full (Pills):** Stick to the `md` (1.5rem) or `lg` (2rem) scale. Perfect pills feel too modern/tech-focused; we want the "chunky" hand-drawn feel.
* **Don't use Grey:** If you need a neutral, use `surface_dim` or a desaturated version of our Cream. Pure grey is the enemy of the 1950s warmth.

### Accessibility Note:
While the `primary` Electric Blue is vibrant, ensure all `on_primary` text passes WCAG AA contrast ratios. When using Blue text on Cream, always use the `primary` (#0028d0) token rather than the lighter `primary_container` variant to ensure legibility.
