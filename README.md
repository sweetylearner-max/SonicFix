<div align="center">

<img src="assets/logo.png" alt="SonicFix Logo" width="120"/>

# 🔊 SonicFix
### Next-Generation Multimodal Machinery Diagnostic Platform

*Hears the problem. Sees the machine. Diagnoses with precision.*

[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=for-the-badge&logo=flutter)](https://flutter.dev)
[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=for-the-badge&logo=python)](https://python.org)
[![Firebase](https://img.shields.io/badge/Firebase-Functions-FFCA28?style=for-the-badge&logo=firebase)](https://firebase.google.com)
[![Gemini](https://img.shields.io/badge/Gemini-Multimodal_AI-4285F4?style=for-the-badge&logo=google)](https://deepmind.google/technologies/gemini/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

</div>

---

## 🧠 What is SonicFix?

**SonicFix** is an intelligent diagnostic platform that fuses **acoustic analysis** and **visual AI** to identify mechanical failures in real time — no technician required.

Point your camera at a faulty AC compressor, car engine, or industrial motor. Let it listen. In seconds, SonicFix tells you **what's wrong**, **why it's failing** .

> Built at a hackathon. Shipped with ❤️.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🎙️ **Acoustic Classification** | YAMNet filters noise before Gemini processes audio |
| 👁️ **Visual Machine ID** | Identifies make/model from camera feed |
| 🔗 **Sensory Fusion** | Audio waveform + vision correlated simultaneously |
| 💬 **Chat Interface** | Dynamic bubbles with waveform players & diagnostic cards |
| 💰 **Localized Cost Estimates** | Real labor & parts pricing for your local market |
| 🔧 **Repair Guides** | Step-by-step actionable technician instructions |

| 🌗 **Light / Dark Mode** | Fully adaptive theme intelligence |
| ⚡ **Self-Healing Backend** | 3-tier model fallback for 99.9% uptime |

---

## 🏗️ Architecture — "Sensory Fusion Pipeline"

```
📷 Camera Feed ──────────────────────────────────┐
                                                  ▼
🎙️ Raw Audio ──► YAMNet (16kHz Mono) ──► Blacklist Filter ──► Gemini Multimodal
                  ↑                                               ↓
             5s Audio Cap                              Vision + Audio Correlation
             Noise Detection                                      ↓
                                                     Failure Mode Identification
                                                                  ↓
                                                     Diagnostic Card + PKR Costs
```

### Visual-First, Audio-Second

SonicFix uses a strict **Visual-First, Audio-Second** approach:

1. **🔍 Visual Identification** — Gemini sees the machine and establishes context (e.g., "Haier AC Compressor, Model X")
2. **🎵 Acoustic Analysis** — YAMNet resamples audio to 16kHz mono and classifies the sound signature
3. **🚫 Blacklist Filtering** — Speech, music, and silence are flagged and context is passed to Gemini to ignore background noise
4. **🔗 Fusion** — Raw waveform is injected directly into Gemini's native audio buffer (no lossy speech-to-text)
5. **📋 Diagnosis** — Failure modes are matched (e.g., "rhythmic clicking → faulty starter relay")

---

## 🔁 Self-Healing Fallback Strategy

| Priority | Model | Use Case |
|---|---|---|
| 🏆 Primary | `gemini-2.5-pro-preview` | Highest accuracy |
| 🥈 Secondary | `gemini-2.0-flash` | Faster response |
| 🥉 Tertiary | `gemini-2.0-flash-lite` | Extreme low-latency fallback |

If the primary model fails or times out, the backend automatically escalates down the chain — zero user disruption.

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK `>=3.0.0`
- Python `3.11`
- Firebase CLI
- Google Cloud project with Gemini API enabled

### Backend (Python + Firebase Functions)

```bash
cd backend
pip install -r requirements.txt
firebase login
firebase deploy --only functions
```

### Frontend (Flutter)

```bash
flutter pub get
flutter run
```

> For release build:
> ```bash
> flutter build apk --release
> ```

---

## 🗂️ Project Structure

```
SonicFix/
├── lib/                    # Flutter source
│   ├── screens/            # UI screens
│   ├── widgets/            # Waveform player, diagnostic cards
│   └── services/           # API + audio recording services
├── backend/                # Python Firebase Functions
│   ├── main.py             # Gemini + YAMNet pipeline
│   └── requirements.txt
├── assets/                 # Icons, animations
└── pubspec.yaml
```

---

## 🛠️ Tech Stack

**Frontend**
- Flutter / Dart
- `animate_do` for micro-animations
- Custom Waveform Audio Player widget

**Backend**
- Python 3.11
- TensorFlow Hub — YAMNet acoustic model
- Google Gemini Multimodal API
- Firebase Cloud Functions

---

## 🌍 Localized Market Intelligence

SonicFix repair estimates are calibrated for **local markets (2026)**:
- Labor rates sourced from regional mechanic market averages
- Parts pricing in local currency
- Repair complexity adjusted for locally available tools and technicians

---

## 🤝 Contributing

Contributions are welcome! Please open an issue first to discuss what you'd like to change.

```bash
git checkout -b feature/your-feature
git commit -m "Add: your feature"
git push origin feature/your-feature
```

---

## 📄 License

This project is licensed under the **MIT License** — see [LICENSE](LICENSE) for details.

---

<div align="center">

Made with ❤️ by **[@sweetylearner-max](https://github.com/sweetylearner-max)**

*If SonicFix helped you, drop a ⭐ on the repo!*

</div>
