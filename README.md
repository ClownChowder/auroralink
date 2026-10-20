# Petal Link

Personal Android phone and Wear OS companion, formerly AuroraLink, for Bluetooth Buds status and companion setup.

Current release: [0.3.2-preview · Watch themes](https://github.com/ClownChowder/auroralink/releases/tag/v0.3.2-preview), published October 19, 2026.

## Current features

- All 16 Petal family palettes on both phone and watch, with matching connected-bloom launcher icons.
- Watch theme picker: **Match phone** (default) or an independent watch palette.
- The matching phone build publishes its selected palette through a persistent Wear OS DataItem. Valid phone themes are cached for disconnected use; unknown palette IDs and unsupported payload versions are ignored.
- Existing Bluetooth settings, package IDs, signing identity and `/auroralink/` message routes remain compatible. Buds control routes are unchanged.

## Installation and source

Install `auroralink.apk` on the Android phone. It includes the matching watch APK; `petal-link-watch.apk` is also attached separately for installation on a Wear OS watch. For phone-to-watch synchronization, use the matching phone and watch builds with a paired Wear OS setup and an available Wear OS Data Layer connection. The phone APK alone does not establish that the watch companion is installed or connected.

Keep the existing installation when updating: package and signing identity are unchanged. Allow APK installation for the installer you use if prompted. Physical watch installation and a live paired connection have not yet been verified for this release. Checksums are attached as `SHA256SUMS`.

Download the APK and full corresponding source ZIP from [Releases](https://github.com/ClownChowder/auroralink/releases). This repository indexes personal releases; use the explicitly attached `auroralink-source.zip` for the full app source. Automatic GitHub source archives contain only the release index.

## Validation and remaining testing

The 0.3.2-preview release reports phone/watch builds and lint passed, with 7 phone host tests, 3 watch host tests and 3 Android emulator tests passed. Emulator checks cover all 16 rendered palettes, single launcher selection, the picker and theme caching/override behavior. Existing non-blocking lint warnings remain.

**The emulator was a generic Android emulator at watch dimensions, not a paired Wear OS device.** Watch theme parity is implemented, but physical phone/watch usage, physical watch installation, live Data Layer synchronization and a live companion round trip remain unverified. No live transport or Buds control result is claimed.

## Obtainium

Keep source `https://github.com/ClownChowder/auroralink` and APK filename filter `^auroralink\.apk$`. The URL and asset name are retained for compatible updates.

Android package: `com.example.budswatchcontrol.preview`

Signing certificate SHA-256: `386f097ea7de3749f0b0cc87e433d0f8a8a70cebb1848d7e7cb4bd5f60cff2b4`

Future builds require the same signing key, increased versions, corresponding source and checksums. Obtainium detects published releases; it does not develop or build new versions. Signing keys, pairing tokens and personal app data are not published.

## Credits

See [CREDITS.txt](CREDITS.txt). Original notices and dependency attribution remain in the source and applicable artifacts. Samsung software and firmware are not redistributed; no endorsement is implied.
