# Privacy Policy for QuietNote

**Effective Date:** November 23, 2026  
**Developer:** [Sujil]  
**Contact Email:** [sujilgp@gmail.com]  
**App Package:** `app.quietnote.android`

## 1. Overview
QuietNote ("the App") is a 100% offline, privacy-first voice-to-action and note-taking application. We do not collect, store, transmit, sell, or share any personal or sensitive user data. The App operates entirely on your device with no user accounts, no cloud backend, no analytics, and no advertising SDKs.

## 2. Zero Internet Access (v1.0)
QuietNote v1.0 is engineered without the Android `INTERNET` permission (`android.permission.INTERNET` is explicitly blocked in production builds). Because the App has no network access, it is technically incapable of transmitting your voice recordings, transcripts, or notes off your device. On-device speech-to-text models are delivered directly by Google Play via Google Play Asset Delivery.

## 3. Permissions We Request & How They Are Used
QuietNote requests only the minimum device permissions required for core offline functionality:

* **Microphone (`RECORD_AUDIO`) & Foreground Microphone Service (`FOREGROUND_SERVICE_MICROPHONE`):** Used exclusively when you explicitly trigger a voice recording (via the app, Home Screen widget, or Quick Settings tile). Audio is captured in memory (RAM) for local on-device transcription and is never uploaded or shared.
* **Biometrics (`USE_BIOMETRIC`):** Used solely to authenticate you locally via the Android Keystore so you can lock and unlock your encrypted note vault. QuietNote never accesses or stores your raw biometric data.

## 4. Data Storage & Security
All data you create in QuietNote stays strictly on your device:

* **Encrypted Local Database:** Notes, transcripts, and tasks are stored in a local SQLite database encrypted with SQLCipher (AES-256).
* **Hardware-Backed Keys:** Database encryption keys are protected by the Android Keystore (TEE/StrongBox) and bound to your device's biometric or PIN authentication.
* **No Plaintext Audio Persistence:** Standard voice recordings (up to 90 seconds) are buffered strictly in volatile memory (RAM) during transcription and cleared immediately afterward without writing plaintext audio files to flash storage.
* **Screen Privacy:** The App enables Android's `FLAG_SECURE` flag to prevent unauthorized screenshots and Recent Apps previews.
* **User-Initiated Encrypted Backups (`.qnvault`):** You may manually export your notes into a passphrase-encrypted `.qnvault` archive. Exporting or sharing this file is strictly user-initiated and controlled by you.

## 5. Third-Party Sharing
QuietNote does not integrate any third-party analytics, crash-reporting, or advertising SDKs, and does not share any user data with third parties.

## 6. Data Retention & Deletion
Because we do not collect or store your data on any server, you have complete control over retention and deletion:

* You can delete individual notes or permanently purge items directly inside the App.
* Uninstalling QuietNote from your Android device permanently removes the encrypted local database and all associated keys from your device.

## 7. Children's Privacy
QuietNote is a general productivity utility not directed at children under 13. Because the App collects no personal data from any user, we do not knowingly collect personal information from children.

## 8. Changes to This Privacy Policy
If future versions of QuietNote introduce optional online features (such as Google Play Billing or user-initiated encrypted cloud backups), this Privacy Policy and the Google Play Data Safety section will be updated prior to release.

## 9. Contact Us
If you have any questions about this Privacy Policy or QuietNote's security architecture, please contact us at:  
**Email:** [sujilgp@gmail.com]
