# Vercel Deployment Guide for HTML Portfolio

## 📋 Project Analysis

Your project contains:
- **6 HTML files**: portfolio.html, bootstrap1.html, bootstap4.html, coursal.html, task4.html, tasl2.html
- **4 Image files**: edgar.jpg, image.jpg, images.jpeg, profile.jpg
- **All files use Bootstrap CDN** (no local dependencies needed)

## 🚀 Deployment Steps

### Method 1: Deploy via Vercel CLI (Recommended)

1. **Install Vercel CLI** (if not already installed):
   ```bash
   npm install -g vercel
   ```

2. **Login to Vercel**:
   ```bash
   vercel login
   ```

3. **Deploy your project**:
   ```bash
   vercel
   ```
   - Follow the prompts
   - It will ask if you want to deploy to production (type `Y`)

4. **For production deployment**:
   ```bash
   vercel --prod
   ```

### Method 2: Deploy via GitHub (Easiest)

1. **Push your code to GitHub** (you already did this):
   ```bash
   git add .
   git commit -m "Ready for Vercel deployment"
   git push origin main
   ```

2. **Go to Vercel Website**:
   - Visit: https://vercel.com
   - Sign up/Login with your GitHub account

3. **Import Your Repository**:
   - Click "Add New Project"
   - Select your repository: `abiahtech06-svg/Portfolio`
   - Click "Import"

4. **Configure Project** (Vercel auto-detects HTML):
   - Framework Preset: **Other** (or leave as default)
   - Root Directory: `./` (default)
   - Build Command: Leave empty (not needed for static HTML)
   - Output Directory: Leave empty (default)

5. **Deploy**:
   - Click "Deploy"
   - Wait for deployment to complete
   - Your site will be live at: `https://your-project-name.vercel.app`

## 📁 File Structure

```
/
├── index.html          (Navigation page - entry point)
├── portfolio.html      (Main portfolio)
├── bootstrap1.html     (Form page)
├── bootstap4.html      (Edgar Allan Poe page)
├── coursal.html        (Carousel page)
├── task4.html          (Movie Store)
├── tasl2.html          (MyApp navigation)
├── vercel.json         (Vercel configuration)
├── edgar.jpg           (Image)
├── image.jpg           (Image)
├── images.jpeg         (Image)
└── profile.jpg         (Image)
```

## ✅ What Vercel Will Do

- Automatically serve all HTML files
- Serve images from the root directory
- Handle routing for all your pages
- Provide HTTPS by default
- Give you a custom domain option

## 🔗 Accessing Your Pages

After deployment, you can access:
- Main page: `https://your-project.vercel.app/`
- Portfolio: `https://your-project.vercel.app/portfolio.html`
- Form: `https://your-project.vercel.app/bootstrap1.html`
- Edgar Poe: `https://your-project.vercel.app/bootstap4.html`
- Carousel: `https://your-project.vercel.app/coursal.html`
- Movie Store: `https://your-project.vercel.app/task4.html`
- MyApp: `https://your-project.vercel.app/tasl2.html`

## 🎯 Quick Deploy Commands

```bash
# One-time setup
npm install -g vercel
vercel login

# Deploy to preview
vercel

# Deploy to production
vercel --prod
```

## 📝 Notes

- All your images are in the root directory, so paths like `src="edgar.jpg"` will work correctly
- Bootstrap is loaded from CDN, so no build process needed
- The `vercel.json` file ensures proper static file serving
- The `index.html` provides a nice navigation page for your portfolio

## 🆘 Troubleshooting

**If images don't load:**
- Make sure all image files are committed to Git
- Check that image paths in HTML match the actual filenames

**If pages return 404:**
- Make sure all HTML files are in the root directory
- Check that filenames match exactly (case-sensitive)

**If deployment fails:**
- Make sure you're in the correct directory
- Check that `vercel.json` is valid JSON

