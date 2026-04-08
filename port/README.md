# Gursharan Brar — Personal Portfolio

Live at **[gursharan-brar.github.io/brar-portfolio](https://gursharan-brar.github.io/brar-portfolio)**

Single-file portfolio site. No frameworks, no build step, no dependencies — just `index.html`.

---

## Structure

Everything lives inside `index.html`:

| Block | Description |
|---|---|
| `<style>` | All CSS — custom properties, layout, animations |
| `#hero` | Full-screen section with canvas particle system |
| `#about` | Bio paragraph + stat cards grid |
| `#work` | Two skill cards (Infrastructure / ITSM & Dev) |
| `#projects` | 5-card project grid, BridgeUp spans 2 columns |
| `#experience` | Vertical timeline, scroll-animated dots |
| `#skills` | Two-row CSS marquee ticker, opposite directions |
| `#contact` | Links + resume download button |
| `<script>` | Cursor, navbar, canvas particles, IntersectionObserver |

---

## Design tokens

| Token | Value |
|---|---|
| Background | `#0a0e17` |
| Secondary BG | `#0f1422` |
| Text | `#eae5ec` |
| Muted text | `#8b8fa8` |
| Accent (teal) | `#5eead4` |
| Font | Geist (Google Fonts) |

---

## Deploy to GitHub Pages

```bash
# from the repo root
git add index.html README.md Gursharan_Brar_Resume.pdf
git commit -m "deploy portfolio"
git push origin main
```

Then in the repo **Settings → Pages**, set source to `main` branch, root `/`.

> Add `Gursharan_Brar_Resume.pdf` to the repo root so the resume download button works.

---

## Features

- **Particle canvas** — 90 teal particles with line-connection mesh and animated radial gradient blob
- **Custom cursor** — teal dot + lagging ring, scales on hover, hidden on touch devices
- **Scroll animations** — `IntersectionObserver` triggers fade-up and fade-left per element
- **Timeline** — dots light up teal as each entry scrolls into view
- **Skills ticker** — pure CSS `animation: translateX`, two rows scrolling opposite directions
- **Responsive** — single-column layout below 768 px, hamburger nav
- **No JS libraries** — vanilla only; Google Fonts is the sole external resource
