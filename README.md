# ✋ Gesture App Launcher

A real-time **hand gesture based application launcher** built with **Python, OpenCV, and MediaPipe**.

This project uses the webcam to detect a single hand, identify finger positions, and perform actions like opening **Chrome**, **Calculator**, **Notepad**, **YouTube**, or closing the active window.

## 🚀 Features

- Real-time webcam-based hand gesture detection
- Detects **one hand** using MediaPipe
- Launches applications using specific gestures
- Opens websites from gestures
- Can close the currently active app using a fist gesture
- Includes cooldown control to prevent repeated actions
- Press `Q` to stop the program

## 🧠 Technologies Used

- Python
- OpenCV
- MediaPipe
- PyAutoGUI

## ⚙️ How It Works

The system captures webcam frames using OpenCV, flips the frame for a mirror view, and sends it to MediaPipe for hand landmark detection.

It checks the position of the thumb and fingers to determine which fingers are open or closed. Based on the detected finger pattern, it triggers a specific system action.

## 🖐️ Gesture Controls

| Gesture | Finger Pattern | Action |
|--------|----------------|--------|
| Palm | `[1,1,1,1,1]` | Open Chrome |
| Victory | `[0,1,1,0,0]` | Open Calculator |
| Thumbs Up | `[1,0,0,0,0]` | Open Notepad |
| Index Finger Only | `[0,1,0,0,0]` | Open YouTube |
| Fist | `[0,0,0,0,0]` | Close active app |
| Other gestures | - | Show `Unknown` |

## 📷 Requirements

- Python 3.x
- Working webcam
- Windows OS recommended  
  (because commands like `calc`, `notepad`, and `start chrome` are Windows-based)

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/ashwathymnair3-beep/hand-gesture-launcher.git
