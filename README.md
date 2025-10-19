# 🔔 AI Smart Doorbell for Raspberry Pi 4

> Replace your Ring doorbell with a privacy-focused, locally-hosted AI system featuring face recognition, natural voice interaction, and a beautiful web dashboard.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)


## ✨ Features

### 🎯 Core Capabilities

| Feature | Description |
|---------|-------------|
| 👤 **Face Recognition** | Automatically identify family members, friends, and regular visitors |
| 🗣️ **Natural Voice** | Greet visitors with natural-sounding  |
| 🎤 **Speech Recognition** | Listen and respond to visitor requests  |
| 📱 **Mobile Notifications** | Instant alerts |
| 🌐 **Web Dashboard** | Modern UI for managing faces, settings, and visit history |
| 💾 **SQLite Database** | Track all visitors and maintain face recognition database |
| 📹 **AI Person Detection** | 
NVR with zone-based detection |
| 🔒 **Privacy-First** | All data stays on your local network |

### 🎨 Example Interactions

**Unknown Visitor:**
```
🔔 Doorbell detects person at 2-3 feet
🗣️ "Hello! How can I help you today?"
🎤 "Is anyone home?"
🗣️ "Let me check if anyone is available. One moment please."
📱 Notification sent to homeowners
```

**Recognized Person:**
```
🔔 Doorbell detects John approaching
👤 Face recognition identifies: John Smith
🗣️ "Hello John Smith! How can I help you today?"
📱 "John Smith is at the door"
```

## 📋 Hardware Requirements

### Required
- **Raspberry Pi 4** (4GB RAM minimum, 8GB recommended)
- **Pi Camera Module** (v2 or v3)
- **USB Microphone** (any USB mic)
- **Speaker** (3.5mm jack or USB)
- **microSD Card** (32GB+ Class 10)
- **Power Supply** (Official Pi 4 adapter, 15W)

### Optional
- **Google Coral USB Accelerator** ($60) - Makes detection 10x faster
- **Weatherproof enclosure** - For outdoor installation
- **PoE HAT** - For cleaner power delivery

### Tested Configurations

| Config | Person Detection | Face Recognition | Total Response |
|--------|------------------|------------------|----------------|
| Pi 4 (4GB) + CPU | ~5 FPS | ~2s | ~8s |
| Pi 4 (8GB) + CPU | ~5 FPS | ~2s | ~8s |
| Pi 4 + Coral USB | ~15 FPS | ~2s | ~4s |


### Prerequisites

```bash
# Update your Pi
sudo apt update && sudo apt upgrade -y

# Ensure 64-bit OS (recommended)
uname -m  # Should output: aarch64
```

## 🌐 Web Dashboard Guide

Access at `http://YOUR_PI_IP:5001`

### Dashboard Tabs

#### 📊 Dashboard (Home)
- Real-time statistics
- Total known persons
- Total visits
- Unknown faces count

#### 👥 Known Persons
- Grid view of all recognized people
- Add new persons with photos
- Edit/delete existing persons
- Mark as "Family" or "Trusted"
- See last seen timestamp

#### ❓ Unknown Faces
- Gallery of unrecognized visitors
- Click to identify and add name
- Automatically becomes known person
- Sorted by most recent

#### 📋 Recent Visits
- Complete visitor history
- Shows recognized vs unknown
- Displays spoken text
- Includes timestamps and snapshots

#### ⚙️ Settings
Live configuration (no restart needed):

| Setting | Default | Range | Description |
|---------|---------|-------|-------------|
| Cooldown Seconds | 45 | 10-300 | Time between greetings |
| Face Tolerance | 0.6 | 0.4-0.7 | Recognition strictness |
| Min Person Confidence | 0.75 | 0.5-0.95 | Detection threshold |
| Greeting Message | "Hello! How can I help you today?" | - | Default greeting |
| Recognized Greeting | "Hello {name}! ..." | - | Use {name} placeholder |
| Listen Timeout | 8 | 3-15 | Seconds to listen |
| Enable Face Recognition | true | true/false | Toggle recognition |



## 📝 License

This project is licensed under the MIT License - see [LICENSE](LICENSE) for details.


### Inspiration
- Ring Video Doorbell (for showing what's possible)
- Open source community for privacy-focused alternatives


## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/YOUR_USERNAME/smart-doorbell)
![GitHub forks](https://img.shields.io/github/forks/YOUR_USERNAME/smart-doorbell)
![GitHub issues](https://img.shields.io/github/issues/YOUR_USERNAME/smart-doorbell)
![GitHub pull requests](https://img.shields.io/github/issues-pr/YOUR_USERNAME/smart-doorbell)
![GitHub last commit](https://img.shields.io/github/last-commit/YOUR_USERNAME/smart-doorbell)

---

<div align="center">

**Made with ❤️ for privacy-focused home automation**

**If this project helped you, please ⭐ star the repository!**

[Report Bug](https://github.com/YOUR_USERNAME/smart-doorbell/issues) · 
[Request Feature](https://github.com/YOUR_USERNAME/smart-doorbell/issues) · 
[Documentation](https://github.com/YOUR_USERNAME/smart-doorbell/wiki)

</div>
