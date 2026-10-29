# OMO Robo-Soccer League

A dashboard by **OMOTEC** for managing Codeavour Track 3 robo-soccer teams: registrations, training progress, student assessments, mock matches with a live scoreboard and timer, leaderboard, issues, and CSV export.

The whole app is one static file, `index.html`. It needs no build step and no server.

## Logins

Password for every account: `password123`

| Role | What it can do |
|---|---|
| Team Lead / Admin | Register, edit, rename and delete teams. Manage students. Reset or clear data. Upload a logo. |
| Executive Team | Read-only summary of every team and branch. |
| Trainer (one per trainer name) | Update training, assessments, matches and issues for their own teams. |

## Publish on GitHub Pages

1. Create a new repository on GitHub, for example `omo-robo-soccer-league`.
2. Upload every file in this folder to it, keeping the `.github/workflows/pages.yml` path.
3. Open **Settings → Pages** and set **Source** to **GitHub Actions**.
4. Push to `main`. The site appears at `https://<your-username>.github.io/omo-robo-soccer-league/`.

If you would rather not use Actions, set **Source** to **Deploy from a branch**, choose `main` and `/ (root)`.

## Important limits of this version

- Data is stored in each person's browser (`localStorage`). Registrations are not shared between devices.
- The password check and role rules run inside the page, so anyone who views the page source can read them. Do not use this for real student data.
- For a real multi-user deployment, move the data to a backend such as Supabase (PostgreSQL and authentication) and enforce permissions on the server.

## Files

- `index.html` – the application, including the OMOTEC logo
- `.github/workflows/pages.yml` – automatic deployment to GitHub Pages
- `.nojekyll` – tells GitHub Pages to serve the files as they are
- `.gitignore`
