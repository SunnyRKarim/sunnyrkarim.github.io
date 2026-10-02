# Sunny Karim academic website

This is a simple static academic website prepared for GitHub Pages.

## Files

- `index.html`: homepage
- `research.html`: research papers and projects
- `teaching.html`: teaching page
- `cv.html`: CV landing page
- `assets/css/style.css`: all site styling
- `.nojekyll`: tells GitHub Pages to serve the files directly

## 1. Create the GitHub Pages repository

Create a public GitHub repository named exactly:

`YOUR-GITHUB-USERNAME.github.io`

Upload the contents of this folder to the root of that repository.

## 2. Turn on GitHub Pages

In the repository, go to:

Settings > Pages

Under "Build and deployment", choose:

- Source: Deploy from a branch
- Branch: `main`
- Folder: `/ (root)`

Your site will then be available at:

`https://YOUR-GITHUB-USERNAME.github.io/`

## 3. Add your photograph

Save your profile image as:

`assets/img/profile.jpg`

Then in `index.html`, replace the block:

```html
<div class="portrait-placeholder" aria-label="Profile photo placeholder">
  <span>SK</span>
</div>
```

with:

```html
<img class="profile-photo" src="assets/img/profile.jpg" alt="Sunny Karim">
```

Add this to `assets/css/style.css`:

```css
.profile-photo {
  width: 230px;
  height: 280px;
  object-fit: cover;
  border: 1px solid var(--line);
}
```

You can remove the `photo-note` paragraph after adding the image.

## 4. Add the CV

Create this folder:

`assets/cv/`

Place the compiled CV there as:

`assets/cv/Sunny_Karim_CV.pdf`

In `cv.html`, replace the disabled button with:

```html
<a class="button" href="assets/cv/Sunny_Karim_CV.pdf">Download CV (PDF)</a>
```

The URL of the CV will remain permanent even when the PDF is replaced with a newer version.

## 5. Overleaf workflow

Once the CV is maintained in Overleaf and synchronized to GitHub, the site can be extended with a GitHub Actions workflow so that the LaTeX source is compiled automatically and the newest PDF is placed at the permanent CV path.

## 6. Edit research links

The placeholder `href="#"` entries in `research.html` should be replaced with links to your papers, software, slides, or replication files.

## Design philosophy

The site deliberately uses plain HTML and CSS. There is no framework, package manager, or JavaScript dependency. This makes the site fast, stable, portable, and easy to maintain.
