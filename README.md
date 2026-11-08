# 🤟 Unmute AI

> **Bridging the Silence:** A Real-Time, Edge-AI Sign Language Translation Engine for Inclusive Communication.

---

## 📌 Overview

**Unmute AI** is a free, web-native accessibility tool engineered to translate Indian Sign Language (ISL) gestures into real-time text. By leveraging **Client-Side Edge Computing**, Unmute AI processes video feeds directly inside the user's browser via Google's MediaPipe engine, eliminating expensive hardware requirements, cloud subscription costs, and video stream latency while ensuring absolute user privacy.

The platform is designed to operate as a lightweight, zero-install single-page application (SPA) running entirely through standard web browser capabilities.

---

## ✨ Key Features & Highlights

* **⚡ Client-Side Edge AI:** Runs gesture inference locally on the client device with zero cloud API overhead and maximum data privacy.
* **🎯 21-Point Skeletal Tracking:** Maps 3D coordinate landmarks (`x`, `y`, `z`) for high-precision hand structure tracking regardless of complex backgrounds.
* **🔄 Hand Chirality Normalization:** Algorithmic adjustment for left-hand and right-hand symmetry to ensure consistent detection across both hands.
* **🌐 Zero-Install Architecture:** Operates instantly on any camera-enabled browser without requiring dedicated gloves, sensor arrays, or software downloads.
* **🚀 Lightweight Footprint:** Single-file architecture for minimal loading times and maximum compatibility on low-end hardware.

---

## 🛠️ Tech Stack & Dependencies

* **Frontend Structure:** HTML5, Vanilla JavaScript (ES6+), CSS3
* **AI & Computer Vision Engine:** 
  * `@mediapipe/hands` (v0.4+)
  * `@mediapipe/camera_utils` (v0.4+)
* **Hosting & Execution:** Serverless Browser Runtime (Local File / Static Web Server)

---

## 📂 Repository Structure

```text
Unmute/
├── index.html       # Single-file core engine (UI layout, WebCam pipeline, MediaPipe logic)
├── README.md        # Comprehensive project documentation
└── LICENSE          # Open-source license (MIT)
```

---

## 🚀 Getting Started & Local Setup

Since **Unmute AI** is built using a pure, web-native single-file architecture, there are zero `npm install` requirements or complex build steps.

### Prerequisites

* A modern web browser (Google Chrome, Microsoft Edge, Brave, or Firefox recommended).
* A working webcam (built-in, external USB, or smartphone camera connected via Iriun/DroidCam).

### Running the Application

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Ishaan-2589/Unmute.git
   cd Unmute
   ```

2. **Launch the platform:**
   * **Option A (Direct):** Double-click `index.html` to open it directly in your web browser.
   * **Option B (Recommended):** Serve via VS Code **Live Server** extension or Python static server:
     ```bash
     python -m http.server 8000
     ```
     Then open `http://localhost:8000` in your browser.

3. **Grant Camera Permissions:** When prompted by the browser, allow access to your camera feed.

---

## 🚦 Current Capabilities (v1.0 Ready)

* [x] **21-Landmark Coordinate Streaming:** Real-time canvas overlay rendering hand connections over raw video input.
* [x] **Static Heuristic Classification:** Instant detection for primary gestures (*Like 👍*, *Peace ✌️*, *Hello ✋*, *I Love You 🤟*).
* [x] **Mirrored Video Canvas:** Natural user feed orientation to simulate a real-time mirror display.
* [x] **Privacy Safeguards:** No raw image or video frames leave the browser memory environment.

---

## 🗺️ Future Implementations & Scalability Roadmap

* **Phase 1: Custom ML Classifier (Q3 2026)**
  * Transition from static geometric heuristics to a trained `scikit-learn` / `tfjs` neural network running on multi-point landmark datasets.
* **Phase 2: Dynamic Motion Tracking (Q4 2026)**
  * Temporal gesture sequence recognition using frame-buffer queues (LSTM/RNN logic) for dynamic ISL movement translation.
* **Phase 3: Contextual Sentence Builder (Q1 2027)**
  * Integration of lightweight Natural Language Processing (NLP) to convert raw translated sign keywords into structured, grammatically correct sentences.
* **Phase 4: Workspace Extensions (Q2 2027)**
  * Chrome Extension overlay targeting platforms like Google Meet and Zoom for real-time video call accessibility captions.

---

## 👤 Author & Academic Context

* **Ishaan** — *Lead Developer & AI Integration*
* Developed as part of Academic Minor & Major Project requirements at **JIMS Vasant Kunj**.
* Recognized and showcased at **CYNET 2026**.

---

## 📄 License

This project is licensed under the **MIT License** — feel free to modify and expand upon this codebase for open-source accessibility efforts.
