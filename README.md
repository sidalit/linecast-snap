<div align="center">

# linecast

**Weather, tides, the sun, the moon, maps and the sky in your terminal.**

[![linecast](https://snapcraft.io/linecast/badge.svg)](https://snapcraft.io/linecast)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64, arm64](https://img.shields.io/badge/Architectures-amd64%20%7C%20arm64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [linecast](https://github.com/ashuttl/linecast), seven live terminal apps for weather, radar, tides, sunshine, the Moon, the night sky and maps, built on free public data.

</div>

---

## Getting Started

<a href="https://snapcraft.io/linecast"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install linecast
linecast location set "Portland, Maine"
linecast weather
```

The other apps are `linecast radar`, `tides`, `sunshine`, `moon`, `sky` and `maps`. Press `?` in any view for its keys, or add `--print` for one static frame.

## Configure

There are no `snap set` options. Settings commands such as `linecast location`, `linecast units` and `linecast language` save to `~/snap/linecast/current/.config/linecast/config.json`, and cached data stays under `~/snap/linecast/current/.cache/linecast`.

| Setting | Accepted values | Default |
| --- | --- | --- |
| `linecast location` | `set "Portland, Maine"`, `set 44.54,-68.42` | Guessed from your IP address |
| `linecast units` | `metric`, `imperial`, `auto` | `auto` |
| `linecast language` | A [supported language](https://github.com/ashuttl/linecast/blob/main/docs/languages.md), `auto` | `auto` |
| `linecast clock` | `12`, `24`, `auto` | `auto` |

Run a setting command alone to see its value. The upstream [configuration guide](https://github.com/ashuttl/linecast/blob/main/docs/configuration.md) lists the other settings and environment variables.

## Limitations

- Settings from a host installation in `~/.config/linecast` are not read.
- Without a saved location, the IP-based guess can be far off on a VPN or over SSH.

## Build

```bash
git clone https://github.com/sidalit/linecast-snap.git
cd linecast-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/linecast-snap/issues).
- **Application bugs:** [report them upstream](https://github.com/ashuttl/linecast/issues).

## License

Snap packaging: [MIT](LICENSE).
