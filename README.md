# Project Polaris — Decision Board

Project Polaris is a responsive, static prototype for managing pilot-to-scale decisions in life-sciences consulting. It is an information-dense operator console that models decision throughput, pilot triage, covenant deadlines, scale-contract gating, underwriting exposure, execution capacity, and an append-only audit view.

All organisations, people, contracts, and portfolio records are fictional illustrative data. The site is entirely client-side and safe to publish as a public GitHub Pages demo.

## Key features

- Eight hash-routed operating views with direct links.
- In-memory 72-pilot portfolio; filing a verdict recalculates WIP, decision rate, exit rate, and queue utilisation.
- Triage filters, disposition updates, readiness indicators, and audited mutations.
- Contract builder that refuses issuance below the 8/10 threshold and models procurement-covenant fallback.
- Responsive desktop and mobile layout, accessible focus path, keyboard route shortcuts (`1`–`8`), printable ELT pre-read, and an SVG favicon.
- Zero runtime dependencies, zero network calls, and no backend requirements.

## Screenshots

Add approved product screenshots to `assets/images/` before publishing. Suggested filenames:

```text
assets/images/decision-throughput.png
assets/images/triage-queue.png
assets/images/contract-builder.png
```

Then reference them here with relative paths, for example:

```md
![Decision Throughput](assets/images/decision-throughput.png)
```

## Technology stack

- HTML5
- Modern CSS (no preprocessors)
- Vanilla JavaScript (ES2020+)
- Local SVG favicon

No package manager, build step, framework, CDN, API key, authentication layer, or server is needed.

## Project structure

```text
Project-Polaris/
├── index.html              # GitHub Pages entry point
├── styles.css              # Responsive visual system
├── script.js               # App state, routing, and interactions
├── README.md
├── LICENSE
├── .gitignore
└── assets/
    ├── images/             # Optional screenshots
    ├── icons/
    │   └── favicon.svg
    └── logos/              # Reserved for approved brand assets
```

## Local preview

Open `index.html` directly in a current browser. Because all references are relative, it also works from a basic static server if you prefer one.

## GitHub Pages deployment (free)

1. Create a new public GitHub repository, for example `project-polaris`.
2. From this directory, initialise and push the repository using the commands below.
3. On GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Select branch **main**, folder **/(root)**, then click **Save**.
6. GitHub displays the public URL after deployment, generally:
   `https://YOUR-GITHUB-USERNAME.github.io/project-polaris/`

For a repository named `YOUR-GITHUB-USERNAME.github.io`, the public URL is instead `https://YOUR-GITHUB-USERNAME.github.io/`.

## Git commands

```bash
git init
git add .
git commit -m "Initial Commit"
git branch -M main
git remote add origin <REPOSITORY_URL>
git push -u origin main
```

Replace `<REPOSITORY_URL>` with the HTTPS or SSH repository URL copied from GitHub. The repository must be public for no-login access on the free GitHub Pages plan.

## Netlify deployment (free)

1. Create an account at [Netlify](https://www.netlify.com/).
2. Choose **Add new site → Import an existing project** and select the GitHub repository.
3. Set the publish directory to the repository root (`.`). Leave build command blank.
4. Click **Deploy site**.
5. Netlify assigns a public `https://*.netlify.app` URL. You can customise its subdomain in Site configuration.

You can alternatively drag this project folder into Netlify Drop; no build configuration is necessary.

## Vercel deployment (free)

1. Create an account at [Vercel](https://vercel.com/) and import the GitHub repository.
2. Select **Other** as the framework preset.
3. Leave the build command and output directory empty.
4. Click **Deploy**.
5. Vercel assigns a public `https://*.vercel.app` URL, available without login.

## Public access and hosting model

All three options publish static files over HTTPS. Anyone with the resulting URL can open it without an account or login, provided the GitHub repository / deployed project remains public. Project Polaris needs no database, API, server process, or environment secrets; GitHub Pages can host the final project in its entirety.

## Release checklist

- [ ] Update the copyright holder in `LICENSE` if needed.
- [ ] Confirm no proprietary or real-client data has been added to `script.js` or `assets/`.
- [ ] Optionally add approved screenshots under `assets/images/`.
- [ ] Run the link and asset checks below.
- [ ] Push to `main` and enable GitHub Pages from the root folder.
