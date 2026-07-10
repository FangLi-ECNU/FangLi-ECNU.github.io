# Fang Li's Academic Homepage

This is the source for my academic personal homepage, powered by **GitHub Pages** and **Jekyll**.

👉 **Live site**: `https://<your-username>.github.io/`

---

## How to Deploy on GitHub

### Step 1: Create a GitHub repository

Create a new repository on GitHub named:

- **`<your-username>.github.io`** — for a user/org homepage (recommended)
  - The site will be at `https://<your-username>.github.io/`
- Or any other name — for a project page
  - The site will be at `https://<your-username>.github.io/<repo-name>/`
  - If you use this option, set `baseurl: "/<repo-name>"` in `_config.yml`

### Step 2: Push the files to GitHub

```bash
git init
git add -A
git commit -m "Initial commit: academic homepage"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub → **Settings** → **Pages**
2. Under "Build and deployment", select:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` → `/ (root)` → Save
3. Wait a few minutes — your site will be live!

---

## How to Edit Content

All content is in **Markdown** (`.md`) files. You can edit them directly on GitHub's web interface:

| Page | File | What to edit |
|------|------|-------------|
| Home | `index.md` | Your photo (replace `/assets/images/lifang1.jpg`), intro, contact info |
| Biography | `biography.md` | Appointments, education, visiting experience |
| Publications | `publications.md` | Add new papers (copy-paste the format) |
| Students | `students.md` | Student list, available positions |
| Teaching | `teaching.md` | Add new courses each semester |
| Funds | `funds.md` | Research grants and funding |
| Links | `links.md` | Lab resources and useful links |
| Config | `_config.yml` | Site title, email, navigation |

### Adding a new publication

Just add a line in `publications.md` under the right year:

```markdown
- Author Names. Paper title. *Journal Name*, volume:pages, year. [[pdf]](/assets/papers/2025/paper.pdf)
```

### Replacing the profile photo

Upload a new JPG file to `assets/images/` and update the path in `index.md`.

### Adding a new page

1. Create a new `.md` file (e.g., `news.md`)
2. Add it to `header_pages` in `_config.yml`

---

## Local Preview (Optional)

If you want to preview changes locally before pushing:

```bash
# Install Ruby and Jekyll (one-time setup)
gem install bundler jekyll

# Create a Gemfile
echo "gem 'github-pages', group: :jekyll_plugins" > Gemfile
bundle install

# Run local server
bundle exec jekyll serve
# Visit http://localhost:4000
```

---

## File Structure

```
├── _config.yml          # Site configuration
├── index.md             # Homepage
├── biography.md         # Biography page
├── publications.md      # Publications list
├── students.md          # Students & positions
├── teaching.md          # Teaching history
├── funds.md             # Research funding
├── links.md             # Useful links
├── assets/
│   ├── images/          # Photos and logos
│   └── papers/          # PDF papers (organized by year)
└── README.md
```
