# GitHub: From empty account → polished AI/ML portfolio (step-by-step)

This guide assumes you downloaded the bundle zip and now have a folder containing **separate repos**:

- `atlas-rag-copilot/`
- `sentinel-eval-safety-suite/`
- `orion-tool-agent/`
- `rescue-swarm-ai/`
- `restaurant-hybrid-recommender/`
- `portfolio-hub/` (this landing page)

> **Goal:** publish each project as its own GitHub repo, then deploy the **portfolio-hub** landing page as GitHub Pages.

---

## 0) One-time setup

### Install prerequisites

- Git
- Python 3.11+
- (Optional) VS Code

### Configure Git identity

```bash
git config --global user.name "Rohit Aggarwal"
git config --global user.email "<your-email>"
```

---

## 1) Create the repositories on GitHub

Create **6 empty repositories** (no README/license — you already have those locally):

1. `atlas-rag-copilot`
2. `sentinel-eval-safety-suite`
3. `orion-tool-agent`
4. `rescue-swarm-ai`
5. `restaurant-hybrid-recommender`
6. `portfolio-hub`

For each repo, set:

- Visibility: **Public**
- Default branch: **main**

---

## 2) Publish each project repo (repeat per repo)

From the bundle folder, go into a repo and push it.

Example for `atlas-rag-copilot`:

```bash
cd atlas-rag-copilot

git init
git add .
git commit -m "Initial commit: project with outputs"

git branch -M main
git remote add origin https://github.com/<your-username>/atlas-rag-copilot.git
git push -u origin main
```

Repeat for the other repos (change the folder and remote).

---

## 3) Turn on GitHub Pages for the landing page

1. Go to GitHub → `portfolio-hub` repo
2. **Settings → Pages**
3. Build and deployment:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/docs**
4. Save

Your site will be live at:

`https://<your-username>.github.io/portfolio-hub/`

---

## 4) Personalize the landing page

Edit:

`portfolio-hub/docs/data/config.json`

Replace:

- `<your-username>`
- `<your-profile>`
- `<your-email>`

Commit and push:

```bash
cd portfolio-hub
git add docs/data/config.json
git commit -m "Personalize landing page config"
git push
```

---

## 5) “Polish” checklist

### Repo “About” panel

For each project repo:

- Add a clear 1-line description
- Add topics (tags) like:
  - `machine-learning`, `ai`, `genai`, `rag`, `recommender-system`, `agents`, `evaluation`, `python`
- Add a homepage link (point to your GitHub Pages landing page)

### Pin your best repos

On your GitHub profile:

- Pin: `portfolio-hub`, `atlas-rag-copilot`, and 2–3 others

### Add a GitHub profile README

Create a new repo with the exact name of your GitHub username:

`<your-username>/<your-username>`

Add a `README.md` with:

- one-liner
- link to the landing page
- featured projects

---

## 6) Final verification (what a reviewer will do)

A reviewer typically:

1. Opens the landing page
2. Clicks **AtlasRAG**
3. Skims the README
4. Looks for:
   - outputs included
   - tests
   - run command

So before applying:

- open the landing page in an incognito tab
- click each repo
- verify images load
- verify outputs exist in the repo

---

## 7) Optional: custom domain

If you own a domain, you can point it to GitHub Pages and make your portfolio look even more “senior”.

GitHub Pages → Settings → Pages → Custom domain.
