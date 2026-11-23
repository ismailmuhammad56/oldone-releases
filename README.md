# Oldone Releases

Public distribution point for the Oldone Minecraft mod (NeoForge, Minecraft 26.1.2).

This repository contains **only signed, public release files**. Source code, server software, and
signing keys are never published here.

## Layout

| Path | Contents |
|------|----------|
| `client/release.properties` | Signed description of the current client release (version, size, SHA-256) |
| `client/release.properties.sig` | Ed25519 signature of `release.properties` |
| `client/oldone-client-<version>.jar` | The client mod jar named by the release |
| `directory/servers.properties` | Signed list of Oldone servers |
| `directory/servers.properties.sig` | Ed25519 signature of `servers.properties` |

## How players use it

Players install NeoForge and the **Oldone bootstrap** once. On every start the bootstrap downloads
`client/release.properties`, verifies its signature against the release key pinned inside the
bootstrap, downloads the client jar when it changed, and checks its size and SHA-256 before loading
it. Files that are not signed by the Oldone release key are refused, and an older release never
replaces a newer one.

## Status

| Release | Sequence | Minecraft | SHA-256 of the client jar |
|---------|----------|-----------|---------------------------|
| 0.1.0   | 1        | 26.1.2    | `66a85ce10936333bba17182bd02b29ed51d751161983826038f5310c37aef6fd` |

The bootstrap is available on the [Releases](https://github.com/ismailmuhammad56/oldone-releases/releases) page.

Release signing key fingerprint source (public key, Base64 X.509):
`MCowBQYDK2VwAyEAkOlAnjF+JZWwDAI4+esUWkVztvVeHhV3dBpUVs77kUw=`
