# Garage Log

A maintenance log for my cars. Anyone with the link can view it. Only I can edit, and edits save straight to `data/garage.json` in this repo.

## Setup

1. Create a public repo named `garage-log` and upload `index.html`, `README.md` and the `data` folder.
2. In the repo, go to **Settings → Pages**, set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. If the site is on `<username>.github.io/garage-log/`, the app finds the repo on its own. If you use a custom domain, open `index.html`, find `CONFIG` near the top of the script, and set `owner` to your GitHub username.

## Turning on editing

1. On GitHub, go to **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Under **Repository access**, choose **Only select repositories** and pick `garage-log`.
3. Under **Permissions → Repository permissions**, set **Contents** to **Read and write**.
4. Generate the token, open the site, select **Edit**, and paste it in.

The token is stored only in that browser. Select **Done editing** to remove it from the device. Repeat on each device you edit from (phone, laptop).

## How it works

- Every save is a commit to `data/garage.json`, so the repo history doubles as a change log, and any mistake can be reverted on GitHub.
- **Coming due** compares each schedule item with the last service entry linked to it. An item is due at whichever comes first, its miles or its months.
- Logging an entry with a higher mileage updates the odometer automatically.
- **Mark done** on a work item turns it into a service entry.
- After you save, visitors may see the old data for a minute or two while GitHub Pages refreshes.

## Design

The styling follows the public Porsche Design System tokens (monochrome canvas, near-black primary, grey surfaces, restrained status colors). Inter stands in for Porsche Next, which is licensed. The page uses no Porsche logos, crest or wordmark.
