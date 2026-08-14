# Vaazhai 🍃

A single-file, animated landing page for **Vaazhai**, a fictional Tamil Nadu banana-leaf meal restaurant. Built entirely with vanilla HTML, CSS, and JavaScript — no frameworks, no build step, no dependencies beyond two Google Fonts.

## What it is

A pure CSS/SVG-style illustration of a full banana-leaf meal (rice, sambar, rasam, poriyal, kootu, vada, payasam, pickle, curd, papadam, banana) rendered as layered `div`s and gradients, wrapped in a scrollable storytelling page: hotel history, today's specials, a step-by-step "how it's served" animation, and a full menu.

## Features

- **Illustrated banana leaf hero** — every dish is a hand-tuned CSS shape (radial gradients, clip-paths, box-shadows), procedurally grown leaf veins, and looping steam/particle animations.
- **Tap-to-identify dishes** — click any item on the leaf for a floating tooltip with its Tamil + English name.
- **Scroll-triggered plating animation** — the "How it's Served" section replays the meal being laid out step by step (`IntersectionObserver` + CSS keyframes), with a synced step list and a replay button.
- **Bilingual copy** — Tamil script paired with English throughout (headings, dish names, captions, menu).
- **Full responsive layout** — hero leaf, "legacy" photo plaques, specials cards, assembly diagram, and menu grid all reflow for mobile.
- **Accessibility touches** — respects `prefers-reduced-motion` by disabling steam, pulses, and the plating animation.
- **Gen Z-flavored copy pass** — playful microcopy in the hint text, section descriptions, special tags, and footer (see below).

## File structure

This is a single self-contained file:

```
vaazhai.html   ← everything: <style>, markup, and <script> in one document
```

No separate CSS/JS files, no images (all visuals are CSS-generated), no external scripts beyond the Google Fonts stylesheet link.

## How to use it

1. Open `vaazhai.html` directly in any modern browser (double-click it, or drag it into a browser tab) — no server or build step required.
2. To host it, upload the single file to any static host (GitHub Pages, Netlify, Vercel, S3, etc.) and point your domain at it.

## Customizing

- **Colors / theme**: all core colors (wood tones, leaf greens, gold accents, dish colors) are defined as CSS custom properties in `:root` at the top of the `<style>` block — change them there to re-theme the whole page.
- **Fonts**: `Yatra One` (display) and `Mukta` / `Catamaran` (body) are loaded via the Google Fonts `<link>` in `<head>`.
- **Menu items & prices**: edit the `<ul>` lists inside `.menu-grid` under the `MENU` section near the bottom of the body.
- **Specials**: each `.special-card` under the `SPECIALS` section has a tag, name (English + Tamil), blurb, and price — duplicate a card to add more.
- **Assembly steps**: the `#miniLeaf` step items and the matching `#stepsList` entries share timing via `--d` (CSS delay) and `data-t` (JS timeout in ms) — keep these in sync if you add/remove/reorder steps.

## Browser support

Uses modern CSS (`clip-path`, `aspect-ratio`, CSS custom properties, `background-clip: text`) and `IntersectionObserver`. Works in current Chrome, Firefox, Safari, and Edge. No polyfills included.

## Notes

This is a fictional/demo restaurant page — content (hours, prices, address) is illustrative, not a real business.
