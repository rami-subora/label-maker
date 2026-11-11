# label-maker
# 🏷️ Universal Sticker Studio & Label Maker

A lightweight, zero-dependency client-side web utility engineered to design, calibrate, and print onto pre-cut label and sticker sheets (specialized for **Ref. 1276 / Avery 3652**, with universal grid calculation support for A4 and US Letter).

Built to solve the notorious margins, table shifting, and alignment issues that occur when attempting to print sticker sheets from traditional word processors like Microsoft Word.

---

## 🚀 Live Demo

Try the live application hosted directly on GitHub Pages:
**[https://rami-subora.github.io/label-maker/](https://rami-subora.github.io/label-maker/)**

---

## ✨ Key Features

### 1. 🧮 Automatic Grid & Dimension Calculator
* Enter any number of **Columns** and **Rows**; the tool instantly calculates the physical sticker dimensions in millimeters ($W \times H$).
* Supports both standard **A4** ($210 \times 297\text{ mm}$) and **US Letter** ($215.9 \times 279.4\text{ mm}$) sheet metrics.
* Preconfigured with instant presets for popular sheets:
  * **Ref. 1276:** 3 × 7 (70.0 × 42.4 mm — 21 stickers/sheet)
  * **Ref. 1263:** 3 × 8 (70.0 × 37.1 mm — 24 stickers/sheet)
  * **Ref. 1277:** 2 × 7 (105.0 × 42.4 mm — 14 stickers/sheet)
  * **Ref. 1264:** 2 × 2 (105.0 × 148.5 mm — 4 shipping labels/sheet)
  * **Avery 5160:** 3 × 10 (US Letter address labels)

### 2. ♻️ Partial Sheet Saver (Click-to-Skip)
* Never waste an unfinished sticker sheet.
* **Direct Canvas Interaction:** Click any individual sticker slot on the live canvas to mark it as **SKIPPED**.
* **Quick Start Field:** Input `Start printing at sticker #X` to skip the first $N$ already-peeled labels.
* Active items automatically cascade forward without dropping data.

### 3. 🛡️ Hardware Non-Printable Margin Guard
* Standard office laser printers (such as the **Lexmark X954**) cannot physically print within the outer **4.2 mm** edge of the sheet.
* Features a calibrated **4.5 mm safe margin** with a toggleable visual boundary so text is never truncated on edge-to-edge stickers.

### 4. 🔤 Dynamic Tokens & Custom Variables
* Built-in dynamic variables:
  * `{n}`: Sequential sticker index
  * `{total}`: Total active sticker count
  * `{date}`: Current timestamp date (`YYYY-MM-DD`)
* **User-Defined Variables:** Define custom tags (e.g., `{batch}`, `{inspector}`, `{price}`) and click to insert them across headings, bodies, or QR codes.

### 5. 📱 Embedded QR Code Generator
* 1-click toggle to embed scannable QR codes on each label using dynamic URLs or serial numbers.
* Adjustable left/right positioning.

### 6. 💾 Zero-Friction Auto-Save (`localStorage`)
* Silently caches all text inputs, custom variables, colors, and layout configurations directly in your browser.
* Refreshing or closing the tab restores your work immediately without requiring an account.

### 7. 🖨️ Precision Export Options
* **Direct 300-DPI PDF Download:** Client-side vector-scale export using `jsPDF` and `html2canvas` at exact $1:1$ scale.
* **Open Printable Tab:** One-click fail-safe tab for native OS print dialogs (`Ctrl+P` / `Cmd+P`).
* **Test Border Mode:** Toggles dashed cutlines for test runs on standard plain paper before using expensive sticker paper.

---

## 🛠️ Recommended Printer Settings

To guarantee perfect physical alignment:

1. **Paper Size:** Ensure the printer dialog matches the project format (**A4** or **US Letter**).
2. **Scale:** Always set to **"100%"** or **"Actual Size"**. Never select *"Fit to Page"* or *"Shrink to Fit"*.
3. **Media Type:** Select **"Labels"** or **"Heavy Paper / Cardstock"** in your printer preferences (under *Media & Quality*).
4. **Feeder:** Feed sticker paper through the **Multipurpose / Bypass Feeder Tray** for the straightest paper path and optimal toner fusion.

---

## 💻 Tech Stack

* **Core:** Semantic HTML5, Vanilla JavaScript (ES6+)
* **Styling:** [Tailwind CSS](https://tailwindcss.com/)
* **Icons:** [Lucide Icons](https://lucide.dev/)
* **PDF Engine:** [jsPDF](https://github.com/parallax/jsPDF) + [html2canvas](https://html2canvas.hertzen.com/)
* **QR Generator:** [QRious](https://github.com/neocotic/qrious)

---

## 📄 License

MIT License. Free to use, adapt, and distribute.
