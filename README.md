# Lab Protocol QR Code Generator (Offline Edition)

A simple, private, offline tool to turn your laboratory Excel protocol spreadsheets (`.xlsx`) into scannable QR codes for the **Lab Protocol Runner** mobile app.

---

## 🔒 100% Private & Offline (Air-Gapped)
* **Zero Internet Required:** All conversion happens right inside your web browser. 
* **Corporate Safe:** No data or protocol information is ever uploaded to the cloud or sent across the network.
* **No Installation or Setup:** Works on Windows, Mac, and Linux without installing Python, Node.js, or browser extensions.

---

## 🚀 Quick Start (In 3 Steps)

### 1. Open the Tool
Double-click `protocol_qr_generator_offline.html` to open it in any modern browser (**Google Chrome**, **Microsoft Edge**, **Mozilla Firefox**, or **Safari**).

### 2. Load Your Protocol
* **Drag and drop** your protocol spreadsheet (`.xlsx`) into the dashed upload box, or click the box to browse your computer.
* *(Want to test first? Click **"Load Sample: Dilution Protocol"** or **"Load Sample: 20-Step Assay"** to see it immediately in action).*

### 3. Choose How to Present the QR Code
Depending on where you are working in the lab, pick one of the two delivery views:

* **🖥️ Animated Loop (Scan off your computer monitor):**
  * If your protocol is large, the generator will split it into small, clean parts.
  * Leave the loop playing on your screen. Point the mobile app camera at the monitor—it will automatically detect each part in sequence and assemble the protocol in seconds.
  * You can adjust the cycle speed with the slider (350ms is recommended).

* **🖨️ Side-by-Side (Print Paper SOP Sheets):**
  * Click the **"🖨️ Side-by-Side (Print / SOP)"** tab.
  * Click **"Print Compliance SOP Sheet"** or press `Ctrl + P` (`Cmd + P` on Mac) to print a clean paper sheet for your bench binder or lab notebook.

---

## 💡 Bench Scanning Tips

* **Tough Lighting or Older Phone Cameras?**
  * In the **Optical Chunking & Calibration** section, change the **Target Chunk Size** to `500 Bytes` or `600 Bytes`. Smaller chunks produce larger, less dense QR dots that scan easily through plastic sleeves, bench hoods, or screen glare.
* **Reflections on Monitors:**
  * If overhead fluorescent lights create glare on your computer screen, tilt the monitor slightly downward or dim the room lighting when scanning the animated loop.
* **Pausing the Animation:**
  * You can pause the loop at any time to scan individual parts at your own pace.

---

## 📋 How Your Excel File Should Look

The generator reads standard Excel workbooks containing two worksheets:

1. **`Variables` Sheet** (Optional):
   * Columns: `VariableKey`, `Label`, `Type` (number or text), `Default`, `Unit`
   * Used for initial values like stock concentrations or sample counts.
2. **`Steps` Sheet** (Required):
   * Columns: `Title`, `Instruction`, `Timer` (e.g., `10m`, `45s`), `Type` (`calc`, `number`, `text`, or `table`), `Options`, `Label`, `Variable`, `Value or Expression`, `Unit`
   * Used to define each step of the procedure, automatic dilution/volume math, and data entry fields.

---

