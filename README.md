# prodinfo.io Desktop — Downloads

This repository holds only built binaries and the auto-updater manifest for **prodinfo.io
Desktop**. It contains no source code — the app is developed in a private repository and its
release CI publishes signed installers and `latest.json` here so they can be downloaded and
verified without requiring access to the private source repo.

## Download

See the [latest release](../../releases/latest) for the current Windows (`.msi`), macOS
(`.dmg`), and Linux (`.deb` / `.AppImage`) installers.

## Auto-update

The desktop app checks `releases/latest/download/latest.json` in this repository and verifies
every artifact's signature against a public key embedded in the app before installing an update.
