# Media Production Website

## Overview

A professional media production company website built with advanced HTML5 and CSS3. The site showcases video production, audio recording, and photography services across four pages. Originally a starter codebase with 58+ errors, it has been debugged, fixed, and enhanced with semantic HTML, CSS Grid, Flexbox layouts, animations, and full form validation.

## Issues Found

The starter code contained errors across all 5 files:

**HTML (all 4 pages):**
- Generic `<div>` elements used instead of semantic tags (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`)
- Missing metadata: `lang`, `charset`, `viewport`, `description`
- All `<img>` tags missing `alt` attributes
- No `<figure>` or `<figcaption>` on any images

**media.html:**
- Video missing `controls` and fallback content
- Second video, audio element, and iframe all missing

**contact.html:**
- Form had only 3 text inputs, no labels, no validation
- Missing radio buttons, checkboxes, select, date, number inputs
- No fieldset grouping

**styles.css:**
- No Flexbox or Grid layouts
- No pseudo-classes, combination selectors, or attribute selectors
- No transforms, transitions, or animations
- Poor colour contrast in hero section
- No responsive design

## Fixes and Implementations

All 58+ errors were identified and resolved. Every `<div>` wrapper was replaced with the correct semantic element. Complete metadata was added to all pages. All images were given `alt` attributes and wrapped in `<figure>`/`<figcaption>`.

## Flexbox Layouts

Two distinct Flexbox layouts were implemented:
1. **Navigation bar** (`.main-nav`): `flex-direction: row`, `justify-content: flex-start`, `align-items: center`, `flex-wrap: wrap`
2. **Services section** (`.services-cards`/`.services-flex`): `flex-direction: row`, `justify-content: space-evenly`, `align-items: stretch`, `flex-wrap: wrap`

Both collapse to `flex-direction: column` on mobile via media query.

## CSS Grid Layout

The portfolio gallery and testimonials section use CSS Grid:
- `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))`
- `grid-template-rows: auto`
- `gap: 20px`
- Responsive: collapses to single column at 768px

## Selectors and Pseudo-classes

**Selector types (6):** element, class, ID, attribute, descendant, child combinator

**Pseudo-classes (6):** `:hover`, `:focus`, `:nth-child(even)`, `:first-child`, `:last-child`, `:not()`

**Combination selectors (3):** `.site-header > h1` (child), `h2 + p` (adjacent sibling), `input[required]:focus` (attribute + pseudo-class)

## Animations, Effects, Transforms, and Transitions

- **Text effect:** `text-shadow` on hero heading
- **Transforms:** `translateY(-5px)` on service cards, `scale(1.03)` on grid items, `rotate(-3deg)` on hero decoration
- **Transitions:** service card hover (transform, box-shadow), form input focus (border-color, box-shadow)
- **Keyframe animation:** `fadeInDown` on hero heading

## Accessibility Improvements

- All images have descriptive `alt` attributes
- All form inputs have associated `<label>` elements
- Form uses `<fieldset>` and `<legend>` for grouping
- Focus states on all interactive elements
- Proper colour contrast on hero section

## Cross-Browser Compatibility

Tested in Google Chrome and Mozilla Firefox. No browser-specific CSS was required. All HTML validated through W3C Markup Validator. All CSS validated through W3C CSS Validator.

## How to View Locally

1. Clone the repository
2. Open `index.html` in any modern browser
3. Navigate between pages using the top navigation bar
4. No server or build tools required

## Known Issues

- Form submits to `#` as no backend exists. Connect to a server or form service for real submissions.

## Screenshots

| Screenshot | File |
|------------|------|
| Homepage desktop | `screenshots/homepage-desktop.png` |
| Homepage mobile | `screenshots/homepage-mobile.png` |
| About page mobile | `screenshots/about-mobile.png` |
| Form validation | `screenshots/form-validation.png` |
| Animation demo | `screenshots/animation-demo.gif` |
| Media elements | `screenshots/media-elements.png` |
| Flexbox layout | `screenshots/flexbox-layout.png` |
| Grid layout | `screenshots/grid-layout.png` |
| Chrome browser | `screenshots/browser-chrome.png` |
| Firefox browser | `screenshots/browser-firefox.png` |

## Reflection

The biggest challenge was debugging the form on `contact.html`. The original had no labels, wrong input types, and zero validation. Rebuilding it with 10 input types, 3 fieldsets, and proper validation attributes required careful planning to meet all requirements without JavaScript.

Implementing CSS Grid with `auto-fit` and `minmax` for the portfolio gallery was straightforward but required testing at multiple breakpoints to confirm the responsive behaviour worked correctly.

The Flexbox navigation was simple to implement but needed `flex-wrap` to handle smaller screens properly. Using a media query to switch `flex-direction` to `column` on mobile solved the layout issue cleanly.

Balancing the number of required CSS features (selectors, pseudo-classes, transforms, transitions, animations) without overcomplicating the stylesheet was important. The goal was to meet every requirement while keeping the CSS maintainable and close to the original styling.