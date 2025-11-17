# Website Deployment Guide

## Repository Structure

I've created two separate Git repositories ready for deployment:

### 1. Codex Mycelius (`codex-mycelius-site/`)
- **Domain:** codexmycelius.com
- **Files:** index.html, codex_style.css, netlify.toml, README.md

### 2. Fungio Manifesto (`fungio-manifesto-site/`)
- **Domain:** fungioergosum.com  
- **Files:** index.html, fungio_style.css, netlify.toml, README.md

## Deployment Steps

### 1. Push to GitHub

For each site, create a GitHub repository:

```bash
# For Codex Mycelius
cd codex-mycelius-site
git remote add origin https://github.com/yourusername/codex-mycelius.git
git branch -M main
git push -u origin main

# For Fungio Manifesto
cd ../fungio-manifesto-site
git remote add origin https://github.com/yourusername/fungio-manifesto.git
git branch -M main
git push -u origin main
```

### 2. Connect to Netlify

1. Go to [netlify.com](https://netlify.com) and sign in
2. Click "New site from Git"
3. Choose GitHub and authorize
4. Select your repository
5. Build settings are automatic (thanks to `netlify.toml`)
6. Click "Deploy site"
7. Repeat for the second repository

### 3. Connect Custom Domains

In Netlify dashboard for each site:
1. Go to Site Settings → Domain Management
2. Click "Add custom domain"
3. Enter your domain (codexmycelius.com or fungioergosum.com)
4. Follow DNS configuration instructions

In Shopify:
1. Go to Settings → Domains
2. For each domain, update DNS settings to point to Netlify
3. Use the DNS records Netlify provides

### 4. Automatic Deployment

Once connected:
- Any push to the `main` branch automatically deploys
- Netlify provides build logs and preview deployments
- SSL certificates are automatic

## Future Updates

To update either site:
1. Edit files in the respective directory
2. Commit changes: `git add . && git commit -m "Update content"`
3. Push: `git push origin main`
4. Netlify automatically deploys within minutes

## Benefits

- **Automatic deployment** on every push
- **Free SSL certificates**
- **Global CDN** for fast loading
- **Build previews** for testing
- **Custom domains** fully supported


