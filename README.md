# Pluto Browser for All Data — releases

Public distribution point for the **All Data** build of Pluto Browser: the installers and the
update manifests the browser reads to know when a newer version exists. This build connects to
`https://pluto.alldataint.com`.

This repository holds **no source code**. It contains only:

- `standard/‹platform›.json` — small manifests the browser polls (version + download URL + sha256)
- GitHub **Releases** — the actual installer files, attached as release assets

## Channel and platforms

| Channel    | Manifest                       | Download                                          |
|------------|--------------------------------|---------------------------------------------------|
| `standard` | `standard/win-x64.json`        | `PlutoBrowserSetup.exe` (Windows x64)             |
| `standard` | `standard/mac-universal.json`  | `Pluto-Browser-‹version›-standard-mac-universal.dmg` (macOS, Intel and Apple Silicon) |

The macOS manifest points at the `.zip` (the updater payload); the `.dmg` is for a first install.

## Manifest shape

```json
{
  "version": "1.0.0",
  "url": "https://github.com/Juxtalabs/pluto-browser-alldata-releases/releases/download/v1.0.0/PlutoBrowserSetup.exe",
  "sha256": "‹64-hex lowercase over the installer›",
  "notes": "- What changed."
}
```
