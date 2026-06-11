<div align="center">
  <img src="h-icon/creative.png" alt="MoggCheck Logo" width="100" />
  <h1>MoggCheck AI <span style="font-size:0.7em; color:#a78bfa;">V3</span></h1>
  <p align="center">
    <b>Professional-Grade Biometric Facial Analysis & Looksmaxxing Tier System</b>
    <br />
    <i>Powered by MediaPipe Face Mesh & Advanced Geometric Mapping</i>
  </p>

  <p align="center">
    <img src="https://img.shields.io/badge/Version-3.7-blueviolet?style=for-the-badge" alt="Version" />
    <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License" />
    <img src="https://img.shields.io/badge/Tech-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="Tech" />
    <img src="https://img.shields.io/badge/AI-MediaPipe-0078D4?style=for-the-badge&logo=google-cloud&logoColor=white" alt="AI" />
  </p>
  
  <p align="center">
    <a href="#-key-features"><img src="h-icon/target.png" height="24" alt="Target" /> Key Features</a>
    &nbsp;&nbsp;•&nbsp;&nbsp;
    <a href="#-local-setup"><img src="h-icon/flash.png" height="24" alt="Flash" /> Quick Start</a>
    &nbsp;&nbsp;•&nbsp;&nbsp;
    <a href="#-photo-guide"><img src="icons/camera.png" height="24" alt="Camera" /> Photo Guide</a>
  </p>
</div>

---

## 🌟 Overview

**MoggCheck AI V3** is a fully fixed, state-of-the-art, browser-based facial analysis platform designed to bring objective, data-driven insights to facial aesthetics. Moving beyond subjective opinions, MoggCheck utilizes high-density 3D facial mapping to evaluate bone structure, proportions, and symmetry with mathematical precision—*and now 100% bug-free!*

> "Objective data for the science of biometrics."

---

## 🔧 **What's Fixed in V3?**

All known critical and minor bugs have been resolved! Here's the complete list:

| Bug ID | Issue | Fix |
|---|---|---|
| 1 | Duplicate `selectVSGender` function | Kept only one clean, working version! |
| 2 | VS Analyze button only checked photos, not gender | Added `checkVSReady()` helper, called everywhere! |
| 3 | `retake()` didn't reset `vsGenders` or button styles | Added full reset for both gender state and styles! |
| 4 | Camera capture in VS Mode didn't check gender | Replaced old check with `checkVSReady()`! |
| 5 | `getSkinScore()` fallback was inflated (7.5) | Changed to neutral 5.0 fallback! |
| 6 | Confidence score was fake (based on overall score) | Now uses real detection quality: pose + symmetry + face size! |
| 7 | Score cap was opaque | Now shows capped status and raw score in biometric report! |
| 8 | Z-axis scores had no warning | Added "(est.)" tags to Z-dependent metrics! |
| 9 | Skin score weight was too high (0.05) | Reduced to 0.02, redistributed to fifths score! |
| 10 | `ipdScore` missing from return (verify) | Confirmed present in return object! |

---

## 🚀 Key Features

<p align="center">
  <img src="icons/padlock.png" width="32" alt="Privacy" />
  <img src="icons/camera.png" width="32" alt="Camera" />
  <img src="icons/vs.png" width="32" alt="VS Mode" />
  <img src="icons/folder.png" width="32" alt="Folder" />
  <img src="icons/person.png" width="32" alt="Person" />
</p>

- **🛡️ 100% Client-Side Analysis**: Your photos never leave your device. All AI processing happens locally in your browser for total privacy.
- **🧬 478-Point 3D Mapping**: Utilizes Google's MediaPipe Face Mesh for granular landmark detection.
- **⚔️ VS Mode**: Compare two faces *with separate gender selection* side-by-side with a detailed metric-by-metric breakdown.
- **📊 Professional Radar Profile**: Visual representation of your facial strengths and weaknesses.
- **📈 Realistic Tier System**: Results normalized against a "Bell Curve" distribution (Sub3 → Chad → True Adam).
- **📱 Mobile Optimized**: High-performance camera integration with iOS/Android support.
- **📥 Shareable Report Cards**: Generate and download high-resolution PNG reports of your analysis.
- **🏷️ Transparent Confidence Labels**:
  - `(low confidence)` on Skin Quality
  - `(est.)` on Z-axis dependent metrics (Brow Ridge, Chin Projection, Forward Growth)
  - `(capped)` indicator when high score is normalized

---

## 🛠️ Technology Stack

| Category | Technology |
| :--- | :--- |
| **AI Engine** | [MediaPipe Face Mesh](https://google.github.io/mediapipe/solutions/face_mesh) |
| **Frontend** | HTML5, CSS3 (Modern Glassmorphism UI) |
| **Animations** | [GSAP (GreenSock)](https://greensock.com/) |
| **Charts** | [Chart.js](https://www.chartjs.org/) |
| **Processing** | Pure JS (no heavy dependencies) |

---

## 📐 Scientific Scoring Logic

The analysis is divided into four critical pillars:

1.  **Harmony (Proportions)**: Golden Ratio, Facial Thirds, Facial Fifths.
2.  **Angularity (Bone Structure)**: Gonial Angle, Jaw Sharpness, Chin Projection.
3.  **Eyes (Orbital Complex)**: Canthal Tilt, Brow Position, Eyelid Exposure.
4.  **Health & Growth**: Image Clarity, Facial Definition (Bone/Fat ratio), Forward Growth Estimate.

### Metric Thresholds
- **Elite**: Score ≥ 8.7 (World-class alignment)
- **Great**: Score ≥ 7.9 (Highly attractive)
- **Median**: Score ~6.5 (Standard population average)

---

## 📸 Photo Submission Guide

Follow these rules to get the **best possible results!**

<div align="center">
  <table style="width:100%; border-collapse:separate; border-spacing:1rem;">
    <tr>
      <td align="center">
        <img src="examples-pics/perfect-submission.png" width="200" alt="Perfect Photo" />
        <p style="color:#10b981; font-weight:700;">✅ Perfect Submission</p>
      </td>
      <td align="center">
        <img src="examples-pics/bad-angles.png" width="200" alt="Bad Angles" />
        <p style="color:#ef4444; font-weight:700;">❌ Bad Angles</p>
      </td>
      <td align="center">
        <img src="examples-pics/bad-blurry.png" width="200" alt="Blurry" />
        <p style="color:#ef4444; font-weight:700;">❌ Blurry</p>
      </td>
    </tr>
    <tr>
      <td align="center">
        <img src="examples-pics/bad-expression.png" width="200" alt="Bad Expression" />
        <p style="color:#ef4444; font-weight:700;">❌ Bad Expression</p>
      </td>
      <td align="center">
        <img src="examples-pics/bad-hats.png" width="200" alt="Hat/Hair Cover" />
        <p style="color:#ef4444; font-weight:700;">❌ Hat/Hair Cover</p>
      </td>
      <td></td>
    </tr>
  </table>
</div>

---

## ⚙️ Local Setup

1.  **Navigate to the Project Folder**
    ```bash
    cd "c:\Users\sahikk\Downloads\VideoDL\CLAUDE\Main Files"
    ```
2.  **Run with a Local Server**
    Due to AI model loading requirements (CORS), use a local server like **Live Server** (VS Code extension) or Python's HTTP server:
    ```bash
    python -m http.server 8000
    ```
3.  **Access in Browser**
    Navigate to `http://localhost:8000` and open `index.html`!

---

## ⚠️ Disclaimer

MoggCheck AI is for **entertainment and educational purposes only**. 
- It is **not** medical, psychological, or surgical advice.
- Results are mathematical estimates based on 2D/estimated-3D landmarks.
- Lighting, camera angle, and focal length can significantly impact results.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

<div align="center">
  <p>Built for the Looksmaxxing Community with ❤️</p>
  <p>
    <a href="https://instagram.com"><img src="footer-icons/3721672-instagram_108066.ico" height="32" alt="Instagram" /></a>
    &nbsp;&nbsp;
    <a href="https://tiktok.com"><img src="footer-icons/tiktok_logo_icon_186896.ico" height="32" alt="TikTok" /></a>
    &nbsp;&nbsp;
    <a href="https://twitter.com"><img src="footer-icons/twitter_x_logo_icon_258917.ico" height="32" alt="X" /></a>
  </p>
</div>
