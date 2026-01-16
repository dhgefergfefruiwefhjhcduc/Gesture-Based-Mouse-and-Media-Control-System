# Gesture-Based Mouse and Media Control System 🖐️🖱️🎵

A **real-time computer vision application** that enables **touchless control of mouse actions and media playback** using **hand gestures** captured via a webcam. The system leverages **MediaPipe Hand Landmarker**, **OpenCV**, and **system-level automation** to provide an intuitive Human–Computer Interaction (HCI) experience.
- Watch Demo Video : https://drive.google.com/file/d/1FXgd0-Sx_DP1QJYnvSIjOl1XayCmx2RH/view?usp=drive_link
---

## 🚀 Features

* **Mouse Control Mode**

  * Move cursor using index finger
  * Single-click and double-click using pinch gestures
  * Smooth cursor movement using exponential smoothing

* **Volume Control Mode**

  * Adjust system volume using distance between thumb and index finger
  * Real-time visual volume feedback

* **Media Control Mode**

  * Play / Pause media
  * Next track
  * Previous track

* **Robust Gesture Detection**

  * Angle-based finger state detection
  * Depth (Z-axis) validation
  * Hand-size normalized thresholds

---

## 🧠 Technologies Used

* **Python 3**
* **OpenCV** – Video capture and visualization
* **MediaPipe Tasks API** – Hand landmark detection
* **NumPy** – Numerical computations
* **PyAutoGUI** – Mouse & keyboard automation
* **PyCAW** – System volume control (Windows)

---

## 🏗️ System Architecture

```
Webcam Feed
     ↓
MediaPipe Hand Landmarker
     ↓
Landmark Processing & Gesture Logic
     ↓
Action Mapping (Mouse / Media / Volume)
     ↓
System Control via PyAutoGUI & PyCAW
```

---

## ✋ Gesture Mapping

| Gesture                       | Action         |
| ----------------------------- | -------------- |
| Index + Thumb                 | Volume Control |
| Index + Thumb + Middle        | Mouse Mode     |
| Index + Middle + Ring         | Play / Pause   |
| Index + Middle + Ring + Pinky | Next Track     |
| All Fingers Open              | Previous Track |

> Gesture detection is stabilized using cooldown timers and geometric constraints to avoid false triggers.

---

## 📦 Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/gesture-based-mouse-media-control.git
cd gesture-based-mouse-media-control
```

### 2️⃣ Install Dependencies

```bash
pip install opencv-python mediapipe numpy pyautogui pycaw comtypes
```

### 3️⃣ Download MediaPipe Model

Download the **hand_landmarker.task** file from the official MediaPipe repository and place it in the project root directory.

---

## ▶️ Usage

Run the application using:

```bash
python main.py
```

* Ensure your webcam is connected
* Press **`q`** to quit the application

---

## ⚙️ Configuration Highlights

* **Gesture Cooldown**: Prevents repeated media triggers
* **Alpha Smoothing**: Improves cursor stability
* **Hand Size Normalization**: Ensures consistent performance across different users

---

## 🖥️ Platform Support

* ✅ Windows (Fully supported)
* ⚠️ Linux / macOS (Media keys & volume control may require changes)

---

## 📌 Project Highlights (Resume-Ready)

* Implemented a real-time **gesture-based HCI system** using computer vision
* Designed **multi-mode interaction logic** for mouse, media, and volume control
* Applied **geometric reasoning, angle detection, and depth analysis** for gesture recognition
* Integrated low-level **OS automation** for seamless user interaction

---

## 🔮 Future Improvements

* Add multi-hand support
* Gesture-based scrolling
* Custom gesture training module
* Cross-platform volume/media abstraction
* GUI for gesture configuration

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🙌 Acknowledgements

* MediaPipe Team – Hand Landmarker API
* OpenCV Community

---

⭐ If you find this project useful, consider giving it a star on GitHub!
