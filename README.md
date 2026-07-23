# Daniel's Blog

A minimal, static blog built with plain HTML/CSS — no build step, no framework. Ready to host free on GitHub Pages.

## Files

- `index.html` — homepage listing all posts
- `about.html` — about page
- `style.css` — shared styling for the whole site
- `posts/` — one HTML file per blog post

## How to add a new post

1. Copy an existing file in `posts/` and rename it, e.g. `posts/2026-08-15-my-topic.html`.
2. Update the `<title>`, the `<h1>`, the date in `.post-meta`, and the body text.
3. Open `index.html` and copy the `<li>` block inside `<ul class="post-list">`. Paste a new one at the **top** (newest first) and update the date, link, title, and excerpt.

That's it — no rebuild needed. Just save and push.

## Publishing to GitHub Pages (username.github.io)

1. Create a GitHub account if you don't have one (github.com).
2. Create a new **public** repository named exactly `USERNAME.github.io` (replace USERNAME with your GitHub username).
3. Upload these files to the repository. Either:
   - Drag-and-drop the files on github.com ("Add file" → "Upload files"), **or**
   - Use git from the Terminal:
     ```
     cd ~/Desktop/Danielsblog
     git init
     git add .
     git commit -m "First post"
     git branch -M main
     git remote add origin https://github.com/USERNAME/USERNAME.github.io.git
     git push -u origin main
     ```
4. Your site goes live at `https://USERNAME.github.io` within a minute or two.

If you name the repo something other than `USERNAME.github.io`, go to the repo's **Settings → Pages**, set the source to the `main` branch, and the site will be served from `https://USERNAME.github.io/REPO-NAME/`.
