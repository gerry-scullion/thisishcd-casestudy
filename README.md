# Case Study Submission Form

A single-page Netlify form for collecting case studies for the book *This is Human-Centred Design*. Styled to match thisishcd.com — cobalt blue hero, cream body, Archivo display + Inter body, yellow CTA.

## What's in this folder

- `index.html` — the form itself (single long page, all sections inline)
- `success.html` — thank-you page shown after submission
- `netlify.toml` — Netlify build & redirect config
- `README.md` — this file

## Deploy in 60 seconds (drag & drop)

1. Sign in at [app.netlify.com](https://app.netlify.com).
2. Click **Add new site → Deploy manually**.
3. Drag this whole `case-study-form` folder into the browser drop zone.
4. Done. Netlify gives you a `*.netlify.app` URL — open it and the form is live.

## Deploy via Git (recommended for ongoing edits)

1. Push this folder to a new GitHub/GitLab repo.
2. In Netlify: **Add new site → Import from Git** → pick the repo.
3. Build command: leave blank. Publish directory: `.` (or whatever folder you put this in).
4. Deploy.

## Where do submissions go?

In your Netlify site dashboard → **Forms** → `case-study`.

You'll see every submission with all fields, uploaded files (photos + PDF), and timestamps. Submissions are kept indefinitely on the free tier (up to 100 / month) and can be exported as CSV.

## Get notified by email when someone submits

1. Netlify dashboard → **Forms** → **Form notifications**
2. **Add notification → Email notification**
3. Pick the `case-study` form and add your email.

## File uploads — important limits

Netlify's free tier caps **total form upload size at 8 MB per submission**. The form already warns submitters about this and offers a Dropbox/Drive link field as a fallback for large photo sets. The PDF upload field is capped to a single PDF.

If you expect a lot of large files, upgrade Netlify Forms (Pro tier) or swap the file inputs for an external uploader like Uploadcare or Filestack.

## Customising

All styling lives in the `<style>` block at the top of `index.html`. The colour palette is in CSS variables on `:root`:

```css
--blue: #0a3cff;       /* hero background */
--cream: #f5f1e8;      /* page background */
--yellow: #ffd60a;     /* submit button */
--ink: #0b0b0d;        /* primary text + button border */
```

Tweak these and the rest of the design follows. To add or remove a theme pill, edit the `.pills` block in section 2.

## Spam protection

Two layers are already enabled:

- **Honeypot field** (`bot-field`) — invisible to humans, catches naive bots.
- Netlify's built-in Akismet check — runs automatically on all submissions.

For more aggressive bot protection, add reCAPTCHA in Netlify dashboard → **Forms** → **Settings**.

## Custom domain

Once it's live, add a custom subdomain in Netlify → **Domain settings**, e.g. `casestudies.thisishcd.com`.
