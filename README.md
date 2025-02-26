# AI Medical Assistant

## Overview
AI Medical Assistant is an AI-powered solution designed to assist pharmacists and healthcare professionals by automating prescription analysis and medical image diagnostics. It leverages **Optical Character Recognition (OCR)** for prescription text extraction and **Deep Learning** for disease prediction based on medical images.

## Problem Statement
Medical professionals often face challenges in processing handwritten prescriptions and diagnosing diseases efficiently. Our solution addresses this by:
- Automating prescription recognition to reduce human errors in medication dispensing.
- Using AI to analyze medical images for faster and more accurate disease diagnosis.

## Solution Approach
Our system consists of two core AI functionalities:
1. **Prescription Analysis:** Uses Tesseract OCR to extract text from handwritten prescriptions.
2. **Disease Diagnosis:** Uses a deep learning model to predict diseases from medical images.

## Architecture & Workflow
1. User uploads an image of a prescription or a medical scan.
2. The prescription text is extracted using **Tesseract OCR**.
3. Medical images are analyzed using a **CNN-based AI model** for disease prediction.
4. The processed data is returned via a Flask-based API.

## Technologies Used
- **Programming Languages & Frameworks**
  - Python (Flask for API, OpenCV for image processing)
  - TensorFlow/Keras & PyTorch (for medical image classification)
- **Data Structures**
  - **Heap (`heapq`)**: Prioritizes image processing based on file size.
  - **Queue (`deque`)**: Manages API request processing efficiently.
  - **Dictionary (`defaultdict`)**: Caches extracted prescription text for faster retrieval.
- **Tools & Libraries**
  - Tesseract OCR (for prescription text recognition)
  - Open-source medical image datasets (for training the diagnostic model)

## Implementation & Code Quality
- **Efficient AI Models:** Uses pre-trained deep learning models fine-tuned for medical image classification.
- **Optimized Processing:** Uses image preprocessing techniques (grayscale conversion, adaptive thresholding) to enhance OCR accuracy.
- **Scalable API:** Built with Flask, supporting multiple requests with minimal latency.

## Testing & Validation
- **Automated Tests:**
  - `test_ocr()`: Verifies OCR accuracy on mock prescription images.
  - `test_diagnosis()`: Ensures AI model predicts diseases correctly from sample medical images.
- **Performance Metrics:** Evaluated on **real-world medical datasets**.

## Impact & Feasibility
- Reduces **medication errors** caused by illegible prescriptions.
- Speeds up **disease diagnosis**, assisting overburdened healthcare workers.
- Easily **deployable in hospitals & pharmacies** as an API or mobile application.

## Future Enhancements
- Expanding **AI model support** for multiple disease categories.
- Integrating **multilingual OCR** for diverse prescription formats.
- Enhancing **security & privacy** for patient data protection.

## Installation & Setup
1. **Clone the Repository:**
   ```bash
   git clone <repository_link>
   cd AI-Medical-Assistant
   ```
2. **Create a Virtual Environment & Install Dependencies:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. **Download and Configure Tesseract OCR:**
   - Install Tesseract OCR and ensure it is accessible via the system path.

## How to Run
1. **Start the Flask API:**
   ```bash
   python app.py
   ```
2. **Using the API Endpoints:**
   - Upload a prescription image:
     ```
     POST /analyze_prescription
     ```
     Send an image file as `multipart/form-data`
   - Upload a medical scan for diagnosis:
     ```
     POST /diagnose
     ```
     Send an image file as `multipart/form-data`
3. **Test the System:**
   ```bash
   python -c 'from app import test_ocr, test_diagnosis; test_ocr(); test_diagnosis()'
   ```

## References & Appendices
- **Sample Prescription Images Dataset** (mock data used for OCR training)
- **Open-source Medical Imaging Datasets** (e.g., NIH Chest X-ray dataset, Kaggle healthcare datasets)
- **System Architecture Diagram** *(Attach a clear diagram illustrating system components & workflow)*



