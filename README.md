# Aither App Dounloads

**One download for the entire Aither desktop ecosystem.**

Aither App Dounloads is the central distribution repository for **Aither Apps**, the single desktop hub for the Aither suite.

## What you download

Install **Aither Apps** once. From the Aither Apps desktop launcher you can open:

- Aither Weather
- Aither Clock
- Aither Notes
- Aither Maps
- Aither Calculator
- Aither Dashboard
- Aither Files
- Aither Mail
- Aither Gaming
- Aither AI
- Aither Web

There are **no separate desktop downloads required for each app**. The launcher opens the web deployments in dedicated desktop windows, so the individual Aither apps can update independently.

## Platforms

The release workflow builds the Aither Apps desktop launcher for:

- Windows — `.exe` installer
- macOS — desktop build
- Linux — `.AppImage`

All official installers are published through the **Releases** section of this repository.

## Build source

The desktop launcher is maintained in [`AitherForge/AitherApps`](https://github.com/AitherForge/AitherApps/tree/main/desktop).

This repository is the distribution hub; the launcher source remains in Aither Apps.

## Not included

- **AitherTech** is intentionally excluded from the desktop suite.
- **AitherBackend** is infrastructure and is not a desktop application.
- **Aither Admin / AitherError404** remains hidden and is not exposed as a normal download or launcher app.

## Release process

The GitHub Actions workflow in `.github/workflows/release.yml` builds all supported desktop targets directly from the Aither Apps repository and publishes the installers to this repository's GitHub Releases.

### Manual release

1. Open **Actions**.
2. Select **Build Aither Apps Desktop**.
3. Choose **Run workflow**.
4. Enter the version, such as `1.0.1`.
5. Run the workflow.
6. The resulting Windows, macOS, and Linux installers are attached to the release.

## Development

To develop the desktop launcher itself, work in `AitherForge/AitherApps/desktop`:

```bash
cd desktop
npm install
npm start
npm run dist
```

The goal is simple: **one Aither desktop installation, every Aither app.**
