# Push this folder to GitHub

The repo has already been initialized and a first commit has been made. You just need to create the empty repo on GitHub and push.

GitHub converts spaces in repo names to dashes, so the URL will be **`New-RAK-Stock-Order`**.

---

## Option A — easiest (GitHub website + 3 terminal commands)

### 1. Create the empty repo on github.com

1. Go to <https://github.com/new>
2. **Repository name:** `New-RAK-Stock-Order`
3. **Visibility:** Public
4. **Do NOT** tick "Add a README", "Add .gitignore", or "Add license" (the folder already has them — adding on GitHub will cause a conflict)
5. Click **Create repository**

### 2. Push from your Mac

Open Terminal and paste these three commands (replace `YOUR-USERNAME` with your GitHub username):

```bash
cd "/Users/talalnabina/Documents/Claude/Projects/test website creator with RAK stock order excel/github-repo"
git remote add origin https://github.com/YOUR-USERNAME/New-RAK-Stock-Order.git
git push -u origin main
```

If git prompts for a password, use a **Personal Access Token** (not your GitHub password): <https://github.com/settings/tokens> → Generate new token (classic) → tick `repo` scope.

### 3. Turn on GitHub Pages

1. Go to your new repo on GitHub
2. **Settings** → **Pages** (left sidebar)
3. **Source:** Deploy from a branch
4. **Branch:** `main` / `(root)` → **Save**
5. Wait ~1 minute. Your live store will be at:

   ```
   https://YOUR-USERNAME.github.io/New-RAK-Stock-Order/
   ```

---

## Option B — one-line with `gh` CLI (if you have it)

If you have the GitHub CLI installed (`brew install gh` if not):

```bash
cd "/Users/talalnabina/Documents/Claude/Projects/test website creator with RAK stock order excel/github-repo"
gh auth login            # only the first time
gh repo create "New-RAK-Stock-Order" --public --source=. --push
gh api -X POST /repos/:owner/New-RAK-Stock-Order/pages -f source='{"branch":"main","path":"/"}'
```

The last line enables Pages. Your site will be live within a minute at `https://YOUR-USERNAME.github.io/New-RAK-Stock-Order/`.

---

## What's in this commit

```
index.html       1.1 MB   ← the live storefront (served by GitHub Pages)
catalog.pdf     1.0 MB   ← printable A4 catalog, 11 pages
catalog.docx   334 KB    ← editable Word catalog
README.md                ← project description
.gitignore               ← ignores .DS_Store etc.
```
