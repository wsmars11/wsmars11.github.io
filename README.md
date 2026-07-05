# Your Finance Portfolio Site

Built with [Astro](https://astro.build). Static, fast, free to host on GitHub Pages.

## 1. Preview it locally

You'll need [Node.js](https://nodejs.org) (v18+) installed.

```bash
npm install
npm run dev
```

Open the URL it prints (usually `http://localhost:4321`).

## 2. Personalize the content

Open `src/pages/index.astro` and edit the top section:

- `NAME`, `TITLE`, `TAGLINE` — your header info
- `ledgerLines` — the four quick stats near the top
- `experience` — your roles, in reverse chronological order

Further down in the HTML:

- The three paragraphs under **"Why Finance"** — replace with your own pivot story
- The `mailto:` and LinkedIn links in the **Contact** section
- Swap `public/resume/README.txt` for your real resume, named `resume.pdf`,
  and update the `href` in the "Download résumé" button to `/resume/resume.pdf`

## 3. Deploy to GitHub Pages

**Option A — root site (recommended), e.g. `yourname.github.io`**

1. Create a GitHub repo named exactly `your-username.github.io`
2. Push this project to it:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/your-username/your-username.github.io.git
   git push -u origin main
   ```
3. In the repo on GitHub: **Settings → Pages → Source → GitHub Actions**
4. Wait ~1 minute, then visit `https://your-username.github.io`

The included `.github/workflows/deploy.yml` will auto-build and deploy on every push to `main`.

**Option B — project site**, e.g. `yourname.github.io/portfolio`

Same as above, but:
1. Name the repo anything you like, e.g. `portfolio`
2. Before pushing, edit `astro.config.mjs` and uncomment the `site`/`base` lines, filling in your username and repo name
3. Same Pages settings as above

## 4. Custom domain (optional)

Settings → Pages → Custom domain. Add a `CNAME` record at your DNS provider
pointing to `your-username.github.io`. GitHub will manage HTTPS automatically.

## Project structure

```
src/
  pages/index.astro   — the entire site (single page)
  styles/global.css   — color, type, and spacing tokens
public/
  resume/             — drop your resume PDF here
```
