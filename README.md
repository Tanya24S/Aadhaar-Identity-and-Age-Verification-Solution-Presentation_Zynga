# 🛂 Aadhar-Based Identity and Age Verification App

This is a Streamlit-powered application built for the Zynga Hackathon. It verifies user identity by:

1. Extracting the user's **Date of Birth (DOB)** from an uploaded Aadhar card using OCR (Tesseract)
2. Capturing a **live selfie via webcam**
3. Detecting and comparing faces between Aadhar and selfie images using **FaceNet (facenet-pytorch)**
4. Providing real-time feedback on **image clarity** and **lighting**
5. Checking if the user is **18 years or older**

---

## ✅ Features

- 📷 **Webcam Selfie Capture** (`st.camera_input`)
- 🧠 **Face Detection + Matching** (via PyTorch MTCNN + FaceNet)
- 🔍 **DOB Extraction** using Tesseract OCR
- ⚠️ **Warnings for blurry or dark selfies**
- ✅ All done in-browser using **Streamlit**

---

## 🧠 How It Works

- Users upload an image of their Aadhar card
- Users take a live selfie
- The system:
  - Extracts DOB from Aadhar
  - Verifies age (>=18)
  - Detects and compares faces
  - Shows face match confidence

---

## 📦 Setup Instructions

### ✅ Prerequisites
- Python 3.10
- Anaconda (recommended)
- Tesseract OCR installed from [here](https://github.com/UB-Mannheim/tesseract/wiki)

> After installing Tesseract, update the path in `ocr.py` if needed.

---

### 🧰 Create & Activate Environment

You can use the provided environment file:

```bash
conda env create -f environment.yml
conda activate zynga_env

Or install manually:
pip install torch torchvision torchaudio facenet-pytorch opencv-python pytesseract streamlit

🚀 Run the App
streamlit run main.py
Then open your browser at http://localhost:8501.

📁 Folder Structure
Zynga/
│
├── main.py                      # Streamlit frontend
├── environment.yml   
├── utils/
│   ├── age_check.py             # Age verification logic
│   ├── face_compare.py          # Embedding + similarity logic
│   ├── face_detect.py           # Face extraction using MTCNN
│   ├── ocr.py                   # OCR to extract DOB

⚠️ Notes
Make sure your webcam permissions are enabled in your browser
Tesseract must be installed and its path set correctly
No personal data is stored — everything is done locally for demo purposes

👥 Team
No comments
Members- Tanya Sharma, Yashika Mann, Shreya Ruhela

Built for Zynga Hackathon 2025
(IGDTUW)
