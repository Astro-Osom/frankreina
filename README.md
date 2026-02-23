# frankreina
Personal website
[README.md](https://github.com/user-attachments/files/25476354/README.md)
# frankreina.com

Personal website for Frank Reina — filmmaker, writer, and creator of Future Vibrant Self.

## Setup

This is a static single-page site hosted on GitHub Pages.

### Files

- `index.html` — the entire site (HTML, CSS, JS in one file)
- `headshot.jpg` — your headshot photo (add this yourself)
- `CNAME` — custom domain config for GitHub Pages

### Deploy to GitHub Pages

1. Create a new repo on GitHub named `frankreina.com` (or any name)
2. Push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/frankreina.com.git
   git push -u origin main
   ```
3. Go to **Settings → Pages** in your repo
4. Set source to **Deploy from a branch** → `main` → `/ (root)`
5. Your site will be live at `https://YOUR_USERNAME.github.io/frankreina.com/`

### Connect your custom domain (frankreina.com)

1. In your GitHub repo, go to **Settings → Pages → Custom domain**
2. Enter `www.frankreina.com` and save
3. In NameSilo, add these DNS records:
   - **A records** (for apex domain `frankreina.com`):
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - **CNAME record**:
     ```
     www → YOUR_USERNAME.github.io
     ```
4. Check **Enforce HTTPS** in GitHub Pages settings once DNS propagates (can take up to 24 hours)

### Set up Formspree

1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form
3. Copy your form endpoint (looks like `https://formspree.io/f/xyzabc123`)
4. In `index.html`, replace `YOUR_FORM_ID` with your actual form ID

### Add your headshot

Drop your headshot image into the repo root as `headshot.jpg`. The site references this filename directly.

## Structure

Single-page layout with these sections:

- **Hero** — name, tagline, headshot
- **Biography** — expandable bio with "Read more" toggle
- **Filmography** — 4×2 grid of YouTube video tiles
- **Manifesto** — "Self-transformation through storytelling"
- **Projects** — Scrambled + Future Vibrant Self cards
- **Writing & Video Journals** — Substack link + YouTube channel tile
- **Newsletter signup** — Formspree form (first name, last name, email)
- **Footer** — social links, project site links

## Tech

- Pure HTML/CSS/JS — no build tools, no frameworks
- Google Fonts (Cormorant Garamond + DM Sans)
- YouTube thumbnail API for film tile images
- Formspree for email collection
- Intersection Observer for scroll fade-in animations
- Responsive down to mobile (2-column film grid on small screens)
