# Research Hub - Personal RSS Reader

A mobile-friendly RSS reader for criminal justice, macroeconomics, and demography research.

## Features
- 📱 Mobile-first design (works great on phones)
- 🏷️ Organized by category (Criminal Justice, Macro, Demography, California, Journals)
- 🔍 Keyword filtering
- 📴 Works offline (caches articles locally)
- 🏠 Add to home screen like an app

## Free Deployment Options

### Option 1: GitHub Pages (Recommended)
1. Create a GitHub account at github.com (free)
2. Create a new repository (click the + button, "New repository")
3. Name it something like `research-hub`
4. Upload all three files (index.html, manifest.json, sw.js)
5. Go to Settings → Pages → Source → select "main" branch → Save
6. Your site will be live at: `https://YOUR-USERNAME.github.io/research-hub`

### Option 2: Netlify Drop (Easiest)
1. Go to https://app.netlify.com/drop
2. Drag and drop the folder containing these files
3. Done! You'll get a random URL like `random-name-123.netlify.app`
4. (Optional) Create a free account to keep the site permanently and get a custom name

### Option 3: Glitch
1. Go to glitch.com and sign in with Google/GitHub
2. Click "New Project" → "glitch-hello-website"
3. Delete the existing files and upload these three files
4. Your site is live at the URL shown in the top left

## Adding to Home Screen

### iPhone/iPad
1. Open the site in Safari
2. Tap the Share button (square with arrow)
3. Scroll down and tap "Add to Home Screen"
4. Name it "Research Hub" and tap Add

### Android
1. Open the site in Chrome
2. Tap the three-dot menu
3. Tap "Add to Home Screen" or "Install App"

## Customizing Feeds

To add or remove feeds, edit the `FEEDS` object near the top of the `<script>` section in `index.html`. Each feed needs:
- `name`: Display name for the source
- `url`: The RSS feed URL

Example:
```javascript
{ name: 'My New Source', url: 'https://example.com/feed.rss' },
```

## Troubleshooting

**Some feeds don't load:**
The app uses a free CORS proxy (allorigins.win) to fetch feeds. Some RSS feeds may be incompatible or temporarily unavailable. The app will gracefully skip failed feeds.

**Articles seem stale:**
Tap the refresh button (↻) in the bottom right to force a refresh. Articles are cached for 30 minutes.

**Want to add more feeds?**
Edit the FEEDS object in index.html. You can find RSS feed URLs by:
- Looking for the orange RSS icon on websites
- Adding `/feed` or `/rss` to website URLs
- Searching "[website name] RSS feed"
