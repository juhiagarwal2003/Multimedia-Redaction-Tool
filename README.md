# 🔒 Multimedia Redaction Tool

> ✨ *Redact it. Blur it. Protect it.*  
> A powerful all-in-one redaction tool to safeguard sensitive data in **text, images, and videos** — with support for **English and Hindi**. Built with **Streamlit**, and powered by **spaCy**, **OpenCV**, and **Tesseract OCR**.

---

## 🚀 What Can It Do?

🔹 **Text Redaction**  
→ Auto-redact sensitive entities (like names, organizations, locations, dates) from PDFs, DOCX files, and even images via OCR.  

🔹 **Face Redaction**  
→ Blur faces in both images and videos using facial detection.  

🔹 **Multilingual Support**  
→ Redacts both **English** and **Hindi** text using spaCy NER models.  

---

## 📁 Supported File Formats

| File Type | Extensions Supported |
|-----------|----------------------|
| Documents | `.pdf`, `.docx`      |
| Images    | `.jpg`, `.png`       |
| Videos    | `.mp4`               |

---

## 🧰 Tech Stack

- 🎯 **Streamlit** – Sleek and fast web UI  
- 🧠 **spaCy** – Named Entity Recognition for text  
- 🧪 **Tesseract OCR** – Text extraction from images  
- 👁️ **OpenCV** – Face detection in media  
- 📄 **pdfplumber** – PDF text extraction  
- 🧾 **python-docx** – Word document handling  
- 🧙 **Faker** – For generating synthetic data

---

## ⚙️ Installation Guide

### 🔧 Prerequisites

- Python 3.7+
- Visual Studio Code (VS Code)
- Tesseract OCR ([Download here](https://github.com/tesseract-ocr/tesseract))

> ⚠️ After installing Tesseract, update this line in `app.py`:
```python
pytesseract.pytesseract.tesseract_cmd = r'C:\Program Files\Tesseract-OCR\tesseract.exe'
```

---

### 📦 Setup Instructions

```bash
# Clone the repository
git clone https://github.com/yourusername/multimedia-redaction-tool.git
cd multimedia-redaction-tool

# Create and activate virtual environment
python -m venv venv      # or python3 -m venv venv
# Then activate it:
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Download spaCy models
python -m spacy download en_core_web_trf
python -m spacy download xx_ent_wiki_sm
```

---

## 🚀 Running the App

```bash
streamlit run app.py
```

Then, go to [http://localhost:8501](http://localhost:8501) in your browser.

---

## 🧑‍💻 VS Code Setup (Optional but Recommended)

1. Open the project folder in VS Code  
2. Select the correct Python interpreter (`./venv/bin/python` or `.\\venv\\Scripts\\python.exe`)  
3. Install the Python extension if not already done  
4. Run and debug Streamlit from VS Code:
   - Go to Run > Add Configuration > Python
   - Use this `launch.json`:
```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Streamlit",
            "type": "python",
            "request": "launch",
            "module": "streamlit",
            "args": ["run", "${workspaceFolder}/app.py"],
            "console": "integratedTerminal"
        }
    ]
}
```

---

## 🧪 How to Use

### 📝 Text Redaction (PDF / DOCX / Image)

1. Upload a document or image file  
2. Select entities to redact: `PERSON`, `ORG`, `DATE`, `GPE`, etc.  
3. Click **Redact**  
4. View the cleaned output directly in the browser

---

### 🖼️ Face Redaction (Images)

1. Upload an image file (`.jpg`, `.png`)  
2. The app auto-detects and blurs all faces  
3. View side-by-side original and redacted images

---

### 🎞️ Face Redaction (Videos)

1. Upload a `.mp4` video  
2. Each frame is scanned and blurred  
3. Redacted video is rendered for playback in the app

---

## 🧪 Example Use Cases

- **Legal Documents**: Mask identities in scanned agreements  
- **Surveillance Footage**: Blur individuals in public-facing media  
- **Dataset Privacy**: Clean training data before sharing

---

## 🧾 Project Structure (Essentials)

```
.
├── app.py                 # Main Streamlit application
├── README.md              # You are here ✨
├── requirements.txt       # Python package dependencies
├── venv/                  # Virtual environment
```

---

## 📦 Dependencies

Install everything using:

```bash
pip install -r requirements.txt
```

### Main Packages:

- `streamlit==1.25.0`
- `pdfplumber==0.7.6`
- `docx==0.2.4`
- `faker==19.2.0`
- `spacy==3.7.0`
- `pytesseract==0.3.10`
- `opencv-python==4.8.0.76`
- `opencv-python-headless==4.8.0.76`
- `langdetect==1.0.9`
- `Pillow==10.0.0`
- `numpy==1.23.5`

---

## 📬 Contributions Welcome

Got an idea? Found a bug?  
Open an issue or submit a pull request.  
Let's build safer tools together 💪

---

## 📝 License

MIT License – Use it. Improve it. Share it.  
Just don't forget to give credit 🤝

---

### Made with ❤️ using open source tools.
