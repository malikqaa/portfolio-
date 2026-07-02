# Qammar Abbas — Portfolio Website

[![Live Site](https://img.shields.io/badge/Live-qammarportfolio--two.vercel.app-00d4ff?style=flat-square)](https://qammarportfolio-two.vercel.app/)
[![Made with HTML CSS JS](https://img.shields.io/badge/Built%20with-HTML%2FCSS%2FJS-1a2340?style=flat-square)]()
[![Deployed on Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-000000?style=flat-square&logo=vercel)](https://vercel.com/)

My personal portfolio — built from scratch with plain HTML, CSS, and JavaScript. No frameworks, no build step, no dependencies to install. I wanted something fast, fully mine, and easy to tweak whenever I add a new project or update my experience.

**Live site:** https://qammarportfolio-two.vercel.app/

---

## Why I built it this way

I'm a BS Statistics (Data Science) student who works across data science, ML, and full-stack development, and I wanted a portfolio that reflected that — clean, dark, a little technical in its visual language, but still fast and dependency-free. Rather than reaching for a template or a framework, I built the whole thing with vanilla HTML/CSS/JS so I could control every animation, every transition, and every pixel myself, and so anyone looking at the repo can see exactly how it works without digging through node_modules.

## Features

- **Custom cursor & scroll progress bar** — a small interactive touch that makes the site feel less static
- **Animated hero section** with a canvas-based particle network background and a typewriter effect cycling through my roles
- **Scroll-triggered reveal animations** using the Intersection Observer API — sections, skill bars, and stat counters animate in as you scroll, not on page load
- **Projects section** showcasing my featured work, including:
  - **MaternaRisk AI** — an ML-based maternal health risk classifier (XGBoost, Scikit-learn, deployed as a Streamlit app)
  - **RevenuePulse** — a multi-page Power BI analytics dashboard (e-commerce sales, customer analytics, marketing ROI)
- **Skills section** with animated proficiency bars grouped by category
- **Experience timeline** covering my internships, freelance work, and leadership roles
- **Services section** outlining what I offer (dashboard development, full-stack builds, data visualization, etc.)
- **Testimonials carousel**
- **Contact section** with a client-side form and direct links to email, LinkedIn, GitHub, and a downloadable CV
- **Fully responsive** — collapses into a mobile-friendly layout with a slide-out nav menu below 900px
- **Zero dependencies** — no npm install, no bundler, just open `index.html` or deploy as-is

## Tech Stack

| Layer | What I used |
|---|---|
| Structure | Semantic HTML5 |
| Styling | Vanilla CSS3 — custom properties (CSS variables) for theming, CSS Grid & Flexbox for layout, no framework |
| Interactivity | Vanilla JavaScript (ES6+) — no jQuery, no React, no build tools |
| Animations | `IntersectionObserver` for scroll reveals, `requestAnimationFrame` for the particle canvas and cursor tracking |
| Fonts | [Syne](https://fonts.google.com/specimen/Syne), [DM Sans](https://fonts.google.com/specimen/DM+Sans), [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) via Google Fonts |
| Hosting / CI | [Vercel](https://vercel.com/) — auto-deploys on every push to `main` |

I intentionally kept this dependency-free. The goal was a portfolio that loads fast, has no supply-chain surface area to worry about, and that I can hand-edit at 1 a.m. without remembering a framework's quirks.

## Project Structure

```
.
├── index.html              # Everything lives here — markup, <style>, and <script>
├── Qammar_Abbas_Professional_Cv.pdf   # Downloadable CV linked from the footer
└── README.md
```

I kept the CSS and JS inline in a single `index.html` on purpose — for a one-page portfolio of this size, splitting it into multiple files added more overhead than it saved. If the site grows (a blog, more project pages, etc.), I'll modularize it then.

## Running It Locally

No build step, no installs — just open the file:

```bash
git clone https://github.com/malikqaa/qammarportfolio.git
cd qammarportfolio
open index.html   # or just double-click it / drag it into a browser
```

If you want live-reload while editing, any static server works fine, e.g.:

```bash
npx serve .
# or
python3 -m http.server 8000
```

## Deployment

The site is deployed on **Vercel**, connected directly to this repository. Every push to `main` triggers an automatic build and deploy — there's no manual deploy step on my end. If you fork this repo, you can spin up your own instance in a couple of minutes by importing it into Vercel and pointing it at `index.html`.

## Updating Content

Since everything lives in one file, updating the site is straightforward:

- **New project** → duplicate a `.project-card` block inside `#projects`, swap the image, title, description, tech badges, and links
- **New skill** → add a `.skill-item` inside the relevant `.skill-cat` block with a `data-w` percentage
- **New experience entry** → add a `.exp-card` inside `#experience`
- **Resume update** → replace `Qammar_Abbas_Professional_Cv.pdf` and keep the filename the same (or update the `download` link in the footer)

## What's Next

A few things on my list for future iterations:
- Splitting out the CSS/JS into separate files as the site grows
- Adding a lightweight blog section for write-ups on projects like MaternaRisk AI
- Optimizing image delivery (moving embedded/base64 images to optimized external assets)
- Adding light mode as an option alongside the current dark theme

## About Me

I'm Qammar Abbas — a BS Statistics (Data Science) student at COMSATS University Islamabad (Lahore Campus), currently working as an ML Engineer Intern at FlyRank and interning at the Pakistan Bureau of Statistics. I build things across data science, machine learning, and full-stack web development, and I'm working toward eventually founding my own software house, DevOrbit.

- 🌐 Portfolio: [qammarportfolio-two.vercel.app](https://qammarportfolio-two.vercel.app/)
- 💼 LinkedIn: [linkedin.com/in/qammar-abbas-298374346](https://www.linkedin.com/in/qammarabbas-dev)
- 📧 Email: qammarabbas437@gmail.com
- 🐙 GitHub: [@malikqaa](https://github.com/malikqaa)

## License

This project is open for reference and inspiration. If you fork or reuse parts of the design, a credit back to this repo is appreciated but not required.

---

<p align="center">Built with care, one section at a time.</p>
