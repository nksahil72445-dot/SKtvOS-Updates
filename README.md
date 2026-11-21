# SKtvOS Updates

**Current test release: [SKtvOS 3.2.4 / build 44](https://github.com/nksahil72445-dot/SKtvOS-Updates/releases/tag/v3.2.4-build44).** Refined glass focus, Android9 signing-reader fix and one-button software updates. Not yet physically tested on TV.

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

Each release includes an APK checksum file (`SHA256SUMS.txt` on older releases; `PUBLIC-SHA256SUMS.txt` on build 44). A checksum helps detect a changed download; Android's signature checks and SKtvOS's comparison with the installed signing identity are also required. Files posted under other accounts or repositories are not the configured update feed.

## VPN setup note

3.2.4 shows available connection information and an Open VPN app chooser, without a preferred-provider setting. Android always-on VPN settings may still restrict switching providers. Installing the APK does not change those device settings.

Build43 uses the older updater reader: install build44 once through Android installation without uninstalling. Later releases can use the corrected in-app updater.
