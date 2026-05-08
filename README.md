# ExpLab Homepage

This folder contains a standalone promotional landing page for ExpLab.

It is intentionally separate from the application code in `frontend/` and `backend/`.

## Deploy with GitHub Pages

This repo now includes a GitHub Actions workflow at
`/.github/workflows/deploy-homepage.yml` that publishes this folder to GitHub Pages.

### What to do in GitHub

1. Push the repo to GitHub.
2. In the repository, go to `Settings` -> `Pages`.
3. Under `Build and deployment`, set `Source` to `GitHub Actions`.
4. Push a change to `homepage/` or run the `Deploy Homepage` workflow manually from the `Actions` tab.

### Add a custom domain

After Pages is working, you can point a domain such as `getexplab.com` to it:

1. In `Settings` -> `Pages`, enter your custom domain.
2. At your DNS provider, add these `A` records for the apex domain:

```txt
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

3. If you also want `www`, add a `CNAME`:

```txt
www -> anasfrh.github.io
```

4. Wait for DNS to propagate, then enable `Enforce HTTPS` in the GitHub Pages settings.

## Open locally

You can open `index.html` directly in a browser, or serve the folder with a simple static server.

Example:

```bash
cd /Users/anasfarah/Documents/Projects/ExperimentationPlatform/homepage
python3 -m http.server 4321
```

Then visit `http://127.0.0.1:4321`.
