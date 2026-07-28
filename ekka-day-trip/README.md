# 🎡 EKKA Show Day trip invite

A playful one-page fairground invitation. The "No" button runs away, then it walks the invitee
through a few fun questions and, at the end, sends their answers straight into a Google Calendar
invite (guests: the invitee + brobert.uy@gmail.com) with an email fallback.

## Personalise the name in the URL
Add `?name=` to the link:
```
https://YOUR-SITE/?name=Jess
https://YOUR-SITE/?name=jess%20lee   (spaces = %20)
```
`?to=` also works. No name = it just says "you".

## Put it on GitHub Pages (gives a public link you can SMS)
1. Create a new repo on github.com, e.g. `ekka-day-trip`.
2. Upload **`index.html`** (this folder) to the repo — drag-and-drop in the browser is fine.
3. Repo **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   branch **main** / root, Save.
4. Wait ~1 min. Your link is `https://YOUR-USERNAME.github.io/ekka-day-trip/?name=Jess`.

Or via command line (once you're signed in to `git`/`gh`):
```bash
cd ekka-day-trip
git init && git add index.html README.md && git commit -m "EKKA day trip invite"
gh repo create ekka-day-trip --public --source=. --push   # needs GitHub CLI + login
```
Then enable Pages as in step 3.

## Files
- `index.html` — the whole site (self-contained, mobile-first). This is the one to host.
- `artifact.html` — same page, body-only, used to publish the Claude Artifact version.
