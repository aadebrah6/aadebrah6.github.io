# aadebrah6.github.io

Personal website and digital CV for Augustine Atta Debrah — analytical chemist,
Ph.D. candidate at the Georgia Institute of Technology.

**Live site:** https://aadebrah6.github.io

---

## What's here

```
index.html    The entire site — HTML, CSS, and one small script, no dependencies
cv.pdf        Full curriculum vitae, linked as the primary download
resume.pdf    One-page résumé, the version submitted with applications
LICENSE       Terms (see "Reuse" below)
```

There is no build step, no framework, and nothing to install. The file you edit
is the file that gets served.

---

## How to update it

**In the browser (easiest):** open `index.html` in this repository, click the
pencil icon, edit, then commit. GitHub Pages redeploys in about a minute.

**On your computer:** clone the repo, open `index.html` in any text editor, save,
then commit and push. To preview before pushing, just open the file in a browser —
double-clicking works, because nothing needs a server.

### Common edits

| Task | Where to look |
|---|---|
| Add a publication | Copy any `<div class="pub">` block, paste it above the others, edit the text, renumber `pnum` |
| Add a job | Copy a `<div class="job">` block inside `<section id="experience">` |
| Add a technique | Find the matching `<div class="skill">` row and extend the `<dd>` text |
| Change colors | The `:root` block at the top of the `<style>` section — every color is defined once there |
| Swap the CV | Replace `cv.pdf` with a new file of the same name |
| Swap the résumé | Replace `resume.pdf` with a new file of the same name |
| Edit the About text | `<section id="about">` — plain paragraphs, no special markup |
| Update the peak labels | The `<svg>` in the hero — each `<text class="plabel">` sits above its peak |

### Editing the chromatogram

The hero graphic is a hand-written SVG path. Each peak is one cubic curve in the
`d` attribute of `.peaks`, in the form `C <x-32>,<baseline-8> <x-24>,<baseline-8> <x>,<height>`
followed by its mirror. Lower `<height>` values make taller peaks — the baseline
sits at y=158, so y=38 is a tall peak and y=110 is a short one. Peak labels are
positioned by their `x` matching the peak's `x`.

---

## Deployment

Hosted on GitHub Pages from the `main` branch, root directory.
Settings → Pages → Source: `main` / `(root)`.

The same folder deploys unchanged to Netlify or Cloudflare Pages — both accept a
drag-and-drop of the directory.

---

## Reuse

The code — the layout, CSS, and the chromatogram SVG — is MIT licensed, so anyone
is welcome to build on it.

The content is not. The CV text, About narrative, biography, publication list, cv.pdf, and resume.pdf are
personal professional records and are all rights reserved. Please don't copy them
into your own site. If you want the design, take `index.html` and replace the text
with yours.

See [LICENSE](LICENSE) for the full terms.
