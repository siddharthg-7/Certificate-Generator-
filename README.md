<div align="center">
  <h1>🎓 Automated Certificate Generator</h1>
  <p><b>An intelligent, ultra-realistic certificate generation engine designed for college clubs, technical events, and student communities.</b></p>

  <p>
    <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python Version"/></a>
    <a href="https://python-pillow.org/"><img src="https://img.shields.io/badge/Pillow-Image%20Processing-0078D4?style=for-the-badge&logo=python&logoColor=white" alt="Pillow"/></a>
    <a href="https://github.com/siddharthg-7/Certificate-Generator-/stargazers"><img src="https://img.shields.io/badge/PRs-Welcome-28A745?style=for-the-badge&logo=github&logoColor=white" alt="PRs Welcome"/></a>
    <a href="https://github.com/siddharthg-7/Certificate-Generator-/blob/main/README.md"><img src="https://img.shields.io/badge/Maintained%3F-yes-6c5ce7?style=for-the-badge" alt="Maintained"/></a>
  </p>
</div>

---

## Why This Project?

If you've ever organized a hackathon, college workshop, or society competition, you know the grueling post-event chore: spending hours manually typing participant names into design software, exporting files one by one, and struggling with inconsistent alignments. 

We built **Certificates Generator** to automate this entire workflow. In just a few seconds, it transforms an ordinary Excel roster into high-resolution, perfectly aligned **PNGs and high-DPI PDFs**—ready for instant distribution. 

Unlike primitive scripts that stamp rigid, robotic text onto an image, our **Ultra-Realistic Edition** leverages intelligent zone positioning, natural spatial variation, and adaptive typography. The result? **Certificates that look authentically hand-crafted by a graphic designer.** 🎨✨

---

##  Key Features (Ultra-Realistic Edition)

###  1. Intelligent & Adaptive Placement
- **Automatic Zone Detection:** Smartly scans the contrast and layout of your certificate template (`.png`) to identify optimal text placement areas.
- **Dynamic Font Sizing:** Dealing with a long name like *"Alexander Hamilton"* or a short name like *"Lee"*? The rendering engine dynamically recalculates font scaling and kerning to prevent awkward wrapping and overflows.
- **Inline Text Support:** Seamlessly embeds names inside descriptive sentences or structured paragraphs (e.g., *"This is proudly presented to `[NAME]` for outstanding contribution..."*).

###  2. Humanized Generation
- **Natural Spatial Variations:** Applies micro-offsets (±5 pixels) to emulate natural, organic positioning so that no two certificates share identical mathematical alignments.
- **Realistic Aesthetic Assurance:** Designed specifically to eliminate the "machine-generated" look, ensuring formal and professional output every time.

###  3. Effortless Execution
- **Zero-Config Dependency Installer:** Run the script once, and it will automatically invoke `pip` in the background to set up essential libraries (`openpyxl`, `Pillow`, `img2pdf`). No manual virtual environment hassle!
- **Interactive File Picker:** Features a smooth native GUI dialog to browse and choose your `.xlsx` roster without tampering with code paths.
- **Dual-Format Compilation:** Concurretly outputs lossless raster graphics (`.png`) and publication-grade vector documents (`.pdf`) for versatile delivery via email or messaging platforms.

---

##  Built With

| Component | Technology | Role & Description |
| :--- | :--- | :--- |
| **Core Engine** | `Python 3` | Main orchestration, logical flow, and runtime management |
| **Image Rendering** | `Pillow (PIL)` | High-speed TrueType typography drawing & raster compositing |
| **Data Extraction** | `openpyxl` | Parsing student columns, registration IDs, and metadata from Excel sheets |
| **Vector Compilation** | `img2pdf` | Lossless conversion from buffered raster images to standard PDF deliverables |
| **Native GUI** | `tkinter` | Cross-platform interactive desktop dialog for intuitive roster loading |

---

##  Getting Started

###  Prerequisites
All you need installed on your machine is **Python 3.8+**. The script natively resolves and installs all third-party dependencies automatically upon initiation!

###  Quick Setup Guide
1. **Clone the Repository** (or download the ZIP bundle):
   ```bash
   git clone https://github.com/siddharthg-7/Certificate-Generator-.git
   cd Certificate-Generator-
   ```
2. **Prepare Your Template & Roster**:
   - Place your background certificate template named `certificates.png` in the project folder.
   - Ensure your TrueType font file named `Lora-Bold.ttf` (or your preferred font configured in JSON) is present.
   - Create or populate an Excel file (`.xlsx`) with participant IDs in **Column A** and names in **Column B** (check `sample certificates.xlsx` for reference).
3. **Launch the Engine**:
   ```bash
   python certificates.py
   ```
4. **Select Your Excel File**: When the graphical window prompts you, select your roster file.
5. **Collect Your Certificates**: Check the automatically generated `Output/Images` and `Output/PDFs` directories for your pristine certificates! 🎉

---

##  Customizing Text Placement

On first execution, the generator outputs an easily editable `text_placement_config.json` file. You can customize spatial bounding boxes and zones to effortlessly fit any layout style.

###  Common Layout Scenarios

| Placement Layout | Target Use Case | Example JSON Configuration |
| :--- | :--- | :--- |
| **Inline Paragraph** | Embedding names inside an introduction sentence | `"y_range": [0.40, 0.50]` |
| **Below Header Banner** | Centering names under large "Certificate of Participation" headers | `"y_range": [0.35, 0.45]` |
| **Above Signatory Line** | Positioning formal titles right above footer signatures | `"y_range": [0.55, 0.68]` |

>  **Pro-Tip:** Review our **[QUICK_SETUP.md](QUICK_SETUP.md)** for ready-to-use configuration presets and our **[VISUAL_GUIDE.txt](VISUAL_GUIDE.txt)** for an ASCII breakdown of the normalized `0.0`–`1.0` grid system!

---

##  Sample Console Output

Here is what running a high-speed batch generation looks like in your terminal:

```console
$ python certificates.py
[System] All dependencies verified successfully.
[GUI] Roster selected: sample certificates.xlsx
[Engine] Initializing Ultra-Realistic Text Placer (Offset: ±5px)...

 ✔ Row 3: John Smith                    → Zone: center_middle (Compiled PNG & PDF)
 ✔ Row 4: Jane Doe                      → Zone: center_middle (Compiled PNG & PDF)
 ✔ Row 5: Alexander Hamilton            → Zone: center_middle (Compiled PNG & PDF)

=======================================================
  Success! Generated 25 certificates in 3.12 seconds.
 Location: C:\project-self-1\Output\
=======================================================
```

---

##  Documentation & Roadmap

We are continuously pushing the architecture of this utility forward into a full-scale verification platform:

-  **[Quick Setup Guide (QUICK_SETUP.md)](QUICK_SETUP.md)**: Common placement layouts and configuration recipes.
-  **[Coordinate Grid Reference (VISUAL_GUIDE.txt)](VISUAL_GUIDE.txt)**: Deep dive into relative spatial bounding boxes and geometry.
-  **[Architectural Roadmap (FUTURE_WORKS.md)](FUTURE_WORKS.md)**: Our engineering roadmap toward developing a full-stack dashboard and cryptographic QR code anti-forgery database.

---

##  Contributing

We warmly welcome ideas, feature suggestions, and pull requests from student societies, college clubs, and developers worldwide!
1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

<div align="center">
  <p><b>Designed & Engineered for College Clubs, Tech Societies, and Open Source Hackers </b></p>
  <p> Star this repository if it saved your weekend!</p>
</div>
