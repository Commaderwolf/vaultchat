# VaultChat — P2P Encrypted Messenger

Zero-cost, zero-server encrypted chat. Works on any phone or PC.

## Deploy to GitHub Pages (free, ~2 minutes)

1. Go to **github.com/new** — create a repo called `vaultchat`, set to **Public**
2. Upload `index.html`, `manifest.json`, and `README.md`
3. Go to **Settings → Pages → Source → Deploy from branch → main → / (root)**
4. Your app is live at `https://YOUR-USERNAME.github.io/vaultchat`

That's it. Share that URL with anyone.

## How to connect (for users)

**Person A (host):**
1. Open the URL, enter name + secret key → Enter Vault
2. On the "My Code" tab — copy the offer code
3. Send that code to Person B (text, Discord, email, anything)

**Person B (joiner):**
1. Open the same URL, enter name + **same secret key** → Enter Vault
2. Switch to the "Join" tab — paste Person A's offer code → Generate My Answer
3. Copy the answer code, send it back to Person A

**Person A:**
4. Paste Person B's answer code → Connect
5. Connected! Direct P2P, no server involved.

## How it works

- **WebRTC DataChannels** — direct browser-to-browser connection after the one-time code exchange
- **AES-256-GCM encryption** — every message encrypted before it leaves your device
- **PBKDF2 key derivation** — 100,000 rounds, SHA-256
- **Free STUN/TURN** — uses Google's public STUN servers + Open Relay Project's free TURN servers for NAT traversal
- After connecting, **no relay server is involved at all** — messages go directly between browsers

## Features
- Text chat with timestamps
- Image sharing (auto-compressed)
- File sharing (up to 4MB)
- Self-destructing messages (10s)
- Typing indicators
- Key fingerprint verification
- PWA installable (Add to Home Screen)
