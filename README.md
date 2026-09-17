# prodinfo.io Desktop — Downloads

This repository holds only built binaries and the auto-updater manifest for **prodinfo.io
Desktop**. It contains no source code — the app is developed in a private repository and its
release CI publishes signed installers and `latest.json` here so they can be downloaded and
verified without requiring access to the private source repo.

## Download and install

Open the [latest release](../../releases/latest) and download the installer for your operating
system. First-time installation is manual; after that, Desktop checks for signed updates when it
starts.

### macOS (Apple Silicon and Intel)

1. Download the universal `.dmg` file.
2. Open it and drag **prodinfo.io** to **Applications**.
3. Open **prodinfo.io** from Applications.

If macOS blocks the first launch, open **System Settings → Privacy & Security**, then choose
**Open Anyway** for prodinfo.io. This confirmation is required only for the first launch.

### Windows

1. Download the `.msi` installer.
2. Open the downloaded file and follow the Windows Installer prompts.
3. Start **prodinfo.io** from the Start menu.

If Windows shows a first-run security prompt, confirm that you downloaded the installer from this
repository's latest release before continuing.

### Linux (Debian/Ubuntu)

1. Download the `.deb` package.
2. Install it from a terminal:

   ```bash
   sudo apt install ./prodinfo.io_<version>_amd64.deb
   ```

3. Start **prodinfo.io** from the application menu or run `prodinfo.io` from a terminal.

### Linux (other distributions)

1. Download the `.AppImage` file.
2. Make it executable and run it:

   ```bash
   chmod +x prodinfo.io_<version>_amd64.AppImage
   ./prodinfo.io_<version>_amd64.AppImage
   ```

## First run

1. Open **Settings** and configure an AI model provider. You can use a local Ollama model or a
   supported hosted provider.
2. Create a job from a product page, PDF, or spreadsheet.
3. Review the extracted records, select an output route, and export to a file or connected target.

For pages that require sign-in, MFA, or block direct scraping, use **Open capture browser** when
creating a web job. Sign in and navigate there, then capture the rendered product page; browser
cookies and credentials are not included in the captured data.

## Updates

Desktop checks the `latest.json` updater manifest in this repository and verifies signed update
artifacts before installing them. If automatic update is unavailable on your platform, download
the current installer from the [latest release](../../releases/latest).

## Auto-update

The desktop app checks `releases/latest/download/latest.json` in this repository and verifies
every artifact's signature against a public key embedded in the app before installing an update.
