# My Portfolio Site

Live URL (default GitHub Pages):
https://rafifind.github.io/my-portfolio-site/

## Quick start

Edit files in this folder, then commit and push to `main` to deploy.

```pwsh
# From d:\DevelopmentWorkspace\Web_Projects\my-portfolio-site
git add .
git commit -m "Update site content"
git push
```

GitHub Actions will build and publish automatically. The job name: "Deploy to GitHub Pages".

## Local preview (optional)

```pwsh
# Python 3 quick server
python -m http.server 5500 -d "d:\DevelopmentWorkspace\Web_Projects\my-portfolio-site"
# Open http://localhost:5500
```

## Project structure

- `index.html` — main page
- `styles.css` — styles (light/dark theme supported)
- `images/` — assets (e.g., `profile.jpg`)
- `favicon.svg` — favicon
- `robots.txt` — allows crawling and points to the sitemap
- `sitemap.xml` — helps search engines discover the site
- `.github/workflows/pages.yml` — GitHub Pages deployment workflow

## Configuration

- Canonical URL is set to the default Pages URL in `index.html`.
- If you later add a custom domain, update these in one pass:
  - Remove the canonical `href` and `og:url` pointing to the default URL and replace with your domain.
  - Update `robots.txt` sitemap and `sitemap.xml` to use your domain.
  - Add a `CNAME` file with a single line containing your domain.
  - Configure DNS and enable HTTPS in GitHub Pages.

## Troubleshooting

- Workflow not running: ensure you pushed to `main` and the workflow file is `.github/workflows/pages.yml`.
- 404 after deploy: wait 2–5 minutes and hard refresh. Verify that the artifact path in the workflow is `.`.
- Custom domain issues: remove custom domain from Settings → Pages if you’re using the default URL, or configure DNS correctly if using a domain.

## Updating contact email

In `index.html`, replace `mailto:example@gmail.com` with your address.
