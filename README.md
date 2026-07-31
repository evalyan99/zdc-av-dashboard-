# ZDC 2026 Fall · AV Dashboard

Hosted AV projection dashboard for the ZDC 2026 Fall event.

## Live URL

Once deployed to GitHub Pages, the dashboard is available at:

```
https://<your-github-username>.github.io/<repo-name>/
```

## How it works

- `index.html` — redirects the root URL to `dashboard.html`
- `dashboard.html` — the full AV dashboard; auto-fetches live session data from Box on every page load

The dashboard fetches `zdc-2026-fall-av-data.json` directly from a Box shared link. No login required. The AV vendor just opens the URL and refreshes the page to see the latest data.

## Updating data

1. Open the admin page (`Admin/zdc-2026-fall-av-admin.html`) from Box Desktop
2. Load the current JSON, make changes, click **Export data file**
3. Replace `Data/zdc-2026-fall-av-data.json` in Box (drag the downloaded file into the Box Desktop folder)
4. Box syncs automatically — the dashboard reflects the update on the next page refresh

## Deploying

### First time

1. Create a new GitHub repository (public)
2. Upload `index.html` and `dashboard.html` from this folder
3. Go to **Settings → Pages → Source → Deploy from branch → main → / (root)** → Save
4. GitHub will publish the site — the URL appears at the top of the Pages settings page within ~60 seconds

### Updating the dashboard

Re-upload `dashboard.html` to the repository. The live URL stays the same.
