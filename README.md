# Seed Garden

Your personal idea journal — powered by Firebase, hosted on GitHub Pages.

## Files

```
index.html        ← the whole app
manifest.json     ← PWA manifest
sw.js             ← service worker (offline support)
icons/
  icon-192.png
  icon-512.png
```

## Deploy to GitHub Pages

1. Go to github.com and sign in
2. Click "+" → "New repository"
3. Name it `seedgarden`, set to Public, click "Create repository"
4. On the next screen click "uploading an existing file"
5. Drag all these files (and the icons folder) into the upload area
6. Click "Commit changes"
7. Go to Settings → Pages → Source: "Deploy from branch" → Branch: main → Folder: / (root)
8. Click Save

Your app will be live at: https://YOURUSERNAME.github.io/seedgarden

Takes 1-2 minutes to go live.

## Fix Firebase Auth Domain

After deploying, you need to add your GitHub Pages URL to Firebase's allowed domains:

1. Go to Firebase console → Authentication → Settings → Authorized domains
2. Click "Add domain"
3. Add: YOURUSERNAME.github.io
4. Click Add

Without this step, Google Sign-In will be blocked.

## Install on Pixel (Android)

1. Open Chrome on your Pixel
2. Go to your GitHub Pages URL
3. Sign in with your Google account
4. Tap the three-dot menu → "Add to Home screen"
5. Tap Add

Seed Garden now lives on your home screen like a native app.
When browsing, tap Share → "Seed Garden" to save any page directly.

## Mac Bookmarklet

Copy this and create a bookmark in Chrome with it as the URL:

javascript:(function(){var t=prompt('Idea title:',document.title||'');if(!t)return;window.open('https://YOURUSERNAME.github.io/seedgarden?title='+encodeURIComponent(t));})();

## Backup

Click "backup ↓" in the toolbar to download all your ideas as a JSON file.
Your data also lives safely in Firebase Firestore — no data loss if you clear your browser.
