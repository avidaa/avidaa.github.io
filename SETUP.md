# GitHub Pages Setup Guide

## Initial Setup (One-time)

1. **Configure GitHub Pages:**
   - Go to your repository on GitHub: `https://github.com/avidaa/avidaa.github.io`
   - Click **Settings** → **Pages**
   - Under **Source**, select: **Deploy from a branch**
   - Branch: **main** (or **master**)
   - Folder: **/docs**
   - Click **Save**

2. **Push your code:**
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

3. **Wait for GitHub Actions:**
   - The workflow will automatically build your site
   - It may take a few minutes for the first deployment
   - Check the **Actions** tab to see the build status

4. **Access your site:**
   - Your site will be available at: `https://avidaa.github.io`
   - It may take a few minutes to become live after the first deployment

## Making Updates

1. **Edit your `.qmd` files** (e.g., `index.qmd`, `blogs.qmd`, etc.)
2. **Commit and push:**
   ```bash
   git add .
   git commit -m "Update content"
   git push origin main
   ```
3. **GitHub Actions will automatically:**
   - Build your site using Quarto
   - Update the `docs/` folder
   - Your site will be updated within a few minutes

## Local Development

To preview your site locally before pushing:

```bash
# Install Quarto if you haven't already
# https://quarto.org/docs/get-started/

# Preview the site
quarto preview

# Build the site
quarto render
```

## Troubleshooting

- **Site not updating?** Check the Actions tab to see if the build succeeded
- **404 errors?** Make sure GitHub Pages is configured to serve from `/docs` folder
- **Build failures?** Check the Actions logs for error messages

