# SnapOCR
An intuitive GUI-based OCR tool with screenshot-like functionality.

[中文版說明](./README_zh.md)

## Overview
SnapOCR is an **efficient and user-friendly** Optical Character Recognition (OCR) tool, designed for **fast and reliable text extraction** from any part of the screen.

## Use Cases
![Test](./asset/Test.gif)
- **Seamless text extraction for LLMs** (e.g., ChatGPT, Claude) without input limitations.
- **Extracting text directly from PC game screens.**
- **Enhancing PDF reading** by quickly capturing and recognizing text.

## Features
- **One-click text extraction** – No need to save screenshots.  
- **Clipboard integration** – Extracted text is automatically copied for easy pasting.  
- **Supports multiple languages** – Works well with various OCR needs.  
- **Optimized for speed** – Leverages GPU acceleration for faster processing (optional).  

## Installation
### **System Requirements**
- **Windows 10+** (Tested on Windows 10 with Python 3.10)
- **Python 3.10**
- **NVIDIA GPU (optional)** – Recommended for faster OCR processing.

### **Setup & First-Time Run**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/SnapOCR.git
   cd SnapOCR
   ```
2. Run SnapOCR.bat
- The first launch may take some time as dependencies are installed.
- Subsequent runs will be faster.

## Usage
1. Launch SnapOCR – Run SnapOCR.bat.
2. Click the button – Select any part of the screen.
3. OCR processing – The text is extracted instantly.
4. Text is copied to clipboard – Paste it anywhere (e.g., ChatGPT, Google Translate).

## Credit
A huge thanks to the following open-source projects:
- [Surya](https://github.com/VikParuchuri/surya) – Powerful OCR model by VikParuchuri.
- [PyAutoGUI](https://github.com/asweigart/pyautogui) – Intuitive automation tools by asweigart.
- [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter) – Beautiful and modern UI by TomSchimansky.