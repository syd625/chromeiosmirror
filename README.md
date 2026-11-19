# chromeiosmirror
[README.md](https://github.com/user-attachments/files/35065273/README.md)
# MirrorBridge — ChromeOS / iPhone browser sharing

A standalone static HTML app. No backend, extensions, or Linux required.

## Deploy

Host `index.html` on an HTTPS static host such as GitHub Pages (Settings > Pages > Deploy from a branch). Open the resulting HTTPS address on both devices. Opening a local HTML file may not allow camera/screen capture.

## Connect

1. Chromebook: select **Chromebook · View**, click **Create connection offer**.
2. Copy the entire offer to the iPhone (a trusted message or note works).
3. iPhone: open the same HTTPS page in Safari, select **iPhone · Share**, paste the offer.
4. Select **Share screen** if available, or **Share camera instead**.
5. Copy the generated answer back to the Chromebook.
6. Paste into **Answer**, click **Connect to iPhone**.

The stream is peer-to-peer via WebRTC where the network permits it. Public Google STUN is used to discover network candidates; no TURN relay is included. Some managed networks will block connectivity. Pairing text includes network information: only share it with your own devices.

## Limits

- Screen capture depends on iOS version, Safari support, permissions and policies. It may not be available or may not capture the entire iPhone display.
- Camera fallback captures camera view, **not** the phone's display.
- No native USB mirroring or remote iPhone control.
- Manual pairing; no server, database, or cloud video storage.
- Screenshot mode opens an image locally in the viewer.
- WebRTC connectivity may fail across restrictive school networks without a relay.

This is an independent original implementation, not a port of Pane's Windows backend.
