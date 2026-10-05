# BKPIT Portfolio — Bidhan Kumar Paul

A modern, dynamic, single-page portfolio for **Bidhan Kumar Paul** (Applied Mathematics student, Python programmer, founder of **BKPIT**).

🌐 **Live site:** https://bidhankumarpaul.github.io/

Built with plain HTML, CSS and JavaScript. No framework, no build step, no dependencies.

---

## ✨ Features

- **Dark / light theme** that follows the device setting, with a manual toggle
- **English / বাংলা** language switch (remembered between visits)
- **Slide-out menu** listing every section, with the current section highlighted
- **Animated hero** with a typing effect, scroll progress bar and scroll-reveal sections
- **Skills** with animated bars (Kotlin and TypeScript are marked *vibe coded*)
- **Featured apps** with tech chips, a GitHub button and a Download APK button; screenshots are pulled from each repo's README
- **Latest projects**, loaded live from GitHub
- **GitHub overview**: profile stats, top languages, recent activity and contribution graph, all live
- **YouTube channel**: the 3 latest videos from [@bkpit](https://www.youtube.com/@bkpit)
- **BKP Writes**: a blog on its own page (`blog.html`)
- **CV section** with download and view buttons
- **Contact form** that sends messages straight to email
- **SEO**: meta tags, social share image, structured data, sitemap, robots.txt, favicon and a custom 404 page

---

## 📁 Project structure

```
.
├── index.html          # Main portfolio page (all HTML, CSS, JS in one file)
├── blog.html           # "BKP Writes" blog page
├── posts.js            # Blog posts (edit this to add posts)
├── 404.html            # Custom "page not found" page
├── robots.txt
├── sitemap.xml
└── assets/
    └── img/
        ├── my-profile-img.jpg      # Profile photo (tried first)
        ├── my-profile-img.png      # Profile photo (fallback)
        ├── logo.png                # BKPIT logo (512×512)
        ├── logo-192.png            # Logo for home-screen / apple-touch icon
        ├── og-image.png            # Social share preview image
        └── projects/               # Optional local screenshots (fallback)
            ├── mangal-1.png
            └── ekagrata-1.png
```

---

## 🚀 Deploy to GitHub Pages

1. Put all the files above in the root of the `BidhanKumarPaul.github.io` repository.
2. Commit and push to the default branch.
3. In the repo, go to **Settings → Pages** and make sure the source is the default branch (root).
4. Open https://bidhankumarpaul.github.io/ after a minute or two.

To preview locally, open `index.html` in a browser. Live GitHub and YouTube data load best from the hosted site or a local server, for example `python -m http.server`.

---

## 🛠️ How to update things

### Add a blog post
Open `posts.js` and copy one block inside `window.POSTS`:

```js
{id:'my-post', title:'My title', date:'2026-10-05', tag:'Math',
 summary:'One-line summary shown on the card.',
 body:`<p>Your post as HTML.</p>`}
```
`id` becomes the link (`blog.html#/my-post`). Newest posts go first.

### Add or change a featured app
In `index.html`, find `<section id="featured">` and copy a `card feat` block. Change the name, description, tech chips and links.
- **Screenshots** are read from the repo's README. Put plain images in the README, for example `![Home](docs/home.png)`.
- **Fallback screenshots**: save images as `assets/img/projects/<name>-1.png`, `-2.png`, `-3.png`.
- **Download APK** links to the repo's latest GitHub Release, so upload an APK there.
- **Live demo**: add `<a class="btn sm" href="YOUR-URL">Live demo</a>` where the comment in the HTML shows.

### Update skills
In `index.html`, find `const S=[['Python',80,'🐍'], ...]`. Each entry is `[name, percent, icon]`. Use `null` instead of a percent to show a *vibe coded* badge.

### Change the CV
Replace the Google Drive file ID in the two CV links (hero button and CV section). The Drive file must be shared as **Anyone with the link**.

### Edit Bengali text
In `index.html`, find the `BN` array. Each entry is `[CSS selector, Bengali text]`.

### Contact form setup
The form uses [FormSubmit](https://formsubmit.co) and needs no account. **After deploying, send one test message and click the activation link FormSubmit emails you.** To change where messages go, edit the email address in the `fetch('https://formsubmit.co/ajax/...')` call.

---

## 🔌 Live data sources

| Section | Source |
| --- | --- |
| GitHub overview, projects, activity | GitHub public API |
| Featured app screenshots | Each repo's README via the GitHub API |
| Contribution graph | ghchart.rshah.org |
| YouTube videos | YouTube RSS feed through rss2json |

If a source can't be reached, the site shows a built-in fallback. GitHub's public API allows about 60 requests per hour per visitor.

---

## 📬 Contact

- **Email:** bidhankumar331@gmail.com
- **GitHub:** [@BidhanKumarPaul](https://github.com/BidhanKumarPaul)
- **LinkedIn:** [Bidhan Kumar Paul](https://www.linkedin.com/in/bidhan-kumar-paul-420a3324b)
- **YouTube:** [@bkpit](https://www.youtube.com/@bkpit)

---

Developed by **BKPIT** · © Bidhan Kumar Paul
