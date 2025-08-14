H35N Light Meter (Web App)

A minimal, browser-based light meter for the Kodak H35N half-frame film camera, designed for iPhone (but works on any modern device with a camera).
It uses your phone’s camera feed to estimate exposure, lets you select your film stock ISO, and toggle Flash ON/OFF to match the H35N’s fixed settings.
Built as a single HTML file — no install needed, just open in Safari/Chrome over HTTPS.

⸻

✨ Features
	•	Live camera preview with center target box for metering.
	•	Film stock ISO selector (ISO 50 → 3200).
	•	Flash ON/OFF toggle:
	•	ON → approx. f/8 @ 1/100s
	•	OFF → approx. f/11 @ 1/100s
	•	Underexposure readout in stops (e.g., “Under by 1.3 stops”).
	•	Calibration panel for real-world accuracy:
	•	Quick presets (Sunny, Hazy, Overcast, Shade) based on EV at ISO 100.
	•	Manual EV set using a gray card or mid-tone surface.
	•	Persistent calibration (saves in local browser storage).
	•	Runs entirely client-side — no data is sent anywhere.
📷 How it Works

Because web browsers auto-expose the video feed and don’t expose actual aperture/shutter data, the app uses a calibration approach:
	1.	Measures average brightness of the center box (Rec.709 weighted luma).
	2.	Converts to EV (Exposure Value) using your calibration constant.
	3.	Compares the scene EV to the H35N’s fixed shutter/aperture and your selected ISO.
	4.	Displays how many stops you are underexposed (negative values).

⸻

🛠 Setup & Usage

1. Open the App
	•	Host the index.html file on a HTTPS server, or open it directly on your Mac and access it on your iPhone.
	•	Example local test:
⚠️ Notes & Limitations
	•	Works best outdoors or in bright light; very dark scenes may be noisy.
	•	Calibration is scene-specific — recalibrate when lighting changes.
	•	Browser metering is approximate; this tool is for quick reference, not lab accuracy.
	•	Tested primarily on iPhone 15 Safari.

⸻

📄 License

MIT License — free to use, modify, and share.

