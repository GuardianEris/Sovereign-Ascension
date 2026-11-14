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


## Version 2: Custom quests and daily planner

- **Planner tab:** Four sections matching a daily organization checklist, with typed tasks, five rotating statuses, optional daily recurrence, and carry-forward for unfinished one-time tasks.
- **Quests tab:** Create a custom objective (such as Make bed) in a quest category. Choose Daily or Selected date only. Tick the objective and claim 5 bonus XP.
- Custom objectives are optional and do not block built-in quest completion. A maximum of five custom quest rewards per day count toward XP, preventing accidental unlimited XP farming.
- Both features save in the same browser storage and are included in JSON export/import backups. Existing version 1 progress is preserved when updating website files.

### Update your live GitHub Pages site

Upload the contents of the `sovereign-ascension` folder to the **root** of the same repository, replacing files with matching names (`app.js`, `style.css`, `sw.js`, etc.). Do **not** delete the repository or clear Safari website data. The service worker cache name has been updated to v2. If the old version remains visible, close and reopen the website, then refresh once online. Export a backup before updating as a precaution.


## Version 2.1 — specific weekday planner tasks
In Planner, choose **One time**, **Daily**, or **Specific days** for each new task. For Specific days, choose one or more weekdays. For example, “Take garbage out” → Personal Must Finish → Specific days → Wed. These tasks appear on selected weekdays starting with the creation date, and completion status is stored separately per date. Weekly tasks are excluded from Carry Forward and never earn XP. Existing daily and one-time tasks remain supported.

### Update an existing GitHub Pages installation
Back up progress using Settings → Export JSON first. Extract the ZIP and upload the files *inside* the sovereign-ascension folder into the root of your existing repository, replacing the same-named files and committing changes. Keep the same website URL and browser storage. Do not clear Safari site data. If an old version remains, wait for the GitHub Pages deployment and reload; the service worker cache name has changed for this release.


## Version 2.2 — Personalization

Use **Builder** to customize each weekday's workout, recovery routine, cleaning, skincare, and mental quests. Add/edit/remove objectives and update quest titles. Use **Settings** to rename your character and change hydration targets. In **Fitness**, type an optional custom exercise name to log exercises not in the presets. Each device has its own local save; no shared login or live co-op synchronization. Export JSON backups before upgrades.

## Version 2.3 — Workout and objective ordering

In Builder, use ↑ Up and ↓ Down to reorder objectives within any weekday and category. The chosen order appears in Quests and Fitness. Unclaimed checkmarks are moved with their objectives where applicable; claimed XP is retained. Existing locally saved data uses the same storage key and backup format. Export a JSON backup before updating.


## Version 2.4 — The Royal Polish

- Larger, labeled **Move up** and **Move down** buttons in the Builder, with clearer touch targets.
- Harmonized purple inputs, select menus, and text areas instead of harsh near-black fields.
- Improved spacing and mobile-friendly two-column Builder controls.
- Versioned script and stylesheet URLs plus a new offline cache identifier to help browsers load updated releases.
- No changes to the saved-data schema, XP, workout ordering logic, or existing planner tasks. Export a JSON backup before updating.
