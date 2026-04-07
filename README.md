# NU Learning Website

A static educational website for NU Learning, built with HTML, CSS, and JavaScript.

## Overview

This project contains:
- A public homepage and navigation pages (`index.html`, `allpaths.html`, `about.html`)
- Learning path pages (Foundations, Full Stack JavaScript, Full Stack Ruby on Rails)
- Course and lesson pages grouped under `courses/`
- Shared static assets in `css/`, `js/`, and `images/`

## Project Structure

```text
Project-Website-NU-Learning/
├─ index.html
├─ allpaths.html
├─ about.html
├─ full-stack-javascript.html
├─ full-stack-ruby-on-rails.html
├─ foundations-course.html
├─ sign-in.html
├─ sign-up.html
├─ courses/
│  ├─ foundations/
│  ├─ html-css/
│  ├─ javascript/
│  ├─ react/
│  ├─ nodejs/
│  ├─ ruby/
│  └─ rails/
├─ css/
├─ js/
└─ images/
```

## Run Locally

You can open `index.html` directly in your browser, or run a local static server.

### Option 1: Open directly
- Double-click `index.html`

### Option 2: Use VS Code Live Server
- Install **Live Server** extension
- Right-click `index.html` -> **Open with Live Server**

### Option 3: Python static server
```bash
python -m http.server 5500
```
Then open: `http://localhost:5500`

## Deployment

This is a static site and can be deployed to:
- GitHub Pages
- Vercel
- Netlify

### Important
- The homepage entry file must be **`index.html`**.
- If deployed under a subpath (for example `/Project-Website-NU-Learning/`), use links that respect that base path.

## Navigation Notes

- Navbar and logo home links should point to `index.html` (or the correct subpath root in production).
- If a page is moved into `courses/...`, update relative links accordingly.

## Common Issues

### 404 after deploy
- Confirm `index.html` exists in the deployment root.
- Check that links do not still point to removed files (for example `home.html`).

### Broken links after reorganizing files
- Update all affected `href` values after moving files into subfolders.
- Verify pages from multiple locations (root + nested `courses/` folders).

## Updating the Site

```bash
git add .
git commit -m "Describe your change"
git push
```
