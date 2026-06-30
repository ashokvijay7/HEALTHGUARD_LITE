# 🛡️ HealthGuard360 Lite
> **Real-Time Health & Ergonomic Monitoring During Computer Use**

HealthGuard360 Lite is a client-side web application designed to counter the physical strains of prolonged computer use. Using advanced machine learning models directly in the browser, the application tracks body mechanics, facial tension, blink rates, and environmental variables to provide instantaneous biometric feedback, ergonomic stress tracking, and FDA drug-safety compliance checks.

---

## 🚀 Key Modules & Capabilities

### 1. 🧘 Wellness Scan & Ergonomic Tracker
Uses **MediaPipe Pose** and **FaceMesh** via the user's camera feed to analyze posture and cognitive load metrics locally without data escaping the browser:
*   **Biomechanical Alignment**: Monitors shoulder drop, forward head tilt, spinal rounding (slouch severity), and hip level.
*   **Facial Tension Index**: Tracks jaw clenching, brow furrowing, and micro-squints to compute a dynamic stress score (Relaxed, Focused, Tense, Stressed, Burnout Risk).
*   **Eye Fatigue Monitor**: Tracks eye aspect ratio (EAR) to detect low blink rates and triggers standard 20-20-20 rule prompts.
*   **Acoustic & Light Assessment**: Quantifies ambient workspace noise and lighting balances using web audio metrics and raw canvas exposure properties.
*   **Automated Coaching Popup**: Snapshots and warns users when sudden structural slouch milestones fall below threshold levels ($<40\%$).

### 2. 💊 MedSafe QuickCheck
An automated client-side drug database and evaluation panel query interface:
*   **FDA Database Interfacing**: Direct integration targets for fetching warnings, side effects, overdosing margins, food interactions, and current enforcement recalls.
*   **Side-by-Side Evaluation**: Contrast structural risk maps, chemical contraindications, and FDA pregnancy classifications side-by-side.
*   **QR Dissemination**: Automatically compiles medical evaluation cards into scannable on-screen QR blocks.

### 3. 👩‍⚕️ Virtual Doc Guidance
An educational triage portal providing friendly, multi-tier advice for common desk-worker complaints (Tension headaches, eye fatigue, localized strains):
*   Offers curated Lists of structured Do’s, Don’ts, Red Flags, and non-prescription counter-actions.

---

## 🛠️ Built With

*   **Core Languages**: HTML5, CSS3 (Custom Variables, CSS Grid, Flexbox), JavaScript (ES6+).
*   **Machine Learning Frame**: [MediaPipe Pose](https://cdn.jsdelivr.net/npm/@mediapipe/pose/) & [MediaPipe Face Mesh](https://cdn.jsdelivr.net/npm/@mediapipe/face_mesh/).
*   **Utilities**: `camera_utils.js`, `drawing_utils.js`, `qrcode.min.js`.
*   **AI Inference Engine**: Google Gemini API integration pipeline via dynamic REST context fetching.

---

## ⚙️ Configuration & Activation

To enable the operational **AI Coach** loop component, open the application index file and replace the hardcoded token parameter:

```javascript
// Locate line 351 in the <script> block:
const GEMINI_API_KEY = 'YOUR_ACTUAL_API_KEY_HERE';
