# url_friendship_swarupa

This is a simple Media Gallery website.

## Goal (QR scan → photos show)
When someone scans your QR, it should open your GitHub Pages website and automatically load your photos from `gallery.json`.

## Add your photos
1. Put your photos/videos inside the `media/` folder.
2. Edit `gallery.json` and add entries for each file.

Example:
```json
{
  "items": [
    {"kind":"image","name":"My Photo","url":"media/myphoto.jpg"},
    {"kind":"video","name":"My Video","url":"media/myvideo.mp4"}
  ]
}
```

Note: GitHub has a file-size limit (100MB per file). For large videos, use Git LFS or host videos elsewhere.

## Upload to GitHub (Windows PowerShell)
From this folder:
```powershell
cd c:\frienship

git init

git add .

git commit -m "Initial commit"

git branch -M main

git remote add origin https://github.com/swarupa-1715/url_friendship_swarupa.git

git push -u origin main
```

## Enable GitHub Pages
On GitHub:
- Repo → **Settings** → **Pages**
- Source: **Deploy from a branch**
- Branch: **main** / **(root)** → Save

Your site URL becomes:
`https://swarupa-1715.github.io/url_friendship_swarupa/`

## If you see 404 (common fixes)
- Make sure you are opening the **GitHub Pages** URL (starts with `https://swarupa-1715.github.io/...`), not the `github.com/...` file view.
- In **Settings → Pages**, ensure:
  - Source = **Deploy from a branch**
  - Branch = **main**
  - Folder = **/(root)**
- Confirm you pushed your code (the repo must contain `index.html` at the root).
- Wait 1–5 minutes after enabling Pages (first deploy can take time).
- Repo should be **Public** for free Pages (private repos may need a paid plan).

## QR code
Open `qr.html` after you enable Pages. It shows a scannable QR for your Pages link.
