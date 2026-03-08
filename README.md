![DartZoom](https://i.imgur.com/TzEpN8I.png)

> **Automatic camera zoom for Autodarts — powered by OBS Move Transition filters.**  
> No manual input. No delays. **Frame-perfect zoom animations**, fully automated.

[![Latest Release](https://img.shields.io/github/v/release/manuel1234567532/dartzoom-releases?style=for-the-badge&cacheSeconds=60)](https://github.com/manuel1234567532/dartzoom-releases/releases)
[![Discord](https://img.shields.io/badge/Discord-Join-5865F2?style=for-the-badge&logo=discord&logoColor=white&labelColor=1a1a2e)](https://discord.gg/nMb3X9sWgv)
[![Chrome](https://img.shields.io/badge/Platform-Chrome-yellow?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=1a1a2e)](https://github.com/manuel1234567532/dartzoom-releases/releases)

---

# ✨ Features

| | |
|---|---|
| 🎯 | **Automatic segment zoom** — zooms to the exact field for every throw (`S1–S20`, `D1–D20`, `T1–T20`, `Bull`, `Bullseye`, `Miss`) |
| 🧠 | **Smart checkout prediction** — pre-zooms to the next required segment before the dart is thrown |
| 🔥 | **T20 streak detection** — stays locked on **T20** after two consecutive trebles |
| 🎬 | **OBS scene automations** — trigger actions on *Game On*, *Game End*, *My Turn* and *Opponent Turn* |
| 🔊 | **Sound effects support** — play OBS media sources on zoom-in / zoom-out |
| 🗺️ | **Custom checkout routes** — override Autodarts checkout guide |
| 💾 | **Filter backup & restore** — export/import all filter transforms as JSON |
| 👥 | **Multi-username support** — track multiple Autodarts players |

---

# 📋 Requirements

Before installing DartZoom, make sure you have:

- 🎥 [OBS Studio](https://obsproject.com/)
- 🔄 [OBS Move Transition Plugin](https://github.com/exeldro/obs-move-transition)
- 🌐 Google Chrome (or Chromium browser)
- 🎯 Active [Autodarts](https://autodarts.io/) setup

---

# 🚀 Installation

## 1️⃣ Install OBS Move Transition Plugin

Download the plugin and run the **Windows installer**.  
It installs automatically into OBS.

---

## 2️⃣ Install the Chrome Extension

1. Open Chrome  
2. Go to:

```
chrome://extensions
```

3. Enable **Developer Mode** (top right)  
4. Click **Load unpacked**  
5. Select the extracted **DartZoom** folder

---

# ⚙️ Setup Guide

## 1️⃣ Create a Board Scene

Create a scene called:

```
Board
```

Add your **board camera** as a source.

Crop the board using:

```
ALT + Drag
```

until the board perfectly fills the frame.

---

## 2️⃣ Add Board Scene to your Stream Scene

In your main streaming scene:

```
Add Source → Scene → Board
```

---

## 3️⃣ Enable OBS WebSocket

Open:

```
Tools → WebSocket Server Settings
```

Settings:

- Enable WebSocket Server
- Disable Authentication
- Click **Apply**

---

## 4️⃣ Configure DartZoom

Open the extension and configure:

| Field | Description |
|---|---|
| Username | Your Autodarts username(s) |
| Scene | Scene containing your board source (e.g. `Board`) |
| Source | Board camera source name (e.g. `Boardcam`) |
| Default Filter | Filter for the wide board view (e.g. `Default`) |

Then click:

```
Create All Cam Filters
```

This automatically creates **64 Move Source filters**.

---

## 5️⃣ Set Zoom Positions in OBS

Open:

```
Right Click Source → Filters
```

### Default View

1. Select `Default`
2. Scroll down
3. Click **Get Transform**

### Segment Zooms

Example `T20`:

1. Visually zoom to the segment
2. Click **Get Transform**

Repeat for all segments you want.

---

# 🧪 Testing

Use the **Test Filters** buttons in the extension.

You should see smooth **zoom animations** between segments.

---

# 🎛️ Settings Reference

| Setting | Description |
|---|---|
| Display Duration | Time the zoom remains visible after a throw |
| Checkout Score | Score threshold for checkout prediction (default `170`) |
| Filter Duration | Animation time of Move Source filters |
| Easing Function | Animation curve (Cubic, Sine, Bounce, etc.) |
| Zoom Sound | OBS media source played on zoom |
| Default Sound | Sound when returning to default view |

---

# 🗺️ Custom Checkout Routes

Override the Autodarts checkout guide.

Example:

```
40  →  S20, D10
32  →  S16, D8
170 →  T20, T20, Bull
```

Supported notation:

```
S1–S20
D1–D20
T1–T20
Bull
DBull
```

---

# 🎬 OBS Automations

DartZoom can trigger OBS actions automatically.

| Event | Trigger |
|---|---|
| Game On | First throw of a match |
| Game End | Match finished |
| My Turn | Your turn begins |
| Opponent Turn | Opponent's turn begins |

Each event can trigger:

- Show source
- Hide source
- Enable filter
- Disable filter

Optional delay supported.

---

# 💾 Backup & Restore

| | |
|---|---|
| 📥 Export Filters | Save filter transforms to `.json` |
| 📤 Import Filters | Restore filter transforms |
| ⚙️ Settings Backup | Export all extension settings |

Perfect for:

- reinstalling OBS
- migrating setups
- sharing configs

---

# 📦 Releases

Download the latest version here:

➡️ **https://github.com/manuel1234567532/dartzoom-releases/releases**

---

# 💬 Community

Need help or want to share your setup?

[![Discord](https://img.shields.io/badge/Join%20the%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/nMb3X9sWgv)

---

# 👨‍💻 Author

Created by **Lobiix**

Discord  
https://discord.com/users/424319034528366612
