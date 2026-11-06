# NEET PG 2030 Tracker

A single-file study tracker: topics by subject, spaced reviews, QBank progress and revision rounds. No installs, no accounts, no external files. Everything lives in `index.html`.

## Put it online (GitHub Pages)

1. Sign in to GitHub and create a new repository (for example `neet-tracker`).
2. Click **Add file → Upload files**, drag in every file (`index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png` and `README.md`), then **Commit changes**. Keep `index.html` in the root of the repository, not inside a folder.
3. Go to **Settings → Pages**. Under **Build and deployment**, set Source to **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, then **Save**.
4. Wait a minute or two. Your tracker will be live at:
   `https://<your-username>.github.io/<repository-name>/`
5. Open that link on your tablet or phone and add it to your home screen for quick access.

To update later, upload a new `index.html` with the same name and commit. GitHub replaces the old one.

Note: a public repository makes the page public. A private repository only gets Pages on a paid GitHub plan.

## Using the tracker

- **Overview:** the home page. It shows overall progress, topics to go, reviews due today, reviews done and QBank percentage, with a card per subject.
- **Subject pages:** each has a progress bar and a map of small squares, one per topic. Green is learned, amber is review due, empty is not yet. Tap a square to jump to that topic. The filter buttons show All, To do and Learned with counts.
- **Topics:** tap **Mark learned**, then **Mark R1 done**, **R2** and so on as each review comes due. Open **Reviews and extras** on a topic to undo a step or tick Feynman, Topic test, PYT, PYQs and Error log.
- **Due today:** lists every review that is due or late, oldest first, and shows batch revision reminders.
- **Plan:** the study method, plus backup and restore and the clear-all button.
- **Themes and text size:** the header has four colour themes (Forest, Midnight, Ember, Mint light) and A− / A+ buttons. Your choices are remembered.

## Install it like an app

After uploading all the files, open your site in Chrome on Android, tap the three-dot menu, then **Install app** (or **Add to Home screen**). It opens full screen and works offline. Your progress stays, because it uses the same browser storage as the website.

### Real APK (optional)

1. Go to pwabuilder.com, paste your site link and tap **Start**.
2. Choose **Package for stores**, then **Android**, then **Generate**.
3. Download the zip, unzip it and install the `.apk`. Allow "install unknown apps" if Android asks.

An APK made for a github.io address may show a thin address bar at the top. The Chrome install above does not.

## Your progress and backups

Progress is saved in your browser on each device. It does not sync between devices, and the GitHub address starts with empty progress.

To move progress to another device or browser:

1. On the old one, open **Plan** and tap **Save backup**. This downloads a `.json` file.
2. On the new one, open **Plan**, tap **Restore backup** and choose that file.

Clearing your browser data or site data deletes your progress, so save a backup now and then.

## Editing the content

Subjects and topics are listed near the top of the `<script>` section in `index.html`. Progress is stored by position, so adding topics at the end of a list is safe. Reordering or removing topics will mismatch saved progress.
