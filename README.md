# 🌌 Explore the Universe

An interactive tour of the solar system, built with **only HTML and CSS** — no JavaScript.

**[View live demo →](#)** *(add your GitHub Pages link here after deploying)*

*(Tip: add a screenshot or short screen-recording GIF here once it's live — it's what makes people actually click through on LinkedIn.)*

## Features

- **Animated starfield** — three depths of stars, each twinkling on its own timer, generated with pure CSS `box-shadow`
- **Orbiting solar system** — all eight planets circle the sun at proportionally different speeds, pause on hover, and show a name tooltip
- **Planet-by-planet explorer** — a focused card per planet with a CSS-only sphere, key stats, and a short fact
- **Previous / Next navigation** — cycles through all eight planets with no JavaScript, using the checkbox/radio-button hack
- **Dot indicators** — jump to any planet directly, with the active dot highlighted
- **Fully responsive** — reflows from desktop down to mobile
- **Accessible by default** — visible focus states on keyboard navigation, `prefers-reduced-motion` respected

## How it works

The whole thing runs on two CSS tricks:

1. **Orbits** — a rotating parent element (`@keyframes spin`) holds each planet, with a counter-rotating child (`@keyframes counter-spin`) so the planet dot and its label stay upright instead of tumbling.
2. **Navigation without JavaScript** — eight hidden `<input type="radio">` elements track which planet is "selected." Every `<label for="...">` acts as a button that changes the selection, and CSS sibling combinators (`~`) show or hide the matching planet card, nav labels, and dot based on which radio is `:checked`.

## Tech

- Semantic HTML5
- Modern CSS: custom properties, `@keyframes`, `backdrop-filter`, `color-mix()`, `aspect-ratio`, media queries
- [Fraunces](https://fonts.google.com/specimen/Fraunces) for display type, [Inter](https://fonts.google.com/specimen/Inter) for body/UI text
- Zero dependencies, zero build step — open `index.html` in a browser

## Running locally

```bash
git clone https://github.com/<your-username>/explore-the-universe.git
cd explore-the-universe
open index.html   # or just double-click the file
```

## Deploying to GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Set the source branch to `main` and folder to `/root`
4. Your site will be live at `https://<your-username>.github.io/explore-the-universe/`

---

Built as a pure CSS/HTML project to practice animation, layout, and interactivity without a single line of JavaScript.
