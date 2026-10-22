# BaselineCSS v2026.10

*Disclaimer: This project was created using AI (Gemini Deep Research).*

A definitive, dual-layer CSS foundation optimized for modern web development in 2026. This project provides both an unopinionated **Reset** to normalize cross-browser quirks and an opinionated **Reboot** to establish a robust, fluid, and accessible baseline for modern design systems.

## 🚀 Features

- **Cascade Layers (`@layer`)**: Built natively on `@layer reset` and `@layer base` to ensure zero specificity conflicts with your component CSS.
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

```css
/* main.css */
@import url('reset.css') layer(reset);
@import url('reboot.css') layer(base);

/* Your custom layers and styles go here */
@layer components, utilities;
```

## 📚 Background & Research

This project was built on an extensive synthesis of 2024–2026 CSS Baseline standards, drawing inspiration from industry leaders while intentionally abandoning legacy technical debt (like destructive resets and hardcoded pixel values). 

For a complete line-by-line technical rationale, please read the included [research.md](./research.md).
