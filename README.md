# FallSafe+ Home Scanning

An interactive web app that lets users walk through HDB rooms and identify fall hazards for elderly residents.

## Project Structure

```
fallsafe-ghpages/
├── index.html              ← Main app (loads images externally)
├── images/
│   ├── living-room.jpg     ← Living room photo
│   ├── dining-room.jpg     ← Dining room photo
│   ├── kitchen.jpg         ← Kitchen photo
│   └── bedroom.jpg         ← Bedroom photo
└── README.md               ← This file
```

---

## Deploy to GitHub Pages — Step by Step

### Step 1: Create a GitHub Account (skip if you have one)

Go to [github.com](https://github.com) and sign up.

---

### Step 2: Create a New Repository

1. Click the **+** button (top right) → **New repository**
2. Fill in:
   - **Repository name**: `fallsafe-home-scan` (or any name you like)
   - **Description**: `FallSafe+ Home Scanning Web App`
   - **Public** (must be public for free GitHub Pages)
   - ✅ Check **"Add a README file"**
3. Click **Create repository**

---

### Step 3: Upload the Files

1. On your new repository page, click **"Add file"** → **"Upload files"**
2. Drag and drop **all files and folders** from this `fallsafe-ghpages` folder:
   - `index.html`
   - `images/` folder (with all 4 .jpg files inside)
   - `README.md`
3. Scroll down, type a commit message like `Initial upload`
4. Click **"Commit changes"**

> **Important:** Make sure the `images` folder uploads as a folder, not just the files. If GitHub flattens it, create the folder first:
> - Click **"Add file"** → **"Create new file"**
> - Type `images/.gitkeep` as the filename
> - Click **"Commit new file"**
> - Then upload the 4 image files into that `images` folder

---

### Step 4: Enable GitHub Pages

1. Go to your repository page
2. Click **"Settings"** (tab at the top)
3. In the left sidebar, click **"Pages"**
4. Under **"Source"**, select:
   - **Branch**: `main`
   - **Folder**: `/ (root)`
5. Click **"Save"**
6. Wait 1–2 minutes for deployment

---

### Step 5: Access Your Live Site

Your site will be live at:

```
https://YOUR-USERNAME.github.io/fallsafe-home-scan/
```

Replace `YOUR-USERNAME` with your GitHub username and `fallsafe-home-scan` with your repository name.

GitHub will also show the URL on the Settings → Pages page once deployment is complete.

---

## Embedding in Another Website

To embed this app inside another webpage (e.g. one built with Kimi K 2.5), use an iframe:

```html
<iframe 
  src="https://YOUR-USERNAME.github.io/fallsafe-home-scan/" 
  width="450" 
  height="800" 
  style="border: none; border-radius: 8px; max-width: 100%;"
  allow="fullscreen"
></iframe>
```

Or, copy the contents of `index.html` directly into your page as a component. The only dependency is the `images/` folder being accessible at the correct relative path.

---

## Replacing Room Photos

To use your own room photos:

1. Take portrait-orientation photos (9:16 ratio works best)
2. Resize to **450px wide** for optimal loading
3. Save as `.jpg` and replace the files in the `images/` folder
4. Adjust hazard marker positions in `index.html` by editing the `x` and `y` values (percentages) in the `ROOMS` data object

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Images not loading | Make sure the `images/` folder is in the same directory as `index.html` |
| Page shows 404 | Check that GitHub Pages source is set to `main` branch, `/ (root)` |
| Changes not showing | GitHub Pages can take 2-5 minutes to update. Hard refresh with `Ctrl+Shift+R` |
| Looks wrong on mobile | The app is designed for portrait orientation. Rotate your phone to portrait mode |
