# origin-trace-core
A forensic watermarking and timestamping protocol for digital content. Proves "Priority of Possession" using invisible frequency-domain steganography and immutable timestamping.
# OriginTrace (Beta)

**"We don't prove you created it. We prove you had it first."**

OriginTrace is a digital forensic tool designed to protect small creators. It embeds an invisible, robust UUID into image and video files (using DWT/DCT Steganography) and logs a timestamp. If content is stolen and reposted, this tool detects the hidden signature even after re-encoding or cropping.

## ⚠️ Important Legal Disclaimers

1.  **Not Legal Advice:** This software is a technical proof-of-concept. The maintainers are not lawyers. The "Evidence Reports" generated are data visualizations, not court orders.
2.  **Proof of Priority, Not Creation:** This tool certifies **Proof of Possession**. It proves the user possessed the file at Timestamp A. It does not verify the user is the original copyright holder (e.g., if a user uploads a Disney movie, we only prove they had the file at that time).
3.  **User Responsibility:** The user assumes all liability for any claims made against third parties using data from this tool.

## 📄 License & Commercial Use
**License:** "Source Available - Non-Commercial"

This code is open for educational use and individual auditing.
*   ✅ You may fork this repo to test it or contribute.
*   ❌ **You may NOT** use this code to build a paid service, SaaS, or commercial product without explicit written permission from the original author.
*   ❌ Commercial forks or re-branding are strictly prohibited.

## 🛠 Tech Stack
*   **Backend:** Python 3.11 (Google Cloud Functions)
*   **Forensics:** OpenCV, invisible-watermark (DWT/DCT), NumPy
*   **Database:** Google Firestore (NoSQL)
*   **Frontend:** Flutter (Web/Mobile)

## 🚀 How it Works
1.  **Ingest:** Creator uploads content.
2.  **Stamp:** System injects a hidden UUID via Frequency Domain Watermarking.
3.  **Verify:** If the content appears elsewhere, the Creator uploads the "stolen" file. The system extracts the UUID to confirm the chain of custody.
