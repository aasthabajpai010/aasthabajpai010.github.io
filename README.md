# Aastha Bajpai — Portfolio Website

A modern, responsive personal portfolio for **Aastha Bajpai** — MCA student at NIT Jamshedpur and Full-Stack (MERN) Developer.

## Features

- **Professional Redesign**: Space Grotesk typography, electric teal–purple palette, dot-grid hero background
- **Dark / Light Mode**: Toggle button in the navbar, preference saved via `localStorage`, auto-detects system theme on first visit
- **Fully Responsive**: Desktop, tablet, and mobile layouts
- **Sections**: Hero, About, Skills, Experience, Projects, Achievements, Education, Contact
- **Skill Pills**: Technologies grouped by category (Languages / Frontend / Backend / Databases / CS Fundamentals / Tools) — clean pill layout instead of cards
- **Real Project Showcase**: AI-Integrated College ERP System, BhashaShikho, House Price Prediction System — each linked to its real GitHub repo
- **Achievements Section**: NIMCET AIR 519, Postman certification, HackerRank / LeetCode / GeeksforGeeks profiles
- **Working Resume Download**: Directly downloads `Aastha_Bajpai_Resume.pdf`

## Tech Stack

- **HTML5** — Semantic markup
- **CSS3** — Grid, Flexbox, CSS custom properties, animations
- **JavaScript** — Vanilla JS, no frameworks
- **Google Fonts** — Space Grotesk (headings) + Inter (body)

## Project Structure

```
PORTFOLIO-WEBSITE/
│
├── .github/
├── assets/
│   └── images/
│       ├── logo.jpg              # NIT Jamshedpur logo (subtle hero background)
│       └── profile-pic.jpg       # Profile photo in hero section
├── .gitignore
├── Aastha_Bajpai_Resume.pdf      # Linked from Download Resume button
├── index.html                    # Main HTML file
├── package.json                  # Only present if http-server was installed locally
├── README.md                     # This file
├── script.js                     # JavaScript — nav, dark mode, scroll, form
└── styles.css                    # All CSS styles
```

## Getting Started

### Quick Open

Double-click `index.html` to open it in your browser. No build step, no dependencies.

### Using a Local Server (recommended)

```bash
# Node.js
npx http-server
```

Then visit `http://localhost:8080`.

### VS Code Live Server

Install the **Live Server** extension → right-click `index.html` → **Open with Live Server**.

## Images

Both images are in `assets/images/` and already wired up in the code:

- `profile-pic.jpg` — displayed in the hero section (rounded rectangle frame)
- `logo.jpg` — NIT Jamshedpur logo, shown as a subtle grayscale background element in the hero

To swap either image, replace the file with the same filename — no code changes needed.

## Deploying to GitHub Pages

1. Push all files to a **public** GitHub repository.
2. Go to **Settings → Pages**, set Source to `main` branch, root folder, and save.
3. Your site goes live at:
   ```
   https://aasthabajpai010.github.io/REPO_NAME/
   ```

### Git commands to push updates

```bash
cd portfolio-website
git add .
git commit -m "Redesign: Space Grotesk, skill pills, new hero, improved dark mode"
git push
```

## Customization

### Colors

CSS variables are at the top of `styles.css`:

```css
:root {
    --primary: #06D6A0;      /* electric teal */
    --secondary: #8B5CF6;    /* purple */
    --primary-dark: #04B589; /* teal hover state */
}
```

Dark theme overrides are in the `[data-theme="dark"]` block right below.

### Dark Mode

Toggle logic (click handler + `localStorage`) is in `script.js` under **"Theme Toggle"**. The no-flash-on-load detection is an inline script in `index.html`'s `<head>`.

### Content

| What to update | Where |
|---|---|
| Skills | `.skill-pill` items inside `.skill-group` divs in `index.html` |
| Projects | `.project-card` blocks in the Projects section |
| Achievements | `.education-card` blocks inside `<section id="achievements">` |
| Experience | `.timeline-item` entries in the Experience section |
| Live Demo links | `href` on `.project-link` anchors in each project card |

## Known Gaps / To-Do

- [ ] Deploy ERP, BhashaShikho, House Price Predictor and replace disabled **Live Demo** buttons with real URLs
- [ ] Connect contact form to Formspree or EmailJS (currently frontend-only)
- [ ] Delete unused `me.jpg` from `assets/images/` if not needed

## Browser Support

Chrome, Firefox, Safari, Edge (latest), iOS Safari, Chrome Mobile.

## Author

**Aastha Bajpai**
- Email: 2024aspire68@gmail.com
- LinkedIn: [aastha-bajpai-6696992ba](https://www.linkedin.com/in/aastha-bajpai-6696992ba)
- GitHub: [aasthabajpai010](https://github.com/aasthabajpai010)
- Institute: NIT Jamshedpur · MCA 2024 – 2027

---

**Built with HTML, CSS & JavaScript**
