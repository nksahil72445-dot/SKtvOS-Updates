# SKtvOS Updates

Public APK downloads and the update feed for SKtvOS. This repository contains release information and APKs, not TV backups, account data, debugging keys, signing private keys or the application source workspace.

## Downloads

Use the published [Releases](https://github.com/nksahil72445-dot/SKtvOS-Updates/releases). APKs are optimized, non-debuggable **test builds** signed with the existing SKtvOS test identity. They have not completed production or full physical-TV validation.

## One-time setup for older SKtvOS installations

SKtvOS versions built with the old private repository URL cannot discover this new feed automatically. On the TV, open this public Releases page in a browser, download the initial public-feed APK and open it through the browser's downloads or a TV file manager. Android may ask to allow installation from that app. Install as an update over SKtvOS; do not uninstall the existing app.

This first step uses the internet and does not require USB or a GitHub account. The initial public-feed build is SKtvOS 3.2.2 / build 40.

## Future updates inside SKtvOS

After the public-feed build is installed:

1. Open **Settings → About → Software Update**.
2. Allow GitHub update access if it is off. Keep **Include test releases** on for these prereleases.
3. Choose **Check for updates**, then **Download & install** when a higher build is available.
4. Confirm Android's installation prompt. If requested, allow update installation from SKtvOS.

No GitHub sign-in is required. Checks and downloads run when requested. The updater verifies the download digest, application ID, signing certificate, Android compatibility and higher build number, and saves a launcher restore point before opening Android's installer. A local restore point is not an off-device backup.

If the installed build is already the newest one, the app reports no newer eligible update; it does not reinstall itself. Android retains control of installation approval.

## Release integrity

Each release includes `SHA256SUMS.txt` for its APK. A checksum helps detect a changed download; Android's signature checks and SKtvOS's comparison with the installed signing identity are also required. Files posted under other accounts or repositories are not the configured update feed.

## VPN setup note

3.2.2 includes provider selection and switching guidance. An Android always-on VPN pinned to the previous provider may still require a change in Android VPN settings before a different provider can connect. Installing this APK does not silently change VPN settings or disconnect a running VPN.
