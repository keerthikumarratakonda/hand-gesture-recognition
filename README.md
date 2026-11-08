# Hand Gesture Recognition & Distress Signal AI 🖐️⚡

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-brightgreen?style=for-the-badge&logo=github)](https://keerthikumarratakonda.github.io/hand-gesture-recognition/)
[![MediaPipe](https://img.shields.io/badge/MediaPipe-Tasks%20Vision-blue?style=for-the-badge&logo=google)](https://developers.google.com/mediapipe)
[![Python](https://img.shields.io/badge/Python-3.10%2B-yellow?style=for-the-badge&logo=python)](https://www.python.org/)
[![FPS](https://img.shields.io/badge/Speed-60%20to%2090%20FPS-orange?style=for-the-badge)]()

A real-time, low-latency 21-joint hand skeleton tracker and gesture recognition engine powered by MediaPipe Vision.

🌐 **Try the Live Web App in your browser:**  
👉 **[https://keerthikumarratakonda.github.io/hand-gesture-recognition/](https://keerthikumarratakonda.github.io/hand-gesture-recognition/)**

---

## 🌟 Key Features

1. **Signal for Help (Domestic Violence & Emergency Distress Signal)**:
   - **Step 1**: Palm facing outwards, thumb placed on the palm (4 fingers extended).
   - **Step 2**: 4 fingers close down over the thumb (fist closed over trapped thumb) -> **Triggers glowing Emergency Distress Alert Banner!**
2. **Real-Time Finger Counting (0 to 10 Fingers)**:
   - Per-hand finger counter (0 to 5 fingers per hand).
   - Two-hand total finger counter (**10 Fingers / 10 Count** when showing both open hands).
   - Dedicated on-screen floating finger counter widget.
3. **21 3D Joint Tracking**: Tracks full hand articulation with glowing neon skeleton visualization.
4. **Handedness Classification**: Automatically detects and labels Left Hand vs. Right Hand.
5. **Multi-Gesture Recognition (14+ Gestures)**:
   - 🚨 **Help** (Emergency Distress Signal)
   - ⚠️ Help Signal (Thumb Tucked - Step 1)
   - 👍 Like / Thumbs Up
   - 👎 Dislike / Thumbs Down
   - 🤙 Call Me
   - 🤘 Rock On / Horns
   - 👌 OK Sign
   - 👆 Point / One (1)
   - ✌️ Peace Up / Two Up (2)
   - 🖖 Three (3)
   - 🖐️ Four (4)
   - ✋ Open Palm / Five (5)
   - ✊ Closed Fist (0)
   - 🤏 Pinch
6. **Anti-Jitter Exponential Smoothing**: Smooth tracking with zero latency at 60–90 FPS.

---

## 🚀 Two Ways to Run

### 1. 🌐 Live Online Demo (No Installation Needed)
Open the web app directly on any phone, tablet, or PC browser:  
🔗 **[https://keerthikumarratakonda.github.io/hand-gesture-recognition/](https://keerthikumarratakonda.github.io/hand-gesture-recognition/)**

### 2. 💻 Run Locally on Desktop (Python + OpenCV)

#### Prerequisites
- Python 3.10 or higher
- Webcam

#### Setup & Launch
```bash
# Clone the repository
git clone https://github.com/keerthikumarratakonda/hand-gesture-recognition.git
cd hand-gesture-recognition/hand_gesture

# Install dependencies
pip install -r requirements.txt

# Launch application
python main.py
```

*On Windows, you can simply double-click `run.bat` inside the `hand_gesture` directory!*

---

## 📁 Repository Structure

```
hand-gesture-recognition/
├── index.html                   # 🌐 Live Web App (GitHub Pages)
├── README.md                    # 📖 Project Documentation
├── .gitignore                   # 🚫 Git ignore rules
└── hand_gesture/                # 💻 Desktop Python Application
    ├── assets/                  # Previews and reference snapshots
    ├── models/                  # MediaPipe gesture recognizer task model
    ├── src/                     # Core computer vision modules
    │   ├── camera.py            # Threaded high-FPS webcam pipeline
    │   ├── gesture_classifier.py# Geometric gesture & distress signal classifier
    │   ├── hand_tracker.py      # MediaPipe 21-joint skeleton tracker
    │   ├── visualizer.py        # Neon HUD & skeleton renderer
    │   └── worker.py            # Asynchronous background worker
    ├── main.py                  # Desktop application entry point
    ├── requirements.txt         # Python dependencies
    ├── run.bat                  # 1-click Windows launcher
    └── run.ps1                  # PowerShell launcher
```

---

## ⌨️ Desktop Controls
- `[S]` : Save snapshot of current frame with hand skeletons and gesture tags.
- `[Q]` or `[ESC]` : Quit the application.

---

## 📄 License
This project is open-source and available under the [MIT License](LICENSE).

