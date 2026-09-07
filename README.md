# Klicsy releases

Installers, auto-update payloads, signatures, and `latest.json` for
[Klicsy](https://klicsy.inokulum.co), the privacy-first, bring-your-own-key
AI screen assistant for macOS and Windows.

This repository holds **release artifacts only**. Source code lives in a
separate private repository; the GitHub Releases here are produced by its CI.

## Install

Grab the newest release from the
[Releases page](https://github.com/jaddaccache-debug/klicsy-releases/releases/latest).

- **macOS**: open the `.dmg` and drag `Klicsy.app` to Applications. Builds are
  ad-hoc signed and not notarized, so on first launch right-click the app and
  choose **Open**, or run:

  ```bash
  xattr -dr com.apple.quarantine /Applications/Klicsy.app
  ```

- **Windows**: run the `Klicsy_<version>_x64-setup.exe` installer.

## Auto-update

Klicsy checks `releases/latest/download/latest.json` in this repository once a
day. Updates are verified with a minisign signature whose public key is
compiled into the app, so a release here cannot be installed unless it was
signed with the maintainer's private key.
