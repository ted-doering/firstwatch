# First Watch

A hand-picked guide to the movies & shows that explain American culture — built for friends newly arrived in the U.S. Browse by theme, genre, era, or must-watch ranking; save favorites and a watchlist; sign in with email or Google so your lists follow you across devices. Curator (`ted@narrative.church`) can add titles and edit the cultural notes.

## Deploy on GitHub Pages

1. Create a new GitHub repo and upload **both** files in this folder:
   - `index.html`
   - `first-watch-share.png`
2. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, pick `main` / root, **Save**.
3. Your site goes live at `https://YOURNAME.github.io/YOURREPO/` (takes a minute).

## Finish the link-preview graphic

Open `index.html` and find the Open Graph tags near the top of `<head>`. Replace every
`https://YOURNAME.github.io/YOURREPO/` with your real Pages URL, then re-upload. That's what
makes texts / Messenger / WhatsApp show the graphic instead of a bare link.
(Messenger & iMessage cache aggressively — if you change it later, re-scrape at
Facebook's Sharing Debugger to refresh.)

## Firebase (already wired in)

The app connects to your Firebase project automatically. Two console settings must be on:
- **Authentication → Sign-in method:** enable **Email/Password** and **Google**.
- **Authentication → Settings → Authorized domains:** add `YOURNAME.github.io`.

Then lock down **Firestore → Rules** with the production rules (shared library writable only by
`ted@narrative.church`; each person owns their own favorites/watchlist doc).

## One limitation

The curator "auto-fill details" button uses an AI helper that only exists inside the design tool
it was built in. On your live site that button will fail gracefully and you just fill the fields in
by hand — everything else (browsing, accounts, favorites, cloud sync, adding titles) works normally.
