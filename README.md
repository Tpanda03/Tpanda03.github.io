# Tejash Panda — Portfolio

Personal portfolio + private dashboard. Built as a single `index.html` — zero dependencies, zero hosting costs.

---

## 🚀 Deploy to GitHub Pages (free hosting)

### Step 1 — Create a GitHub repo

1. Go to [github.com/new](https://github.com/new)
2. Name it exactly: `<your-github-username>.github.io`
   - e.g. `Tpanda03.github.io`
3. Set it to **Public** (required for free GitHub Pages)
4. Click **Create repository**

### Step 2 — Upload the file

**Option A — via GitHub website (easiest):**
1. In the repo, click **Add file → Upload files**
2. Drop `index.html` in
3. Commit to `main`

**Option B — via Git:**
```bash
git clone https://github.com/Tpanda03/Tpanda03.github.io
cd Tpanda03.github.io
cp /path/to/index.html .
git add index.html
git commit -m "initial portfolio"
git push
```

### Step 3 — Enable GitHub Pages

1. In the repo: **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / `root`
4. Click **Save**

### Step 4 — Visit your site

After ~60 seconds: `https://Tpanda03.github.io`

---

## 🔒 Private Dashboard

The private section is PIN-protected using SHA-256 hashing (client-side).

- **First visit:** click `⌗ Private` in the nav — you'll be prompted to **set** a 4-digit PIN
- **After that:** enter your PIN to unlock the dashboard
- All private data (goals, notes, tracker, reading list) is stored in **localStorage** — stays in your browser, never goes to GitHub or any server
- The PIN hash is stored in localStorage, NOT in the source code — so it's safe to have the repo public

> ⚠️ **Note:** Since data is in localStorage, it's device-specific. If you clear your browser data or switch devices, it resets. For now this is intentional — it's a personal scratchpad.

---

## 📝 Updating Content

Open `index.html` in any text editor. Things you'll want to update:

| What | Where in the file |
|------|-------------------|
| Name / headline | `#hero` section, `.hero-name` and `.hero-title` |
| Links (GitHub, LinkedIn, email) | `.hero-links` and `footer-links` |
| Projects list | `const PROJECTS = [...]` in the `<script>` |
| Experience items | `#experience` section, `.timeline-item` blocks |
| Skills | `#skills` section, `.skill-group` blocks |
| About text | `#about` section, `.about-text` |

---

## 🎨 Customization

The entire color palette is in CSS variables at the top of the `<style>` block:

```css
:root {
  --accent: #f0a500;   /* amber — change this to your vibe */
  --bg:     #0c0d0f;   /* background */
  ...
}
```

---

## 📁 File Structure

This is intentionally **one file**. No build tools, no npm, no dependencies.
Just `index.html` → GitHub Pages → done.

When you want to add more pages later (blog, case studies), you can add `about.html`, `blog/index.html`, etc. alongside it.
