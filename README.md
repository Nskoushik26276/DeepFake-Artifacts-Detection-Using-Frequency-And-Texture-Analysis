# DeepFake-Artifacts-Detection-Using-Frequency-And-Texture-Analysis
This project presents a lightweight yet powerful deepfake image detection method that combines Discrete Wavelet Transform (DWT) and Local Binary Patterns (LBP) to identify image manipulation artifacts. Instead of relying on complex deep models, this approach focuses on forensic features such as texture inconsistencies and frequency-domain anomalies created during face manipulation and mask blending.

🔍 Key Idea

Deepfakes often leave subtle traces at blending boundaries and frequency patterns that are difficult to see but detectable through signal-processing techniques. By fusing:

DWT (Haar Wavelet) → captures high-frequency anomalies and edge inconsistencies

LBP → captures micro-texture distortions caused during face synthesis

Grayscale Channel → preserves the global visual structure

…the project creates a 3-channel forensic feature tensor that acts as input to a custom CNN classifier. This significantly boosts generalization and detection accuracy.

📊 Model Performance
Feature Used	Accuracy	Confidence
LBP only	74.94%	81.64%
DWT only	76.21%	83.93%
⭐ DWT + LBP Fusion	91.78%	100%

📌 Result: The combined feature model greatly outperforms individual feature models, proving that texture + frequency fusion is more discriminative for deepfake detection.

🧠 What This Project Demonstrates

✔️ Robust detection without large/complex deep networks
✔️ Signal-processing based forensic representation
✔️ Improved generalization through complementary feature fusion
✔️ A practical approach for lightweight deepfake screening systems

🛠️ Tools & Libraries Used
Component	Tool
Feature Extraction	PyWavelets, scikit-image, OpenCV
Model Training	TensorFlow/Keras
Data Handling	NumPy, Pandas
Visualization	Matplotlib
