StegoLab — Elevate Labs Internship Steganography SuiteA dual-delivery steganography tool created during the Elevate Labs Internship. StegoLab offers both an offline desktop utility (Python/Tkinter) with optional AES-GCM encryption and a modern, client-side web application (React + TypeScript) that runs entirely in the browser.Highlights
Two implementations in one project: Desktop (Python) + Web (React/TypeScript)
Hide/extract text or arbitrary files inside lossless images (PNG/BMP)
Optional strong encryption using AES-GCM with a passphrase
Drag-and-drop UX in both desktop and web versions
No server required for the web version — runs fully in the user’s browser
What’s Included1) Python Desktop App (Tkinter)
Purpose: Offline, user-friendly desktop steganography with encryption
Key features:

Supports PNG and BMP (lossless) image formats
Embed/extract text or files
Optional AES-GCM encryption with passphrase-derived key
Drag-and-drop support (tkinterdnd2)
GUI status updates and simple workflow


Quick start:
bashCopy code[data-radix-scroll-area-viewport]{scrollbar-width:none;-ms-overflow-style:none;-webkit-overflow-scrolling:touch;}[data-radix-scroll-area-viewport]::-webkit-scrollbar{display:none}git clone https://github.com/username/Elevate_Labs_Internship_Project_Steganography_Tool.git
cd Elevate_Labs_Internship_Project_Steganography_Tool/python
pip install pillow pycryptodome tkinterdnd2
python stego_tool.py

2) Web App (React + TypeScript + Vite)
Purpose: Fast, modern browser-based steganography — no backend, instant usage
Key features:

Built with React + TypeScript and styled with TailwindCSS
AES-GCM encryption/decryption implemented in the client
Drag-and-drop for images and files
Extract hidden content directly in the browser and download results
Optionally published to static hosting for immediate access


Quick start:
bashCopy code[data-radix-scroll-area-viewport]{scrollbar-width:none;-ms-overflow-style:none;-webkit-overflow-scrolling:touch;}[data-radix-scroll-area-viewport]::-webkit-scrollbar{display:none}cd Elevate_Labs_Internship_Project_Steganography_Tool/project
npm install
npm run dev
# Build for production:
npm run build

How It Works (High Level)
Choose an image (PNG/BMP).
Choose text or file to hide; optionally provide a passphrase.
The tool encodes the payload into the image pixels using a steganographic embedding algorithm.
If encryption is enabled, the payload is encrypted with AES-GCM before embedding.
To retrieve: provide the stego-image (and passphrase if used) to extract and decrypt the hidden payload.
Project LayoutElevate_Labs_Internship_Project_Steganography_Tool/
├── python/               # Desktop Tkinter application
│   └── stego_tool.py     # Main GUI app + embedding/extraction logic
│
├── project/              # Web client (React + TypeScript)
│   ├── src/              # React source code
│   ├── steganography.js  # Encoding/decoding & crypto logic (client-side)
│   ├── app.js
│   └── ...
Security Notes
Use PNG/BMP only — lossy formats (e.g., JPEG) will corrupt embedded data.
AES-GCM provides confidentiality and integrity. Keep your passphrase safe.
Client-side web version stores and processes data locally in the browser — no server uploads by design.

## 📸 Screenshots
### Web Version
### Main Window
![Screenshot 1](https://github.com/jagadeep18/Elevate_Labs_Internship_Project_Steganography_Tool/blob/main/Screenshot_1.png?raw=true)

![Screenshot 2](https://github.com/jagadeep18/Elevate_Labs_Internship_Project_Steganography_Tool/blob/main/Screenshot_2.png?raw=true)

---

## 🛠 Dependencies

### ✅ Python Version
- Python 3.x  
- Pillow  
- PyCryptodome  
- Tkinter (built-in)  
- tkinterdnd2 (optional, for drag-and-drop)  

### ✅ Web Version
- React + TypeScript + Vite  
- TailwindCSS  
- JavaScript (steganography logic)  

---

## ⚠️ Notes
- 📌 Use **PNG or BMP files only** — JPEG may corrupt hidden data.  
- 🔐 AES encryption is **optional but highly recommended**.  
- 📂 Drag-and-drop is enabled in both versions (requires `tkinterdnd2` in Python).  

---

## 👨‍💻 Author
Developed by *Adhaveni Rakesh**  
🧑‍💻 Internship Project @ **Elevate Labs**


