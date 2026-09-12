# Mat Di Pizzo — composer site

Plain HTML/CSS, no build step. Three sections: about, works, contact.

## Deploy on GitHub Pages

1. Create a new GitHub repo. If you want the site at `https://<username>.github.io`
   (root domain, no path), name the repo exactly `<username>.github.io`.
   Any other name gives you `https://<username>.github.io/<reponame>`.
2. Push these files (`index.html`, `style.css`, `assets/`) to the repo's default
   branch (`main`).
3. In the repo, go to **Settings → Pages**, set **Source** to the `main` branch
   and `/ (root)` folder, then save.
4. Give it a minute — your URL will be shown on that same settings page once
   it's live.

### Adding a custom domain later
In the same **Settings → Pages** panel, enter your domain under **Custom
domain** — GitHub creates the `CNAME` file for you. You'll also need to point
your domain's DNS at GitHub (an A/ALIAS or CNAME record, depending on
apex vs. subdomain) — GitHub's docs walk through the exact records.

## Editing content

- **Bio** — edit the text inside `<section id="about">` in `index.html`.
- **Photo** — swap `assets/profile.jpg` for a new image (same filename, or
  update the `src` in the `<img>` tag). Keep it reasonably sized for the web
  (this one is 900px wide, ~170KB) so the page stays fast.
- **Works** — each entry is one `<article class="work">` block. Copy/paste
  a block to add a new work; delete one to remove a work.
- **SoundCloud embeds** — each work has its own `<iframe>`. To get your own
  embed code: on a track's SoundCloud page, click **Share → Embed**, copy the
  `src="https://w.soundcloud.com/player/?url=..."` value, and paste it in
  place of the placeholder `src` (the placeholders currently point to
  `your-track-url-1/2/3` and won't play anything until replaced).
- **Email** — update the `mailto:` address and visible text in the contact
  section.
- **Reels** — each reel is a `<blockquote class="instagram-media">` in the
  `<section id="reels">` block. To add your own: open the reel on Instagram,
  click the **···** menu → **Embed**, and copy the `data-instgrm-permalink`
  URL into a blockquote (or paste Instagram's whole embed snippet in place of
  one of the placeholders). Copy/paste a blockquote to add more, delete one
  to remove. The page loads Instagram's embed script automatically to render
  them.

## Notes
- Fonts (Fraunces, Public Sans) load from Google Fonts — an internet
  connection is needed for them to display; there's a plain system-font
  fallback if that ever fails.
- The palette pulls a deep wine-red accent from the guitar in your photo,
  set against a near-black warm charcoal background.
