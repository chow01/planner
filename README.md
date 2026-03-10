# listkeeper

A mobile-friendly personal planner that lives entirely in your browser. No server, no account, no sync — just a single HTML file hosted for free on GitHub Pages.

---

## What it does

**Input format:** `[date] [list] [item + description]`

- `12feb with_friends Avengers at 6pm with the FCC crew`
- `today work Submit the Q1 report by noon`
- `na grocery Oat milk and sourdough`

The first two spaces are the separators. Everything after the second space is the item text.

**Date formats accepted:**
| Input | Meaning |
|---|---|
| `12feb` | February 12 (current year) |
| `feb12` | same |
| `today` | today |
| `tomorrow` | tomorrow |
| `na` | no date — appears in list only, not calendar |

**Lists** appear as collapsible groups below the input. Each item shows its creation timestamp on the right.

**Calendar** shows today + the next 6 days by name (e.g. "mon · 12 feb"), then any future dates that have items. All calendar days default to expanded. Days with `na` as date don't appear on the calendar.

---

## Setup on GitHub Pages (free hosting, ~5 minutes)

### Step 1 — Create a GitHub account
If you don't have one: [github.com/signup](https://github.com/signup)

### Step 2 — Create a new repository
1. Go to [github.com/new](https://github.com/new)
2. Name it anything, e.g. `listkeeper`
3. Set it to **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

### Step 3 — Upload the file
1. In your new repo, click **Add file → Upload files**
2. Drag in `index.html` from this folder
3. Scroll down, click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to your repo's **Settings** tab
2. In the left sidebar click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Set branch to `main`, folder to `/ (root)`
5. Click **Save**

### Step 5 — Get your URL
After ~60 seconds, refresh the Pages settings page. Your URL will appear:
```
https://YOUR-USERNAME.github.io/listkeeper/
```

Open it on your phone, add it to your home screen:
- **iPhone:** Safari → Share → "Add to Home Screen"
- **Android:** Chrome → ⋮ menu → "Add to Home screen"

---

## Data storage

All data is saved in your browser's `localStorage`. This means:
- ✅ Works offline after first load
- ✅ No account or login needed
- ⚠️ Data is tied to that browser/device (not synced across devices)
- ⚠️ Clearing browser data will erase your lists

To back up your data: open the browser console (`F12` or dev tools) and run:
```js
copy(localStorage.getItem('listkeeper'))
```
Paste it somewhere safe. To restore, run:
```js
localStorage.setItem('listkeeper', '<paste here>')
```

---

## Updating the app

If you want to replace the file with a newer version:
1. Go to your repo on GitHub
2. Click on `index.html`
3. Click the pencil ✏️ icon to edit, or delete and re-upload
4. Commit the change — GitHub Pages updates in ~30 seconds
