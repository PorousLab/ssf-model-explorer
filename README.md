# SSF Steady-State Removal Model Explorer

Interactive visualization of the two-site kinetic model for pathogen removal in slow sand filtration, based on Schijven et al. (2013).

## 🚀 Quick Deploy (Recommended)

### Option 1: Netlify (Easiest - 2 minutes)

1. Go to [netlify.com](https://netlify.com) and sign up/login (free)
2. Drag and drop this **entire folder** onto the Netlify dashboard
3. Wait for build to complete
4. Your app is live! You'll get a URL like `https://random-name.netlify.app`

To customize the URL: Site settings → Domain management → Add custom domain

### Option 2: Vercel (Also Easy)

1. Push this folder to a GitHub repository
2. Go to [vercel.com](https://vercel.com) and sign up with GitHub
3. Click "New Project" → Import your repo
4. Click Deploy (Vercel auto-detects Vite)
5. Live at `https://your-project.vercel.app`

### Option 3: GitHub Pages (Recommended for GitHub users)

This project includes a GitHub Actions workflow for automatic deployment.

**Steps:**
1. Create a new repository on GitHub (e.g., `ssf-model-explorer`)
2. Push this folder to your repo:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/ssf-model-explorer.git
   git push -u origin main
   ```
3. Go to your repo → **Settings** → **Pages**
4. Under "Build and deployment", set **Source** to **GitHub Actions**
5. Wait 1-2 minutes for the workflow to complete
6. Your site is live at: `https://YOUR_USERNAME.github.io/ssf-model-explorer/`

The site auto-updates every time you push changes to main!

## 💻 Local Development

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📁 Project Structure

```
ssf-model-explorer/
├── index.html          # Entry HTML
├── package.json        # Dependencies
├── vite.config.js      # Vite configuration
├── tailwind.config.js  # Tailwind CSS config
├── postcss.config.js   # PostCSS config
└── src/
    ├── main.jsx        # React entry point
    ├── App.jsx         # Main SSF Model component
    └── index.css       # Tailwind imports
```

## 📚 Reference

Based on: Schijven et al. (2013) — "Removal of microorganisms by slow sand filtration"

The model implements the steady-state solution for the two-site kinetic attachment-detachment model with first-order inactivation.
