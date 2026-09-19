# riri25.github.io
riazul's birthday site!

# 25 for 25 — birthday site

A one-page birthday site: a click-through intro, then a grid of polaroids —
one per friend — each with a photo, a favourite memory, a song, and
(optionally) a voice note.

It's a single static HTML file. No build step, no server, no dependencies
to install.

## Files

```
index.html      the whole site
photos/         one jpg per friend, named to match their entry below
```

## Editing the content

Open `index.html` in any text editor (or GitHub's own web editor) and look
for the block marked:

```
✏️ YOUR CONTENT GOES HERE
```

- **`BIRTHDAY_NAME`** — the birthday person's name.
- **`FRIENDS`** — one `{ name, memory, song, voice }` entry per polaroid.
  - `name` — the friend's name, **exactly** as their photo is named (see below)
  - `memory` — their memory, as plain text
  - `song` — a Spotify or YouTube link, or `""` if none
  - `voice` — a direct link to a voice note file, or `""` if none

There's a second editable block further down marked
`✏️ EDIT THE OPENING SEQUENCE HERE` — that's the intro slideshow text, one
line per screen.

### Photos

You don't write a filename anywhere. For a friend named `"Priya"`, the page
automatically looks for:

```
photos/Priya.jpg
```

So: put every photo in a folder called `photos` next to `index.html`, and
name each file **exactly** like the matching `name` field — same spelling,
same capital letters. Capitalization matters once this is live on GitHub
Pages, even if it doesn't matter on your own computer.

If a file is `.jpeg` or `.png` instead of `.jpg`, that's fine — it'll try
all three automatically. If a photo is missing entirely, that polaroid just
shows a soft placeholder with the friend's initial instead of a broken
image.

### Voice notes

1. Record it, upload it to Google Drive.
2. Right-click the file → Share → "Anyone with the link."
3. Take the share link:
   ```
   https://drive.google.com/file/d/FILE_ID/view?usp=sharing
   ```
   and turn it into a direct link by rewriting it as:
   ```
   https://drive.google.com/uc?export=download&id=FILE_ID
   ```
4. Paste that into the friend's `voice` field.

## Putting it on GitHub Pages

1. Create a repo and upload `index.html` and the `photos` folder to it
   (keep them at the same level — don't nest `index.html` inside another
   folder).
2. Go to **Settings → Pages**.
3. Under "Build and deployment," set the source to deploy from a branch,
   pick `main` (or whichever branch you uploaded to) and the `/ (root)`
   folder.
4. Save. GitHub will give you a URL that looks like:
   ```
   https://yourusername.github.io/reponame/
   ```
   That's the link to send.

Changes usually go live within a minute or two of pushing — refresh if it
looks stale.
