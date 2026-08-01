# Certificates-Generator (Ultra-Realistic Edition)

We have automated the process of generating certificates for participants who have attended workshops, events, or competitions conducted by college clubs and student organizations.  
This program automatically generates the certificates of the members by giving their details as input and saves them in both .jpg and .pdf file formats for better compatibility. 
It saves a lot of time by generating certificates of multiple people at the same time within a few seconds, which otherwise takes a lot of time if to be done manually.

##  New Features (Ultra-Realistic Edition)

###  Intelligent Text Placement
- **Automatic zone detection**: Analyzes your certificate template to find the best text placement area
- **Configurable placement zones**: Define exactly where names should appear on your certificates
- **Support for inline text**: Place names in the middle of sentences or paragraphs naturally

###  Humanized Generation
- **Natural variations**: Each certificate has subtle, unique positioning (±5 pixels)
- **Adaptive font sizing**: Automatically adjusts font size based on name length
- **Realistic color variations**: Slight color differences make certificates look hand-crafted
- **Ultra-realistic output**: Certificates look professionally made, not machine-generated

###  Flexible Configuration
- **Multiple placement zones**: Support different certificate layouts automatically
- **JSON configuration**: Easy-to-edit configuration file for custom positioning
- **Visual guides**: Comprehensive documentation with examples for every scenario

## Introduction 
Certificates Generator is an intelligent Python project to generate ultra-realistic certificates with natural text placement. It features a GUI-based application with advanced image analysis capabilities.

## Technologies

Project is built using:
* **Python** (Core application programming language)
* **Tkinter** (Lightweight GUI dialog for file selection)
* **Pillow (PIL)** (High-speed template rendering and text drawing)
* **OpenPyXL** (Reading student credentials and metadata from Excel `.xlsx`)
* **img2pdf** (Converting generated raster certificates into high-DPI PDF documents)
* **Subprocess & PIP** (Automated runtime dependency installation and management)

## Setup
To run this project, follow the below instructions:

1.	Copy the code from `certificates.py` python file to python IDLE or any interactive interpreter.
2.	Make sure all the related files such as certificate template `certificates.png` and true type font file `Lora-Bold.ttf` are in the same folder.
3.	Make sure that the excel file `sample certificates.xlsx`, used for the details of the participants, exists on the system.
4.	Run the program - it will automatically install all required dependencies.
5.	Select your Excel file when prompted.
6.	The program will automatically generate a `text_placement_config.json` file on first run.
7.	Successful generation of certificate for each member is shown with progress indicators and zone information.
8.	Finally, a success message will be printed with the total count of generated certificates.
9.	`All_Certificates` folder will be created in the specified directory path. Subfolders named `Images` and `PDFs` are created, which store images and portable document formats (pdf) of all generated certificates respectively.

##  Customizing Text Placement

### Quick Start
The program works out-of-the-box with intelligent defaults. For custom placement:

1. **Run the program once** - it creates `text_placement_config.json`
2. **Edit the configuration** - adjust zones to match your certificate design
3. **Run again** - names will appear in your specified locations

### Common Scenarios

**Name in the middle of text:**
```json
"y_range": [0.40, 0.50]  
```

**Name below header:**
```json
"y_range": [0.35, 0.45]
```

**Name above signature:**
```json
"y_range": [0.55, 0.68]
```

See `QUICK_SETUP.md` for detailed examples and `CONFIGURATION_GUIDE.md` for comprehensive documentation.

## Features
 Certificates generated and saved in both image (.png) and document (.pdf) formats  
 Intelligent text placement with automatic zone detection  
 Natural, humanized variations for realistic appearance  
 Adaptive font sizing based on name length  
 Configurable placement zones for any certificate design  
 Support for inline text placement (names in the middle of sentences)  
 Progress tracking with detailed output  
 Error handling and recovery  
 Automatic dependency installation  

## 📚 Documentation & Roadmap

- **[QUICK_SETUP.md](Certificates%20Generator/QUICK_SETUP.md)** - Common scenarios and ready-to-use zone configurations
- **[VISUAL_GUIDE.txt](Certificates%20Generator/VISUAL_GUIDE.txt)** - Detailed ASCI architectural breakdown of the relative 0.0–1.0 coordinate grid
- **[FUTURE_WORKS.md](FUTURE_WORKS.md)** - Comprehensive engineering roadmap for Web App, API, Database, and QR verification extensions
- **text_placement_config.json** - Auto-generated configuration file (editable runtime preferences)

##  Example Output

Each certificate generation shows:
```
 Row 3: John Smith                    → Zone: center_middle
 Row 4: Jane Doe                      → Zone: center_middle
 Row 5: Alexander Hamilton            → Zone: center_middle
```

Final summary:
```
 Success! Generated 25 certificates
 Location: C:\path\to\All_Certificates
```

##  Advanced Features

- **Multiple zone support**: Define fallback zones for different certificate types
- **Variance-based detection**: Automatically finds uniform areas suitable for text
- **Priority system**: Control which zones are preferred
- **Natural randomization**: Configurable offset ranges for human-like variations
- **Adaptive algorithms**: Smart font sizing prevents text overflow

## 💡 Tips for Best Results

1. Use high-resolution certificate templates (recommended: 2000x1500px or higher)
2. Ensure text placement areas have uniform backgrounds
3. Test with a few rows before generating hundreds of certificates
4. Keep the font file (`Lora-Bold.ttf`) in the same directory
5. Use the configuration guides to fine-tune positioning and offset tolerances

---

## 🚀 Future Works & Architectural Roadmap

We have structured an exciting evolutionary architecture path to transform this offline utility into a dynamic Web Application and SaaS credential verification system. Key upcoming milestones include:

* **⚡ Phase 1 (CLI & Portability):** Headless multi-threaded CLI mode and standalone double-click `.exe` bundle using PyInstaller.
* **🌐 Phase 2 (Full-Stack Web App):** A interactive **React / Next.js** dashboard featuring a real-time **Visual Drag-and-Drop Zone Configurator** backed by a stateless **FastAPI** Python streaming server.
* **🏢 Phase 3 (SaaS & Anti-Forgery Database):** Integration of a **PostgreSQL** database layer to embed unique cryptographic **QR Code Verification Tags** on every certificate, accompanied by an automated background email & WhatsApp distribution queue.

📖 **For detailed technical architecture diagrams and tech stack breakdown, read the complete [Future Works Roadmap](FUTURE_WORKS.md).**

---

**Designed for College Clubs & Student Societies | Enhanced with AI-Powered Intelligent Text Positioning**
