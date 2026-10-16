# Jungle Atmos Demo Lab v0.3.2

## Updates

- Change the in-app updater to use the separate public binaries-only feed at `waderaider/jungle-atmos-updates`; the source repository remains private.
- Remove the private GitHub device-flow and stored-token dependency from the updater. An explicit update check now uses anonymous HTTPS requests.
- Continue verifying the installer against the published SHA-256 manifest before the helper applies it.
- Preserve the 21-scene catalog, live per-object source-waveform panel, and 7.1.2 room-map visualization.

The public GitHub release contains only `JungleAtmos-Setup-x64.exe`, `SHA256SUMS.txt`, and this `RELEASE_NOTES.md`. GitHub also generates Source code ZIP/tar.gz entries; the repository snapshot behind those archives contains only the release-notes file and no application source code.

## Audio-format note

The app submits separately positioned objects through Windows Spatial Audio; it does not create a pre-encoded Dolby Atmos media file. Genuine Dolby Atmos output depends on a compatible licensed Windows Dolby Atmos for Home Theater renderer and the HDMI-connected AVR. Confirm the AVR's incoming format during playback. Multichannel PCM or stereo panning is not proof of Atmos decoding or exact 7.1.2 speaker routing.

## Update safeguard

The updater only applies the installer after its SHA-256 digest matches the published checksum manifest. Update checks are initiated from the app.
