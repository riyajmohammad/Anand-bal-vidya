# Anand Bal Vidya Mandir

This is a static website built with HTML and CSS. No framework, package installation, or build step is required.

## View the website

Open `index.html` in a browser. The other pages are standalone HTML files in this folder, and the shared stylesheet, images, and fonts are in `assets/`.

## Publish on GitHub Pages

1. Create a GitHub repository and upload the **contents of this folder** to the repository root (so `index.html`, `assets/`, and `.github/` are at the top level).
2. In the repository, open **Settings → Pages** and set the build and deployment source to **GitHub Actions**.
3. Push to the `main` branch, or run **Deploy static website to GitHub Pages** from the **Actions** tab.

The workflow in `.github/workflows/pages.yml` publishes these files directly, without a build step. Internal links and asset paths are relative, so they also work when GitHub hosts the site under a project URL such as `https://username.github.io/repository/`. `.nojekyll` ensures GitHub Pages serves all website files as-is.

If you instead publish manually from a branch, choose the repository root as the Pages folder.

## Existing form behavior

The original site did not connect its admission, enquiry, login, application-status, or fee-payment forms to a backend. Those forms and buttons remain presentation-only; submitting or using them does not store or send information.

There was no custom client-side JavaScript behavior in the original site, so navigation and form controls use native browser behavior without a JavaScript bundle.

GitHub Pages is static hosting; it cannot process form submissions, logins, or payments. Those features need a separate backend or external service.
