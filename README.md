# Knowledge OS

Static GitHub Pages build for `knowledge-os-v20.html`.

## What gets faster

GitHub Pages can serve the app file faster and more reliably than opening it through Google Drive.

Your note data now syncs through Firebase Firestore at `knowledgeOS/state`.

## Publish with GitHub website

1. Create a new GitHub repository, for example `knowledge-os`.
2. Upload these files from this folder:
   - `index.html`
   - `.nojekyll`
   - `README.md`
3. Open the repository on GitHub.
4. Go to `Settings` -> `Pages`.
5. Under `Build and deployment`, choose:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
6. Save. GitHub will give you a Pages URL after the first deploy.

## Publish with Git commands

After creating an empty GitHub repository, run:

```powershell
git add .
git commit -m "Deploy Knowledge OS"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/knowledge-os.git
git push -u origin main
```

Then enable Pages from `Settings` -> `Pages` using the `main` branch and `/root`.

## Important

Firebase web config values are public client config, but your Firestore database must still be protected with sensible Security Rules before sharing the site widely.

Do not commit private AI API keys into this repo. This app currently calls Anthropic from the browser, so AI features should use a backend/proxy if you want them to work securely on a public website.
