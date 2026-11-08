# 🤟 Unmute AI

> **Bridging the Silence:** A Real-Time, Edge-AI Sign Language Translation Engine for Inclusive Communication.

![Unmute AI Banner](https://img.shields.io/badge/Status-Active%20R%26D-0ea5e9?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-10b981?style=for-the-badge)
![Tech Stack](https://img.shields.io/badge/Stack-Python%20%7C%20React%20%7C%20MediaPipe-38bdf8?style=for-the-badge)

---

## 📌 Overview

**Unmute AI** is a zero-cost, web-native accessibility tool engineered to translate Indian Sign Language (ISL) gestures into real-time text. By leveraging **Client-Side Edge Computing**, Unmute AI processes video feeds directly inside the user's browser, eliminating hardware expenses, server costs, and cloud latency while providing data privacy.

The project employs a **Hybrid R&D-to-Production Pipeline**:
- **Python Research Laboratory:** Used for gesture data collection, heuristic math modeling, and 3D coordinate analysis.
- **React/Vite Web Platform:** High-performance, zero-install production environment running MediaPipe JS for instant accessibility on standard webcams.

---

## ✨ Key Features & Technical Highlights

- **⚡ Client-Side Edge AI:** Runs inference locally on the device with zero cloud API overhead and absolute user privacy.
- **🎯 21-Point Skeletal Tracking:** Maps 3D coordinate landmarks for high precision regardless of background noise.
- **🔄 Chirality-Aware Logic:** Custom heuristic algorithms handle hand symmetry (Right vs. Left hand detection) to reduce false positives.
- **🌐 No-Install Architecture:** Operates on standard browser hardware without requiring dedicated gloves or external depth sensors.
- **Modular Monorepo Structure:** Clear separation between Python data collection scripts and the React web application interface.

---

## 🛠️ Architecture & Monorepo Structure

```text
UNMUTE-AI/
├── lab/                     # R&D Laboratory (Python Environment)
│   ├── data/                # Collected landmark JSON datasets
│   ├── scripts/             # Auxiliary data processing scripts
│   ├── lab.py               # Real-time gesture analysis & collector
│   └── requirements.txt     # Python dependencies (OpenCV, MediaPipe)
│
├── unmute-app/              # Production Web App (React + Vite)
│   ├── src/
│   │   ├── hooks/           # Custom React hooks (useMediaPipe.js)
│   │   ├── App.jsx          # Main dashboard view
│   │   └── App.css          # Styling & components
│   ├── index.html
│   └── package.json
└── README.md
```

---

## 🚀 Current Implementation Status (v1.0 Alpha)

The current version establishes the foundational infrastructure for low-latency gesture detection:

- [x] **21-Landmark Hand Mapping:** Real-time tracking integrated into both Python R&D and React production interfaces.
- [x] **Data Harvesting Pipeline:** Custom gesture saving tool (`lab.py`) that exports coordinate vectors into structured JSON datasets.
- [x] **Chirality Normalization:** Algorithmic adjustment for left- and right-handed gesture inputs.
- [x] **Core Gesture Set:** Active classification support for foundational static signs (e.g., *Hello*, *Like*, *Peace*, *I Love You*).

---

## 🗺️ Roadmap & Future Implementations

The project roadmap scales Unmute AI from a static gesture translator to a comprehensive communication suite:

### Phase 1: Dynamic Gesture Recognition (Q3 2026)
- Integration of sequence tracking (LSTM / Time-Series models) to process fluid, moving ISL signs over time rather than static frames.

### Phase 2: Natural Language Processing (NLP) Layer (Q4 2026)
- Contextual sentence builder to transform raw gesture strings into grammatically correct natural language sentences.

### Phase 3: Seamless Workspace Extensions (Q1 2027)
- **Chrome Extension Overlay:** Direct integration for real-time translation overlays on Google Meet, Zoom, and Microsoft Teams calls.
- **PWA Deployment:** Offline-first Progressive Web App capabilities for low-bandwidth environments in remote regions.

---

## 💻 Getting Started

### 1. Python Laboratory Setup (R&D)

```bash
# Navigate to lab directory
cd lab

# Install dependencies
pip install -r requirements.txt

# Launch the gesture recording environment
python lab.py
```
*Press `S` to save current landmark coordinates to dataset; press `Q` to quit.*

### 2. React Production Setup (Web Dashboard)

```bash
# Navigate to web app directory
cd unmute-app

# Install packages
npm install

# Start local server
npm run dev
```

---

## 👥 Authors & Acknowledgments

- **Ishaan** — *Lead Developer & AI Integration*
- Developed as part of Academic Research at **JIMS Vasant Kunj**.
- Recognition: Showcased at **CYNET 2026**.

---

