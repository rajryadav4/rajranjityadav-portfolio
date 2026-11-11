# Raj Ranjit Yadav – Portfolio Website

Personal portfolio for Raj Ranjit Yadav (MS CS @ Northeastern, Seattle).
Live at https://rajranjityadav.netlify.app, hosted on Netlify. Source: github.com/rajryadav4/rajranjityadav-portfolio
(private). Once the repo is linked in Netlify, every push to `main` deploys, so "publish" means commit + push.

## Structure
- `index.html`: the entire site. HTML, CSS (in `<style>`), and JS (in `<script>` at the bottom) all live in this one file. No build step, no framework.
- `assets/raj_ranjit_yadav_resume.pdf` (lowercase): the resume every "Resume" link opens. To update the resume, replace this file and keep the same file name. Master copy: `~/Documents/Resumes/universal/Raj_Ranjit_Yadav_Resume.pdf`.
- `assets/projects/`: real result screenshots shown in the featured build cards (`.shot` frames). Only use genuine output, with no personal data, company names from applications, or machine names.
- There is no `og-image.png` yet, and no `og:image` tag.

## Page sections (in order, by id)
`#top` hero (headline, counting stats, interactive terminal, "Current quest" card) →
skills marquee → `#story` (01) → `#work` (02) → `#projects` (03) → `#skills` (04) →
`#education` (05) → `#hobbies` (06) → `#contact` CTA → footer.

## Interactive terminal (hero)
- The markup is in `.portrait` > `.term`; buttons are in `#termKeys` with `data-cmd` attributes.
- Command outputs are in the `commands` object in the "Interactive terminal" script block.
- To add a command, add a button with a new `data-cmd` and a matching key in `commands`.
- Fun facts rotate from the `facts` array.
- The intro sequence auto-runs `whoami` and then `python automate.py` on page load.

## Style rules
- Colors are CSS variables on `:root`, with dark-mode overrides under `@media (prefers-color-scheme: dark)` and `:root[data-theme="dark"]`. Always add new colors as variables in all three places.
- Fonts: Plus Jakarta Sans (body and headings) and Instrument Serif italic (the gradient accent words, `em.serif`).
- Accent gradient: `--grad` (blue `--accent` to purple `--accent2`).
- Respect `prefers-reduced-motion` for any new animation.
- Keep the site mobile-friendly. Check that nothing scrolls sideways at a 390px width.

## Content rules
- All facts must match the resume (`assets/raj_ranjit_yadav_resume.pdf`). Never invent metrics, employers, or results.
- Exception: Job Hunter (featured build 02) is not on the resume yet. Its numbers come from its own README and dashboard (15+ sources, 9,476 postings scanned in the 10 Nov 2026 run, 75%+ ATS check). Its repo is private, so the card links to a demo request and to Job Match Assistant.
- Key verified numbers: 300+ documents migrated, 1,000+ attributes mapped, 97% faster validation (5–6 hours → ~10 minutes), 750+ job postings ingested, 700+ jobs ranked, 4.0 GPA, 3,000+ expo attendees, 30+ volunteers.
- The phone number is intentionally left off the site.
- Featured builds link to their public repos (preMORTEM, job-match-assistant). Small builds still point to the GitHub profile (github.com/rajryadav4).

## Workflow
1. Make the change.
2. Preview by opening `index.html` in a browser (`open index.html` on macOS), or `python3 -m http.server` in this folder.
3. Commit with a clear message and `git push`. Netlify deploys in about a minute.
