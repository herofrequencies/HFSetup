# HFSetup

Public Windows installers for Hero Frequencies applications.

Running **Preset Manager** and **mintserver** check this repo for updates via [`versions.json`](versions.json).

## Preset Manager

**[Download HeroFrequenciesPresetManagerSetup.exe](https://github.com/herofrequencies/HFSetup/releases/download/v1.0.0.0/HeroFrequenciesPresetManagerSetup.exe)** ([release notes](https://github.com/herofrequencies/HFSetup/releases/tag/v1.0.0.0))

Setup for Hero Frequencies Preset Manager and the mintserver device service (`HeroMintServer`).

## Release checklist

When staging a new build:

1. Upload the new binary to `PresetManager/` and/or `mintserver/` (create `mintserver/` when needed), and/or attach it to a [GitHub Release](https://github.com/herofrequencies/HFSetup/releases).
2. Edit **`versions.json`** — bump `version` and `url` for each product you released:

```json
{
  "preset-manager": {
    "version": "1.0.0.0",
    "url": "https://github.com/herofrequencies/HFSetup/releases/download/v1.0.0.0/HeroFrequenciesPresetManagerSetup.exe",
    "notes": "Optional one-line summary"
  },
  "mintserver": {
    "version": "0.1.240",
    "url": "https://github.com/herofrequencies/HFSetup/releases/download/mintserver-0.1.240/mintserver.exe",
    "notes": ""
  }
}
```

3. Commit and push to `main`.

**Version format:** Preset Manager uses four-part semver (`1.0.2.0`). mintserver uses `0.1.{buildnum}` (must match `buildnum.txt` in the source tree).

No app code changes are required for each release — only this manifest and the binaries.
