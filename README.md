# Binding

A study of color through perception, interaction, and transition.

## Overview
**Binding** is a web-based project built with HTML and CSS in response to three texts that explore color as an experience. The site translates conceptual ideas about color into an interactive system, exploring how color influences the way we perceive, compare, and interpret information.

## Context

This project serves as the final assignment for **Typography and Interaction 1**. The website responds to three readings:

* Everyday Color Theory — Cortney Cassidy
* Interaction of Color (Ch. 4–5) — Josef Albers
* Gradients — Daisy Alioto

Together, these texts present a layered study of color: how it behaves, how it deceives, and how it evolves within contemporary visual culture. Binding unifies these perspectives into a cohesive, system-driven web experience.

## Systems

### Color System

Color acts as the primary organizing principle across the site. A restrained layout—defined by lines, geometric forms, and technical structure—supports this emphasis.

The site includes light and dark modes with intentionally paired palettes:

* Dark Mode: warm hues (red, orange, yellow)
* Light Mode: complementary cool hues (green, blue, purple)

Although six colors are used overall, each warm hue corresponds to its complementary cool hue:

* Red ↔ Green
* Orange ↔ Blue
* Yellow ↔ Purple

Warm colors were placed in dark mode to increase contrast and improve yellow’s legibility.


### Conceptual Titles

Each text is assigned a thematic title to reinforce its conceptual role:

* Perception — Everyday Color Theory
* Interaction — Interaction of Color
* Transition — Gradients

These titles help frame each article within the larger system of color experience.


### Geometric Motifs

Each article is visually represented by a basic shape:

* Triangle → Perception
  * Implemented as an inline SVG Penrose triangle to evoke perceptual illusion.

* Square → Interaction
  * Two animated squares illustrate relational color behavior, referencing Albers’ teachings.

* Circle → Transition
  * Rendered with a gradient fading to transparency to imply movement and atmospheric change.

Each article “owns” a single color to maintain clarity and cohesion. Rather than using multicolored gradients, the gradient-to-transparent circle keeps the system simple and unified.


### Typographic Emphasis

Curly brackets `{}` are used within articles to call out key terms, functioning as system-level emphasis markers across the texts.

## Media Constraints

The assignment permitted only two images total:

1. Inline SVG: used to create the Penrose triangle
2. Single <img> asset: used on the Home page alongside the Colophon, containing the three shapes and primary colors used throughout the system

This limitation pushed the project toward CSS-driven illustration and structural consistency.

## Challenges

Designing a consistent, responsive system across multiple breakpoints came with several challenges:

* **Achieving cohesive color balance across modes**
  * Ensuring warm hues still read as “dark mode” and cool hues still read as “light mode” without overpowering content.

* **Managing high-impact header layouts**
  * Large, side-by-side intro sections introduced visual weight; desaturating colors helped maintain readability and flow.

* **Recreating Albers-inspired illustrations**
  * Translating Interaction of Color diagrams into pure CSS required careful layering and spacing.

* **Building mobile-first, then scaling upward**
  * Aligning grids, consistent spacing, and text flow meant constant refinement across small, medium, and large breakpoints.

## Technical Features

### HTML + CSS Architecture

* Semantic HTML for clear structure and accessibility
* DRY CSS with nesting for maintainability and reduced repetition
* CSS custom properties `(--variables)` for colors, spacing, and mode toggling
* Mode-aware design using `prefers-color-scheme` to automatically switch between light and dark modes

### Layout

* CSS Flexbox for navigation, card layouts, and element positioning
* CSS Grid to maintain consistent text alignment and layout stability across varying header lengths
* Max-inline-size constraints for improved readability at wider viewports
* Position: sticky for desktop section headings and colophon positioning

### Interactions + Visual Styling

* Animated geometric shapes built with CSS (e.g., interacting squares)
* Gradient-to-transparent circle using radial-gradient
* SVG-based Penrose triangle constructed with inline vector geometry
* Curly-brace annotations using pseudo-selectors and typographic styling
* Custom hover states that shift hues depending on light/dark mode
* Mobile-first typography scale that adapts across breakpoints

### Accessibility Considerations

* Warm hues chosen for dark mode to increase yellow’s readability
* Consistent alignment systems to support clear reading order
* High-contrast states for interactive elements
