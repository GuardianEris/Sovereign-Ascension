# Sovereign Ascension

A private, mobile-friendly real-life RPG Progressive Web App. No subscription, account, tracking scripts or cloud backend.

## Publish free with GitHub Pages

1. Create a free account at https://github.com and create a new **public** repository named `sovereign-ascension`.
2. Extract the ZIP. Upload the **contents** of the `sovereign-ascension` folder (not the enclosing folder) into the repository's root. Commit the files.
3. In the repository, go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
4. After deployment, open `https://YOUR-USERNAME.github.io/sovereign-ascension/`. Allow a few minutes for publishing.
5. On iPhone, open the link in **Safari**, tap **Share → Add to Home Screen → Add**. The installed app should launch in its own window. Other browsers/platforms may offer an Install App action.

**Privacy:** The website source code is public on GitHub Pages, but your quests, workout logs and other progress remain in that device/browser's localStorage and are not uploaded to GitHub. Do not upload your JSON backup to the public repository.

## Data and backups

Use **Settings → Export JSON Backup** regularly, especially before clearing browser data or switching devices. To restore, use **Import JSON Backup**. Import replaces the entire current save, so export it first. Progress does not automatically sync between devices or browsers. If your browser is in private mode or clears website storage, progress may disappear. The PWA's offline cache stores app files, not a cloud copy of your data.

## Using the app

- **Quests:** Choose a calendar day. Monday–Sunday quests rotate by date. Choose Recovery, Normal or High Energy. Check tasks and claim XP. Previously claimed XP is preserved when changing difficulty.
- **Hydration:** Tap +8 or +16 oz. Change the default target in Settings. The target is a flexible tracker, not medical advice.
- **Fitness:** Record exercises, weights, sets, reps or minutes, and notes. Logging a workout does not grant XP separately; claim the movement quest for that day's XP.
- **Progress:** View game stats, rank ladder and achievements.
- **Bosses:** Weekly battles unlock when enough qualifying quests are claimed during the Monday–Sunday week. Boss rewards are claimed once per boss per week.

## Local testing

Double-clicking `index.html` may show the interface, but offline installation requires HTTP(S). To test locally with Python, open a terminal in this folder and run `python3 -m http.server 8000`, then visit `http://localhost:8000`. For phone installation, publish to an HTTPS host such as GitHub Pages.

## Notes

- This app uses no paid services or external dependencies.
- This is a first version, not medically personalized guidance. Use comfortable exercise intensity and follow professional advice when needed.
- To update app code, upload changed files to GitHub. If an old version persists, refresh/reopen the app. For future updates, increment the cache name in `sw.js`.
