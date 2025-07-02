# Behavioural-segmentation


## 📌 Objective

The aim of this project was to develop a real-time system for facial recognition and drowsiness detection to monitor attentiveness of staff using standard webcam input.

---

## 🧠 What the System Does

- Identifies individuals using LBPH face recognition
- Detects eye landmarks to determine drowsiness via Eye Aspect Ratio (EAR)
- Tracks gaze direction and attention patterns
- Alerts when the user shows signs of drowsiness or looks away repeatedly
- Logs accuracy statistics across test image sets

---

## 🛠 Technologies Used

- **Language**: Python
- **Libraries**: OpenCV, dlib, NumPy, PIL (Pillow), threading
- **Models**: 
  - Haar Cascades for face and eye detection
  - dlib's 68-point facial landmark model
  - LBPH (Local Binary Pattern Histogram) for face recognition

---

## 📂 Project Structure

- `train_image.py`: Extracts faces and IDs from training data and trains the LBPH model.
- `testing.py`: Tests the recognition model against test images and computes accuracy.
- `detect_drowsiness.py`: Monitors EAR and gaze to detect sleepiness.
- `recognize.py`: Runs real-time face recognition and overlays user identity.
- `gazedetection.py`: Detects if the user is looking away from the screen.
- `capture_image.py`: Captures training images for new users.
- `generateTestData.py`: Generates sample test image data.
- `combined.py`: Integrates all features in one pipeline.

---

## 🧪 Model Training

- Images were preprocessed in grayscale and labeled with unique IDs.
- Trained model saved as `Trainner.yml`.
- Accuracy: ~88% on test dataset of 150+ hours of surveillance data.

---

## 🚨 Drowsiness Detection

- EAR threshold used: dynamic, tuned experimentally.
- Alert triggered if eyes remain closed for continuous frames.
- Gaze direction checked using pupil center vs eye bounding box.

---

## 📈 Results

- Recognized identity with ~88% accuracy in test conditions.
- Detected over 35+ instances of drowsiness across 150 hours.
- Enabled staff monitoring in real-time without manual supervision.

---

## 🧾 Credits

Developed as a research assignment at DRDO for internal personnel monitoring at secure entry points. Combines classical computer vision with modern attention tracking logic.
