# Jungle Atmos Demo Lab v0.3.3

## Updates

- Fix the updater's install-path handling. The update helper now passes the existing app directory as NSIS's final, unquoted `/D=` parameter, preserving custom install paths, including paths with spaces.
- Keep anonymous HTTPS checks against the public updates-only feed; no GitHub login, OAuth consent, or stored credential is required.
- Verify the downloaded installer against `SHA256SUMS.txt` before applying it.
- Preserve all 21 moving-object scenes, the live per-object source-waveform panel, and the 7.1.2 room-map visualization.

The public release uploads only `JungleAtmos-Setup-x64.exe`, `SHA256SUMS.txt`, and this `RELEASE_NOTES.md`. GitHub also displays generated source-code ZIP/tar.gz entries; this tag's repository snapshot contains only the release-notes file, not application source code.

## Audio-format note

The app submits separately positioned objects through Windows Spatial Audio; it does not create a pre-encoded Dolby Atmos media file. Genuine Dolby Atmos output depends on a compatible licensed Windows Dolby Atmos for Home Theater renderer and the HDMI-connected AVR. Confirm the AVR's incoming format during playback. Multichannel PCM or stereo panning is not proof of Atmos decoding or exact 7.1.2 speaker routing.

## Update safeguard

The updater only applies the installer after its SHA-256 digest matches the published checksum manifest. Update checks are initiated from the app.
