# PulseBot

**AI Agent That Automates Uxento**

PulseBot is an AI agent that makes Uxento obsolete by automating every manual feature through natural language commands. Zero clicking, zero browser extensions—just pure agent-driven token deployment.

🌐 **Live Site**: [pulsebot.fun](https://pulsebot.fun)  
🐦 **Twitter/X**: [@pulsebot](https://x.com/pulsebot)

## Features

- **Auto Quick Deploy**: Tweet-to-token in milliseconds via natural language
- **Instant Vamp**: Clone any token by contract address—no GUI required
- **Cross-Platform Deploy**: Launch simultaneously on Pump.fun, Bonk, BagsApp, FourMeme
- **Automated Rewards**: Auto-claim creator fees when thresholds hit
- **Headless Operation**: No browser, no extensions—runs anywhere agents operate

## Quick Start

```bash
# One-liner installation (PowerShell)
iwr -useb https://pulsebot.fun/install.ps1 | iex
```

Then command via chat:
```
@pulsebot launch this tweet
```

## Repository Structure

```
pulsebot/
├── index.html              # Main landing page
├── styles.css             # Main stylesheet
├── script.js              # Interactive functionality
├── CNAME                  # Custom domain configuration
├── P_large.png           # Logo (large)
├── p_small.png           # Logo (small/favicon)
├── docs/                 # Documentation site
│   ├── index.html       # Documentation pages
│   ├── docs.css        # Documentation styles
│   └── docs.js         # Documentation scripts
└── .github/
    └── workflows/
        └── deploy.yml   # GitHub Actions deployment

```

## Deployment

This project is configured for **GitHub Pages** with automated deployment via **GitHub Actions**.

### Setup Steps

1. **Push to GitHub**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/i2gucci/pulsebot.git
   git push -u origin main
   ```

2. **Configure GitHub Pages**:
   - Go to repository **Settings** → **Pages**
   - Under **Build and deployment**:
     - Source: **GitHub Actions**
   - The workflow will automatically deploy on every push to `main`

3. **Set up Custom Domain** (pulsebot.fun):
   - In repository **Settings** → **Pages** → **Custom domain**
   - Enter: `pulsebot.fun`
   - Wait for DNS check to complete
   
4. **Configure DNS** (at your domain registrar):
   Add these DNS records:
   ```
   Type: A
   Name: @
   Value: 185.199.108.153
   
   Type: A
   Name: @
   Value: 185.199.109.153
   
   Type: A
   Name: @
   Value: 185.199.110.153
   
   Type: A
   Name: @
   Value: 185.199.111.153
   
   Type: CNAME
   Name: www
   Value: i2gucci.github.io
   ```

### Manual Deployment

If you prefer manual deployment without GitHub Actions:
- Simply enable GitHub Pages in Settings → Pages
- Select source: **Deploy from a branch**
- Branch: `main` / `root`

## Development

### Local Testing

Since this is a static site, you can test locally with any HTTP server:

```bash
# Python
python -m http.server 8000

# Node.js (npx)
npx serve

# PHP
php -S localhost:8000
```

Then visit: `http://localhost:8000`

### File Structure Notes

- `CNAME` contains the custom domain (`pulsebot.fun`)
- All assets referenced in HTML use relative paths
- Documentation is in `/docs` subdirectory
- Icons are inline SVG for performance

## Verification Checklist

Before pushing to GitHub:

- [x] CNAME file contains correct domain
- [x] All image paths are correct (P_large.png, p_small.png exist)
- [x] Links between pages work (home ↔ docs)
- [x] GitHub Actions workflow configured
- [x] .gitignore includes unnecessary files
- [ ] DNS records configured at registrar
- [ ] GitHub Pages enabled in repository settings

## Custom Domain Setup

After pushing to GitHub:

1. Wait for initial GitHub Actions deployment to complete
2. In GitHub repo Settings → Pages → Custom domain, enter `pulsebot.fun`
3. Enable "Enforce HTTPS" (after DNS propagates)
4. DNS propagation can take 24-48 hours

## Technologies

- **Frontend**: Vanilla HTML, CSS, JavaScript
- **Font**: Space Mono (Google Fonts)
- **Deployment**: GitHub Pages + GitHub Actions
- **Domain**: pulsebot.fun

## License

© 2026 PulseBot. All rights reserved.

---

**Automate Everything. Click Nothing.**
