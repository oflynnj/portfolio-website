# CSCI 120 Portfolio Website — Starter Template

This is a starter template for your personal, public-facing portfolio/resume website. It's plain HTML and CSS on purpose, so you can see and understand everything the browser is actually doing.

## What's in this template

```
your-repo/
├── index.html      <- the page itself: all the text and structure
├── style.css       <- all the colors, spacing, and layout
├── assets/         <- put images, your resume PDF, etc. here
└── README.md       <- this file
```


## Part 1 — Get your own copy of this template (One time setup)
**Step 1 — clone the shared repository.**
clone this repo which will look like:
```
git clone [<the-repo-url>](https://github.com/cs120-ExploringCS/project1-website.git) my-portfolio
cd my-portfolio
```
This downloads a full copy of the files onto your computer, inside a new folder called `my-portfolio`.

**Step 2 — create your own empty repository on GitHub.**

1. Log in to GitHub and go to [github.com/new](https://github.com/new).
2. Give it a name (e.g. `my-portfolio` or `portfolio-website`).
3. Leave it set to **Public** (this matters for Part 5).
4. **Do not** check "Add a README file" or add a `.gitignore` — leave the new repository completely empty. (If you do initialize it, git will complain about unrelated histories when you try to push in later steps.)
5. Click **Create repository**. GitHub will show you a repository URL like
   `https://github.com/your-username/my-portfolio.git` — copy it.
   
**Step 3 — point your local copy at your new repository, and push.**

Back in your terminal, still inside the `my-portfolio` folder from Step 1:

```
git remote remove origin
git remote add origin https://github.com/your-username/my-portfolio.git
git branch -M main
git push -u origin main
```

What each line does: the first two swap out "where does this project belong on GitHub" from your instructor's repo to your own new one; `git branch -M main` makes sure your branch is named `main`; `git push -u origin main` uploads everything for the first time and remembers this connection so that plain `git push` works from now on.


## Part 2 — Understand the two files

**`index.html`** holds the content and structure: your name, your About paragraph, your project descriptions, your contact links. Every placeholder you need to change is marked with an HTML comment starting with `TODO`, like this:

```html
<!-- TODO: replace with your name -->
<h1>Hi, I'm Your Name.</h1>
```

Open `index.html` in a text editor and search for the word `TODO` (most editors have a "Find" feature, Ctrl+F / Cmd+F) to find every spot that needs your information.

**`style.css`** controls how it looks.  If you want to make it your own, the very top of the file has a block that looks like this:

```css
:root {
  --color-primary: #1d4ed8;   /* try changing this to a color you like */
  ...
}
```

Change a color there and it updates everywhere that color is used on the page.

## Part 3 — Preview your changes locally

After editing `index.html`, you can see your changes locally: find `index.html` in your file browser and double-click it. It will open in your default web browser. Refresh the browser tab after each save to see your latest edit.

## Part 4 — Git workflow

You'll use three git commands frequently. Here's what each one actually does, in order:

1. **`git add <file>`** — "stage" a file, meaning: include this file's changes in the next snapshot I'm about to save. (`git add .` stages every changed file at once.)
2. **`git commit -m "a short message"`** — actually save that snapshot, with a message describing what changed. Think of a commit as a labeled save point you can always go back to.
3. **`git push`** — upload your saved commits from your computer to GitHub, so they show up in your repository online (and, once Pages is turned on, on your live website).

A typical work session looks like this, run from a terminal inside your project folder:

```
git add .
git commit -m "Add my About section and first project"
git push
```

You'll do this every time you want your live site to reflect your latest edits — editing the file alone does **not** update your website; you have to commit and push.
## Part 5 — Turn on GitHub Pages

GitHub Pages is the free service that takes the HTML/CSS files sitting in your repository and turns them into an actual website anyone can visit.

1. On your repository's GitHub page, click **Settings** (top menu bar).
2. In the left sidebar, click **Pages**.
3. Under "Build and deployment," set **Source** to **Deploy from a branch**.
4. Under "Branch," choose **main** and folder **/ (root)**, then click **Save**.
5. Wait a minute or two, then refresh the page — GitHub will show you your
   site's live URL, which will look like:
   ```
   https://your-username.github.io/your-repo-name/
   ```
**Important — repository visibility:** GitHub Pages only works automatically on a **public** repository if you're on a free GitHub account.
