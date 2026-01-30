# Signuity — AI Signature Verification Tool

Signuity is a desktop application that verifies whether a questioned signature matches a set of genuine reference signatures using AI. It provides a similarity score, a genuine/forged decision, and forensic-style visualizations (heatmap, saliency, zoom) that can be included in a downloadable PDF report.

---

## File Details

- **Size:** The application folder is approximately **3 GB**. This is normal: it includes the full app, a bundled Python engine, and ML models (ONNX and PyTorch) so the tool runs entirely on your computer without needing to download anything.
- **Nature:** This is a **portable** package: there is no system installer. You unzip the folder and run `Signuity.exe` from inside it. Do not move or delete files inside the folder, or the app may stop working.
- **Offline:** The app is designed to work **offline**. No internet connection is required for verification or PDF generation.

---

## System Requirements

- **OS:** Windows 10 or Windows 11 (64-bit)
- **RAM:** 4 GB minimum; 8 GB or more recommended for smoother use
- **Disk:** At least 4 GB free space (for the app folder and any outputs)
- **Display:** 1280×720 or higher recommended

---

## Installation Instructions

1. **Unzip** the downloaded file (e.g. `Signuity-win32-x64.zip`) to a folder of your choice (e.g. `Desktop\Signuity`).
2. **Do not** run the app from inside the zip file. Always run it from the unzipped folder.
3. **Optional:** If your antivirus warns about `server.exe` or the folder, add the Signuity folder to the exclusion list. The app uses a local engine and does not connect to the internet for verification.
4. Double-click **`Signuity.exe`** to start the application.
5. **First launch:** The window may take **10–90 seconds** to appear while the engine loads. This is normal. Do not close the app during this time.

---

## User Guide — How to Use

### 1. Start the app

- Double-click **Signuity.exe**.
- Wait until the main window appears (it may take 10–90 seconds on first launch).

### 2. Upload reference signatures

- Under **REFERENCE IMAGE/SIGNATURE**, upload **exactly 4** genuine (authentic) signature images.
- Use **Browse** or drag-and-drop. Supported formats: **JPG**, **PNG** (max 10 MB per file).
- The counter should show **Uploaded: 4/4**.
- A sample signatures from CEDAR dataset are uploaded and grouped in the folder above.
- Naming convention: original_[writernum]_[signaturenum], ex: original_1_2 and original_1_3 are from the same signer. The same applies with the forgeries too.

### 3. Upload the questioned signature

- Under **QUESTIONED IMAGE/SIGNATURE**, upload **1** signature image to verify.
- Same formats and size limit as above.

### 4. Run verification

- Click **Verify** (or equivalent button).
- Wait for processing. When finished, you are taken to the results page.

### 5. View results

- You will see:
  - **Result:** Genuine or Forged.
  - **Similarity score** (and raw distance / threshold if shown).
  - **Visualizations:** heatmap, saliency, and zoom views of the signatures.

### 6. Download PDF report (optional)

- Click the download icon at the top right corner of the result box to create and download a report containing the result and visualizations.
- The PDF is saved to your usual Downloads folder (or the location your browser/app uses).

### Tips

- Use clear, cropped signature images for best results.
- The app may show warnings for very low-resolution or non-signature images; you can choose to proceed anyway if you trust the input.

---

## Troubleshooting

| Issue | What to do |
|-------|------------|
| **"Engine is starting or unavailable. Please wait…"** | Wait 10–60 seconds and click **Verify** again. If it persists, close the app fully and start it again. You may check your Task Manager to see if Python Server is starting. |
| **Window never appears** | Wait up to 90 seconds. If it still does not open, check that no antivirus is blocking `Signuity.exe` or `server.exe`, and that the folder was fully unzipped. |
| **App closes immediately** | Run `Signuity.exe` from the unzipped folder (not from inside the zip). Add the folder to your antivirus exclusions if needed. |
| **Verification very slow** | First run can be slower while models load. Later runs are faster. Ensure you have enough free RAM and disk space. |

---

## Uninstalling

- **Remove the app:** Delete the entire Signuity folder (e.g. `Signuity-win32-x64`) that you unzipped. There is no separate uninstaller.
- **Remove app data (optional):** To clear logs and any stored data, delete the folder:  
  `%APPDATA%\signuity`  
  (Open Run with `Win + R`, type `%APPDATA%\signuity`, press Enter, then delete the folder if it exists.)

---

If you received this README with a packaged copy of Signuity, keep it in the same folder as `Signuity.exe` for reference.
