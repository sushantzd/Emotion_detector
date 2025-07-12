# Emotion_detector
A real-time facial emotion detection system using CNN and OpenCV. Trained on grayscale images using Keras with live webcam integration to classify emotions like Happy, Angry, Sad, etc.

# 😃 Real-Time Emotion Detection using CNN & OpenCV

This project is a real-time facial emotion recognition system built using a Convolutional Neural Network (CNN), trained on grayscale facial images, and deployed with OpenCV for webcam-based live emotion detection. It detects and classifies human emotions into **7 categories**:  
`Angry, Disgust, Fear, Happy, Neutral, Sad, Surprise`

---

## 🧠 Model Architecture

The model is a deep CNN with the following structure:
- 4 Convolutional layers with increasing filters (64, 128, 512, 512)
- Batch Normalization, ReLU Activation
- Max Pooling and Dropout for regularization
- 2 Fully connected (Dense) layers
- Final output layer with Softmax (for 7 emotions)

---

## 🗂 Folder Structure

emotion-detector/
│
├── haarcascade_frontalface_default.xml # Face detection XML (OpenCV)
├── model.h5 # Trained Keras CNN model
├── emotion_detector.py # Real-time webcam application
├── train_model.py # CNN model architecture + training
├── requirements.txt # Python dependencies
└── README.md # Project description


---

## 🏋️ Training Details

- **Dataset**: FER-2013 or similar structured emotion dataset
- **Input Shape**: (48, 48, 1) grayscale images
- **Batch Size**: 128
- **Optimizer**: Adam (`lr=0.001`)
- **Loss Function**: Categorical Crossentropy
- **Epochs**: 48
- **Callbacks**: EarlyStopping, ReduceLROnPlateau, ModelCheckpoint

### 🖼️ Training vs Validation Curves
The training script also includes plotting of accuracy and loss:

![Training Curves](#) <!-- Optional: Replace with image if you save plots -->

---

## 🚀 Real-Time Detection (Webcam)

The `emotion_detector.py` script does the following:
- Captures live feed from webcam
- Detects faces using Haar Cascade
- Preprocesses the face (48x48 grayscale)
- Predicts emotion using the trained CNN
- Displays predicted label on screen in real-time

## 🚀 Requirements
tensorflow==2.13.0
keras==2.13.1
numpy==1.23.5
opencv-python==4.8.0.76
matplotlib==3.7.2

### ▶️ Run the app
```bash
python emotion_detector.py

****✨ ###Future Work****

Use MobileNet or EfficientNet for lightweight deployment
Add GUI with Tkinter or Streamlit
Deploy to cloud using Flask or FastAPI


_**

👨‍💻 Author

Sushant Choudhary

GitHub: sushantzd
LinkedIn: linkedin.com/in/sushantzd
Portfolio: linktr.ee/sushantzd
HackerRank: user22001003912
**_
