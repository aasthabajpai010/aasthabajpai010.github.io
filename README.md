# Aastha Bajpai — Portfolio Website

A modern, responsive personal portfolio for **Aastha Bajpai** — MCA student at NIT Jamshedpur and Full-Stack (MERN) Developer.

## Features

- **Modern Design**: Clean teal/cyan gradient theme with smooth scroll animations
- **Dark / Light Mode**: Toggle button in the navbar, preference saved via `localStorage`, auto-detects system preference on first visit
- **Fully Responsive**: Desktop, tablet, and mobile layouts
- **Sections**: Hero, About, Skills, Experience, Projects, Achievements, Education, Contact
- **Interactive Elements**: Smooth-scroll navigation, scroll-to-top button, mobile hamburger menu, animated cards, working resume download
- **Real Project Showcase**: AI-Integrated College ERP System, BhashaShikho, House Price Prediction System — each linked to its real GitHub repo
- **Achievements Section**: NIMCET AIR 519, Postman certification, HackerRank/LeetCode/GeeksforGeeks profiles

## Tech Stack

- **HTML5** — Semantic markup
- **CSS3** — Grid, Flexbox, custom properties, animations
- **JavaScript** — Vanilla JS, no frameworks
- **Google Fonts** — Inter & Playfair Display

## Project Structure

```
portfolio-website/
│
├── index.html                      # Main HTML file
├── styles.css                      # All CSS styles
├── script.js                       # JavaScript functionality
├── Aastha_Bajpai_Resume.pdf        # Resume (linked from the Download Resume button)
├── README.md                       # This file
├── .gitignore
└── assets/
    └── images/
        ├── profile-pic.jpg         # Profile photo
        └── nit-logo.jpg            # NIT Jamshedpur logo (background element)
```

## Getting Started

### Quick Open

Just double-click `index.html` to open it in your browser. No build step, no dependencies.

### Using a Local Server (recommended — avoids local file/image quirks)

```bash
# Python 3
python -m http.server 8000

# Node.js
npx http-server
```

Then visit `http://localhost:8000`.

### VS Code Live Server

Install the **Live Server** extension, right-click `index.html` → **Open with Live Server**.

## Images

Both images are already in place in `assets/images/`:
- `profile-pic.jpg` — profile photo, displayed in a circular frame in the hero section
- `nit-logo.jpg` — NIT Jamshedpur logo, shown as a subtle grayscale background element (note: it's a `.jpg`, not `.png` — `styles.css` is wired to match)

To swap either image, just replace the file in `assets/images/` with a new one of the same name — no code changes needed.

## Deploying to GitHub Pages

1. Create a new **public** GitHub repository (e.g. `portfolio-website`).
2. Upload all files in this folder — `index.html`, `styles.css`, `script.js`, `Aastha_Bajpai_Resume.pdf`, `README.md`, `.gitignore`, and the `assets/` folder.
3. In the repo, go to **Settings → Pages**, set **Source** to the `main` branch, root folder, and save.
4. Your site goes live at:
   ```
   https://aasthabajpai010.github.io/REPO_NAME/
   ```

### Using Git from the command line

```bash
cd portfolio-website
git init
git add .
git commit -m "Update portfolio: real projects, skills, achievements, dark mode"
git remote add origin https://github.com/aasthabajpai010/REPO_NAME.git
git branch -M main
git push -u origin main
```

## Known Gaps / To-Do

- [ ] Deploy the three featured projects (ERP, BhashaShikho, House Price Predictor) and replace the disabled "Live Demo" buttons with real links — the resume's current live links point to a placeholder `example.com` domain and need updating in both places
- [ ] Connect the contact form to a real backend or a service like Formspree/EmailJS (it's currently frontend-only and just validates + resets on submit)
- [ ] Keep Experience section end-dates in sync with the resume going forward

## Customization

### Colors

Edit the CSS variables at the top of `styles.css`:

```css
:root {
    --primary-color: #0f766e;
    --secondary-color: #14b8a6;
    --accent-color: #06b6d4;
}
```

### Dark Mode

Dark theme colors live in the `[data-theme="dark"]` block right under `:root` in `styles.css` — edit `--bg-white`, `--bg-light`, `--text-dark`, etc. there to adjust the dark palette. The toggle logic (click handler + `localStorage` persistence) is in `script.js` under "Theme Toggle (Dark/Light Mode)", and the no-flash-on-load detection script sits inline in `index.html`'s `<head>`.

### Content

- **Skills**: edit the `.skill-card` items in the Skills section of `index.html`
- **Projects**: edit the `.project-card` items in the Projects section
- **Achievements**: edit the `.education-card` items inside `<section id="achievements">`
- **Experience**: edit the `.timeline-item` entries in the Experience section

## Browser Support

Chrome, Firefox, Safari, Edge (latest versions), and mobile browsers (iOS Safari, Chrome Mobile).

## Author

**Aastha Bajpai**
- Email: 2024aspire68@gmail.com
- LinkedIn: [aastha-bajpai-6696992ba](https://www.linkedin.com/in/aastha-bajpai-6696992ba)
- GitHub: [aasthabajpai010](https://github.com/aasthabajpai010)
- Institute: NIT Jamshedpur
- Programme: MCA, 2024 – 2027

---

**Built with HTML, CSS & JavaScript**