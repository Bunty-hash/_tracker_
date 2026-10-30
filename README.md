# Cafe Stock Tracker

Single-page stock tracker for three outlets (Jurong, Orchard, Tampines), backed by Supabase.
Sign in, adjust stock and reorder levels, and copy a combined supplier order list.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app (no build step) |
| `vercel.json` | Static hosting config and security headers |
| `reference/` | Original first-draft SQL (already superseded by later changes; do not re-run) |
| `data/` | Original stock CSVs (reference only) |

## Deploy to Vercel

1. Push these files to the GitHub repo.
2. In Vercel: **Add New > Project**, import the repo.
3. Framework Preset: **Other**. Leave build and output settings empty. Click **Deploy**.

## Supabase

The app uses the project URL and **publishable** key set at the top of the script in `index.html`.
The publishable key is designed to be public. Access is protected by row-level security: only signed-in users can read or update stock.
Never put the `service_role` / secret key in this repo.

Users sign in with a username; the app maps it to `username@tracker.local` in Supabase Auth.
Initial users: priya (admin), dan, marcus, all with password `password`. **Change these before real use.**
Admins can add users from the Users tab.

