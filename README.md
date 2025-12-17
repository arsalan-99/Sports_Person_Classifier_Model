# 🏅 Sports Celebrity Image Classification Model

This project is a computer vision–based Machine Learning application that identifies sports personalities from images using classical computer vision techniques and supervised learning. The system detects faces in an image, extracts meaningful features using wavelet transforms, and classifies the individual using a trained machine learning model.  
The trained model is integrated with a Flask-based backend and a simple web interface for real-time image classification.

---

## 🌐 Web App Preview


---

## 📦 Tools, Libraries & Techniques Used

### 🔧 Libraries
- **NumPy** – Numerical computations  
- **Pandas** – Data handling and preprocessing  
- **OpenCV** – Face and eye detection using Haar cascades  
- **PyWavelets** – Wavelet-based feature extraction  
- **Scikit-learn**
  - Support Vector Machine (SVM)
  - Random Forest Classifier
  - Logistic Regression
  - StandardScaler
  - GridSearchCV
- **Joblib** – Model serialization
- **Flask** – Backend API for model inference  

---

## 🧠 Approach & Methodology

### 🖼️ Image Preprocessing
- Face detection using Haar Cascade classifiers
- Eye detection to validate face regions
- Cropped face images resized to 32×32 pixels
- Conversion to grayscale for wavelet transformation

### 🌊 Feature Extraction
- Applied **Discrete Wavelet Transform (DWT)** to capture texture and edge information
- Combined raw pixel values with wavelet-transformed features
- Final feature vector created by stacking both representations

---

## 🧪 Model Training & Evaluation
- Trained and evaluated multiple ML models:
  - Support Vector Machine (SVM)
  - Random Forest
  - Logistic Regression
- Used **GridSearchCV** for hyperparameter tuning
- Selected **SVM with linear kernel** as the final model based on validation performance

**Final Model Accuracy:** ~ **75%**

---

## 🚀 Web Application
- Users can upload an image via the web interface
- Image is sent to the Flask backend as Base64
- Backend performs face detection, feature extraction, and classification
- Predicted sports personality and class probabilities are returned and displayed

---
