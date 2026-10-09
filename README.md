# TriagePass

Human-in-the-loop clinical triage handoff tool for government hospitals, PHCs, health camps, industrial-estate clinics and campus health centres across India.

> Educational prototype for triage support only. It does not diagnose or recommend treatment. Every output must be reviewed by a qualified professional. Uses synthetic data only.

## What it does
- Collects symptoms by voice (Hindi, English, Odia, Bengali, Tamil) or text, after a consent step
- Reads lab report photos with in-browser OCR and shows recorded values against usual ranges
- Builds a symptom timeline and detects missing information, then suggests follow-up questions for the health worker
- Assigns a transparent RED / AMBER / GREEN tag from a fixed rule library, with each signal linked to its source text
- Gives nurses and doctors a priority queue with review workflow, tag override and an audit log
- Produces a printable referral note with an anonymous QR code for handoff to the next facility
- Supports six scenarios: OPD queue, occupational screening, campus fever, maternal follow-up, chronic check-in, health camp

## Privacy and responsible-AI controls
- Consent before any case is created
- No names or phone numbers, anonymous case ID only
- Data stays in the browser (localStorage), with an auto-delete timer and delete-all
- Role-based access (health worker, nurse, doctor, admin) and a full audit log
- Deterministic, auditable rules: no black-box model decides urgency

## Tech
HTML, CSS and vanilla JavaScript (single page, no backend). Web Speech API, Tesseract.js, qrcode.js, and a service worker for offline use.

## Limitations
Sign-in is client-side (demo only). Rule thresholds are placeholders pending clinical validation. Regional-language translations need native-speaker review.

## Run it
Open `index.html` in Chrome, or visit the GitHub Pages link. Keep `sw.js` in the same folder.

## Team
Debadatta Sahoo (Captain), Shreemanjali Sahoo, Krishna Panda, Asutosh Dash, Somya Narayana Behera
