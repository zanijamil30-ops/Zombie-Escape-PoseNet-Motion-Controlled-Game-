# 🧟‍♂️ Zombie Escape — PoseNet Motion-Controlled Game (Local PyCharm Edition)

**Zombie Escape** is a motion-controlled browser game powered by **ml5.js (PoseNet)** and **p5.js**.  
Play with your **body movements**, not your keyboard!  
Raise your hands or lean left/right to dodge zombies and survive as long as you can.  

> 🧠 This version is configured for **local development using PyCharm** (JetBrains IDE),  
> running on the built-in **localhost server** — no external hosting required.

---

## 🎮 Game Overview

| Action | Movement |
|--------|-----------|
| ✋ Right hand up | Jump |
| ✋ Left hand up | Crouch |
| ↔️ Lean left / right | Change lanes |

Your webcam detects your pose in real-time, but the **camera feed is hidden** — only your in-game avatar is visible.  
Everything runs **locally in your browser** for privacy and performance.

---

## 🧠 Tech Stack

- **ml5.js (PoseNet)** — real-time human pose estimation  
- **p5.js** — creative coding and animation framework  
- **JavaScript (ES6)** — game logic  
- **PyCharm’s Localhost Server** — for easy testing (`http://localhost:63342/...`)  

All computations are done **client-side**; nothing is uploaded or stored.

---

## 🕹️ How It Works

1. PoseNet detects your wrist and shoulder positions.
2. Gestures are recognized:
   - Raise right hand → trigger a jump.
   - Raise left hand → trigger a crouch.
   - Lean left or right → change player lane.
3. Your avatar reacts accordingly — no real camera feed is displayed.

---

---

## ⚙️ How to Run Locally (PyCharm Localhost Setup)

1. Open **PyCharm** and load this project folder.  
2. Make sure `index.html` is inside your project directory.  
3. Right-click `index.html` → select **“Open in Browser → Chrome / Edge”**.  
4. PyCharm will automatically launch a local development server, typically at:
http://localhost:63342/PythonProject7/index.html

5. Allow camera access when prompted.  
6. Stand visible for ~1 second while auto-calibration runs.  
7. Start moving — your avatar will respond to your gestures!

> ⚠️ Tip: Ensure your hands and shoulders are visible in the webcam and you have good lighting.

---

## 🧩 Key Features

✅ Real-time motion detection (PoseNet)  
✅ Hidden camera feed — only avatar visible  
✅ Automatic calibration (no setup)  
✅ Smooth gesture recognition (EWMA filtering)  
✅ Lightweight browser performance  
✅ Works via **PyCharm’s localhost** without extra server setup  

---

## 🧩 Technical Details

- PoseNet identifies 17 body keypoints.
- Smoothing via Exponential Weighted Moving Average (EWMA).
- Discrete "edge-triggered" logic prevents jitter.
- Hidden `<video>` capture provides data to PoseNet but never appears in the UI.
- Game loop runs at 60 FPS using `p5.js draw()`.

---

## 🧠 Privacy

Your webcam input is processed **only on your device**.  
No frames are recorded or sent anywhere.  
You can safely play offline — all ML runs locally in your browser.

---

## 🧠 Example Localhost URL

If opened through PyCharm (like in your screenshot),  
your address bar will show something similar to:

http://localhost:63342/PythonProject7/index.html?_ijt=abcdef123456&_ij_reload=RELOAD_ON_SAVE


You can refresh or reload at any time — the query string simply allows PyCharm’s auto-reload feature.

---

## 🧑‍💻 Developer Info

**Author:** *Zainab Jamil*  
**IDE:** PyCharm (JetBrains)  
**Language:** JavaScript / HTML5  
**Libraries:** p5.js, ml5.js  
**Local URL:** `http://localhost:63342/PythonProject7/index.html`

---

## 📸 Screenshots


---

## 🪪 License

This project is licensed under the **MIT License** — free for use, modification, and educational demos.

---

## 💡 Future Enhancements

- Add background music and sound FX  
- Implement score multiplier streaks  
- Add calibration indicator and visual feedback  
- Switch to **MediaPipe Pose** for faster & more accurate detection  
- Optional public leaderboard integration  

---

**🧟 Raise your hands — or the zombies get you!**
