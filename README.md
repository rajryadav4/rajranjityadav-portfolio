# rajranjityadav.netlify.app

[![Netlify Status](https://api.netlify.com/api/v1/badges/efa92958-3434-446a-be4f-d4e2ac8520e4/deploy-status)](https://app.netlify.com/projects/rajranjityadav/deploys)

Source for Raj Ranjit Yadav's portfolio: **https://rajranjityadav.netlify.app**

One static page, no build step. Every push to `main` deploys to Netlify.

| Path | What it is |
|---|---|
| `index.html` | The whole site: HTML, CSS and JS in one file |
| `assets/raj_ranjit_yadav_resume.pdf` | The resume every "Resume" link opens |
| `assets/projects/` | Real result screenshots shown on the project cards |
| `netlify.toml` | Deploy settings (publish this folder, no build) |

Preview locally:

```bash
python3 -m http.server 8790
```

Then open http://localhost:8790.
