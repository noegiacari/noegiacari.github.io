# Noelia Giacari, portfolio

A plain HTML and CSS website. No framework, no build step: what you see in the files is exactly what the browser shows.

## The files

| File | What it is |
|---|---|
| `index.html` | Home page: intro and the four project cards |
| `centred.html` | Case study 1, Centred (personal project) |
| `artisancrafts.html` | Case study 2, ArtisanCrafts (IBM UX capstone, draft skeleton) |
| `vegan-book.html` | Case study 3, Vegan Book (freelance, accessibility audit) |
| `sailgenius.html` | Case study 4, SailGenius (collaboration with a developer) |
| `about.html` | About page |
| `style.css` | Every colour, font, size and layout rule for all pages |
| `images/` | One folder per project. `images/covers/covers-source.html` makes the card covers |
| `OUTLINE.md` | The plan: which projects, how to present them, what's still to decide |

## See your changes

Double-click any `.html` file to open it in the browser. After editing, save the file and refresh the browser tab.

## Common changes

**Change text.** Open the `.html` file in a text editor (VS Code is easiest), find the words, change them, save. Only edit the text between the tags, for example `<p>change this</p>`, not the tags themselves.

**Swap an image.** Put the new file in the project's folder in `images/`. Then either give it the same name as the old one, or change the `src="..."` in the page to the new name. Update the `alt="..."` text too: it describes the image for screen readers.

**Replace a grey placeholder with an image.** Change

```html
<div class="case-img placeholder-img"></div>
```

to

```html
<img class="case-img" src="images/vegan-book/cover.png" alt="Short description" />
```

**Reorder the projects.** In `index.html`, each project is one `<div class="case-card"> ... </div>` block. Cut the whole block and paste it where you want it. Also update the "Next project" link at the bottom of each case study so they follow the same order.

**Add a project.** Copy a case study file (for example `vegan-book.html`), rename it, rewrite the content, then copy a card in `index.html` and point its `href="..."` at the new file.

**Change colours or fonts.** At the top of `style.css`, under `:root`, are the main settings (`--black`, `--gray-500`, `--font-sans` and so on). Changing one value there changes it on every page.

## Case study building blocks

Inside a case study, each part is a ready-made block you can copy:

- `<section class="cs-section">`: a numbered section (01, 02...)
- `<div class="cs-block">`: a heading and text inside a section
- `<div class="cs-screens">`: a row of four phone screens
- `<div class="cs-img-grid pair">`: two screens side by side (before and after)
- `<img class="cs-img-full-real">`: one full-width image
- `<div class="results-grid">`: the row of big numbers

## Saving to GitHub

The site is backed up in a **private** GitHub repo: https://github.com/noegiacari/noegiacari.github.io
Only you can see it. It is not a public website yet.

After changing files, send the changes to GitHub from a terminal in this folder:

```
git add -A
git commit -m "Short note of what changed"
git push
```

Or ask Claude to "commit and push the portfolio".

## Going live (later)

When the content is ready, make the repo public (GitHub: Settings, General, Danger Zone, Change visibility).
Because the repo is called `noegiacari.github.io`, GitHub Pages then publishes it at https://noegiacari.github.io
(check Settings, Pages: Source "Deploy from a branch", branch `main`, folder `/`).
