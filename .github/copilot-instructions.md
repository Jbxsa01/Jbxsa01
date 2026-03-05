# GitHub Copilot Instructions

## Repository Overview

This is a **GitHub profile repository** (`Jbxsa01/Jbxsa01`). GitHub automatically renders the `README.md` file from this repository as the public profile page for the user [@Jbxsa01](https://github.com/Jbxsa01).

### Repository Contents

| File | Purpose |
|------|---------|
| `README.md` | GitHub profile page — the only content displayed publicly on the profile |
| `Banner.png` | Profile banner image referenced at the top of `README.md` |
| `.github/copilot-instructions.md` | This file |

There is **no application code, build system, test suite, or package manager** in this repository. All changes are purely to the profile's Markdown presentation.

---

## Owner Profile

**Bjane Asmaa** — Full-Stack Engineer · AI Specialist · Tech Architect  
📍 Morocco | ✉️ bjane.asmaa1@gmail.com | 🌐 [bjaneasmaa.vercel.app](https://bjaneasmaa.vercel.app)

### Core Skills

- **Languages**: Python, JavaScript, TypeScript, Java, C#, PHP, C, C++, SQL
- **Frontend / Frameworks**: React, Node.js, TailwindCSS, Symfony, Django, Spring Boot, .NET MVC, JEE
- **AI / ML**: PyTorch, Hugging Face, Whisper AI, Coqui TTS, Cohere, NLLB, MT5, LangChain, RAG, OCR, NLP
- **Databases**: MySQL, PostgreSQL, MongoDB, MariaDB, PL/SQL, SQL Server
- **Mobile**: Android Native (Java), React Native, Flutter
- **DevOps / Cloud**: Docker, Kubernetes, AWS, Firebase, Git

### Featured Projects (documented in README)

| Project | Stack | Description |
|---------|-------|-------------|
| **Darija AI** | Python, NLP, ML, Speech Recognition | Speech transcription, translation & voice cloning for the Moroccan Darija dialect |
| **CHIFAA** | Python, AI, Healthcare, Telemedicine | AI-powered healthcare platform with symptom checking and secure consultations |
| **Medicare** | Full-Stack, Healthcare, Database | Medical records, appointments & patient management platform |
| **Fourniss'Ma** | Android, Java, Firebase, Geolocation | Mobile sales management app with geolocation support |
| **Plateforme Donation** | Spring Boot, Stripe, JPA/Hibernate | Gamified charity & digital donation platform |
| **SkyTravel** | PHP, Python, Travel Management | Business travel booking & tracking platform |
| **E-parking** | Spring, Java, MySQL, React | Smart online parking reservation with geo-recommendations |
| **Mobile AI (RAG + Assistant)** | RAG, LangChain, LSTM, Flutter | Mobile assistant with Retrieval-Augmented Generation & LangChain pipelines |
| **Application Web .NET MVC** | .NET MVC, C#, SQL Server, Entity Framework | Academic enterprise MVC web application |
| **Somagec IT Management** | Virtualization, System Config | IT infrastructure & fleet management application |

---

## How to Work on This Repository

### Making Changes

All meaningful changes are edits to `README.md`. There is no compilation, linting, or test step — validation is purely visual.

**To update the profile:**
1. Edit `README.md` directly.
2. Ensure any image referenced with a relative path (e.g., `Banner.png`) stays in the repository root.
3. Verify that all badge URLs (`img.shields.io`), GitHub stats cards, and external image links are syntactically correct before committing.

**To replace the banner image:**
- Replace `Banner.png` in the repository root.
- The `README.md` references it via an absolute raw GitHub URL:
  ```
  https://raw.githubusercontent.com/jbxsa01/jbxsa01/main/Banner.png
  ```
  Update this URL if the branch name or file name changes.

### README Structure

The `README.md` follows this top-level structure:

1. **Banner** — full-width image at the very top
2. **Title / Subtitle** — role headline and tagline
3. **Social badges** — LinkedIn, Portfolio, Gmail, GitHub
4. **GitHub stats badges** — followers, stars, profile views
5. **About Me** — narrative bio and core expertise bullet list
6. **Featured Projects** — HTML `<table>` grid, 3 columns, describing each project
7. **Tech Stack** — grouped badge lists (Languages, Frameworks, AI/ML, Databases, Mobile, Tools)
8. **GitHub Analytics** — stats card, top languages card, contribution graph
9. **Let's Connect** — collaboration table and full contact details

The file mixes standard Markdown with raw HTML `<div>` and `<table>` blocks for layout — this is intentional and required for the GitHub profile renderer.

### Style Conventions

- **Icons**: Uses `img.icons8.com/color/96/000000/<name>.png` for inline section icons (width="25" for headings, width="18" for list items, width="20" for project headings).
- **Badges**: Uses `img.shields.io` flat-square style for tech-stack badges and `for-the-badge` style for call-to-action buttons.
- **Colors**: Catppuccin Mocha palette for GitHub stats cards — `bg_color=1e1e2e`, `title_color=89b4fa`, `icon_color=f9e2af`, `text_color=cdd6f4`.
- **Language**: Section headers and badge labels are in English; project descriptions are written in French.
- **Horizontal rules** (`---`) separate every top-level section.

### Adding a New Project

1. Find the last `<tr>` inside the **Featured Projects** `<table>`.
2. If the last row has fewer than 3 `<td>` cells, add the new `<td>` there; otherwise add a new `<tr>` with a new `<td>`.
3. Follow the existing cell template:
   ```html
   <td width="33%">
     <h3><img src="https://img.icons8.com/color/96/000000/<icon>.png" width="20" alt="<Alt>"> Project Name</h3>
     <p><strong>One-line English subtitle</strong></p>
     <p>French description sentence.</p>
     <p><code>Tech1</code> • <code>Tech2</code> • <code>Tech3</code></p>
   </td>
   ```

### Adding a New Tech Badge

Append a new `![BadgeName](https://img.shields.io/badge/<Label>-<Color>?style=flat-square&logo=<logo>&logoColor=white)` line to the appropriate group in the **Tech Stack** section.

---

## Errors & Workarounds Encountered

| Symptom | Cause | Workaround |
|---------|-------|-----------|
| Banner image not rendering on profile | Raw GitHub URL uses `main` branch — will break if branch is renamed | Always use the `main` branch name in the raw URL, or update the URL after any branch rename |
| HTML layout not rendering in some Markdown viewers | GitHub profile README uses raw HTML `<div>`/`<table>` tags | This is intentional; the GitHub profile renderer supports raw HTML — do not convert to pure Markdown tables or the layout will break |
| GitHub stats cards occasionally show errors | Third-party Vercel-deployed services (`github-readme-stats-sigma-five`) can have downtime | No code change required; the cards self-recover. If persistent, switch to the official `github-readme-stats.vercel.app` endpoint |

---

## No Build, Test, or CI Pipeline

There are no GitHub Actions workflows, no `package.json`, no `requirements.txt`, and no test framework in this repository. Changes go live immediately on the profile once merged to the default (`main`) branch. Always visually verify the rendered README at `https://github.com/Jbxsa01` after merging.
