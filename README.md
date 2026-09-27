# Sports Person Classifier

An image classification web app that identifies five sports celebrities from uploaded photos. It uses classical computer vision for face and feature extraction paired with a trained classifier served over a Flask API.

## Preview

<p align="center">
  <img src="UI/Screenshot.png">
</p>

## Tech Stack

- Python
- Flask
- OpenCV
- Scikit-learn
- PyWavelets
- NumPy
- JavaScript / HTML / CSS

## How It Works

- The frontend sends the uploaded image as a Base64 string to the Flask `/classify_image` endpoint.
- OpenCV detects faces and eyes using Haar cascade classifiers to crop and isolate the face region.
- Each cropped face is resized and processed with a 2D Discrete Wavelet Transform (PyWavelets) to extract frequency/texture features, which are stacked with raw pixel data into a single feature vector.
- A scikit-learn pipeline (StandardScaler and Logistic Regression) evaluates the feature vector and returns the predicted athlete along with class probability scores.

## Run It

Clone the repository and install dependencies:

```bash
git clone https://github.com/arsalan-99/Sports_Person_Classifier_Model.git
cd Sports_Person_Classifier_Model

python -m venv .venv
source .venv/bin/activate

pip install -r requirements.txt
```

Start the Flask backend:

```bash
cd server
python server.py
```

Open `UI/app.html` directly in your browser, or serve the UI:

```bash
python -m http.server 8000 --directory UI
```
