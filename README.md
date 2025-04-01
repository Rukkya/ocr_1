# OCR Web App using Flask and Gradio

This project is an **Optical Character Recognition (OCR) Web App** built using **Flask, Gradio, OpenCV, and Tesseract**. It allows users to extract text from images via a **Flask API endpoint** or a **Gradio UI**.

## 🚀 Features
- **OCR Extraction**: Uses Tesseract to extract text from images.
- **Flask API**: Upload an image via an API endpoint to extract text.
- **Gradio Web Interface**: Provides a simple UI for users to upload an image and get extracted text.
- **Supports Multiple Input Formats**: Works with both direct file uploads and NumPy arrays (from Gradio).

## 🛠️ Installation
### 1️⃣ **Clone the Repository**
```bash
git clone https://github.com/rukkya/ocr-web-app.git
cd ocr-web-app
```

### 2️⃣ **Set Up a Virtual Environment (Optional but Recommended)**
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

### 3️⃣ **Install Dependencies**
```bash
pip install -r requirements.txt
```

### 4️⃣ **Install Tesseract OCR**
#### Linux (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install tesseract-ocr
```
#### macOS (Using Homebrew)
```bash
brew install tesseract
```
#### Windows
Download and install Tesseract from:
[Tesseract OCR GitHub](https://github.com/UB-Mannheim/tesseract/wiki)

Ensure the **Tesseract executable path** is added to your system's environment variables.

## 🔥 Usage
### **Run the Flask & Gradio App**
```bash
python3 app.py
```

### **Access the Gradio Web UI**
Once the app is running, open the **Gradio interface** in your browser:
```
http://localhost:7860
```

### **API Usage**
#### **Endpoint:** `/process`
#### **Method:** `POST`
#### **Request:** Upload an image file
```bash
curl -X POST -F "file=@path/to/image.jpg" http://127.0.0.1:5000/process
```
#### **Response:**
```json
{
    "extracted_text": "Detected text from the image"
}
```

## 📂 Project Structure
```
ocr-web-app/
│── app.py                  # Main Flask & Gradio App
│── requirements.txt         # Dependencies
│── README.md               # Project Documentation
```

## 📝 To-Do List
- [ ] Add multilingual OCR support
- [ ] Improve text extraction accuracy
- [ ] Deploy the app using Docker or cloud services

## 🤝 Contributing
Pull requests are welcome! If you'd like to contribute, please fork the repo and submit a PR.

## 📜 License
This project is licensed under the **MIT License**.

## 🙌 Acknowledgments
- **Tesseract OCR** for text recognition.
- **Gradio** for the interactive UI.
- **Flask** for the API backend.


