# BaselineCSS v2026-10

*Disclaimer: This project was created using AI (Gemini Deep Research).*

A definitive, dual-layer CSS foundation optimized for modern web development in 2026. This project provides both an unopinionated **Reset** to normalize cross-browser quirks and an opinionated **Reboot** to establish a robust, fluid, and accessible baseline for modern design systems.

## 🚀 Features

- **Cascade Layers (`@layer`)**: Built natively on `@layer reset`, `@layer theme` and `@layer base` to ensure zero specificity conflicts with your component CSS.
- **Zero Magic Numbers**: Fully driven by CSS Custom Properties, `calc()`, `clamp()`, and relative units (`ch`, `rem`, `lh`).
- **Modern Layout & Viewports**: Utilizes logical properties (e.g., `margin-block`, `inline-size`) for native RTL/internationalization support, along with dynamic viewport units (`dvh`/`svh`).
- **Advanced Typography**: Integrates `text-wrap: balance` (for headings), `text-wrap: pretty` (for body), and fluid typography scales.
- **Progressive Input Styling**: Features `field-sizing: content` for auto-expanding inputs and intelligent `:focus-visible` handling.
- **Accessibility First**: Built-in support for `prefers-reduced-motion`, `color-scheme: light dark`, and semantic HTML preservation.

## 📁 Project Structure

- `reset.css` - The unopinionated minimal layer for establishing safe platform defaults.
- `reboot.css` - The developer-friendly, variable-driven base styles for web applications.
- `research.md` - In-depth research analysis, comparative evaluations of legacy resets, and technical rationale for all modern CSS design decisions.

## 🛠️ Usage

Import the layers at the very top of your main stylesheet to establish your foundation before adding component or utility styles:

### CDN
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/LewisCrouch/baselinecss@v2026-10/reset.min.css" integrity="sha384-nJ2fycD5UFWdGX5I0l/5WIGTXJFqf1mKOyVqgR0G23xjwigeYfO4i2YuRMbZF8jo" crossorigin="anonymous">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/LewisCrouch/baselinecss@v2026-10/reboot.min.css" integrity="sha384-kvs48MxRJY8t6ex8fr7PDV/cjyYODjz9XwNup1+X3Eo7HCiAVDBIXlCNB7/UB8Xl" crossorigin="anonymous">
```

### Define layer order in your project's main CSS file
```css
/* Define ALL layers in order (lowest priority to highest) */
/* BaselineCSS uses reset, theme and base. */
@layer reset, theme, base, components, utilities;

/* Write your custom styles */
@layer components {
  /* ... */
}

@layer utilities {
  /* ... */
}
```

## 📚 Background & Research

This project was built on an extensive synthesis of 2024–2026 CSS Baseline standards, drawing inspiration from industry leaders while intentionally abandoning legacy technical debt (like destructive resets and hardcoded pixel values). 

For a complete line-by-line technical rationale, please read the included [research.md](./research.md).
