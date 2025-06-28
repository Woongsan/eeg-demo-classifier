# 🧠 EEG Signal Classification Demo (Simulated SSVEP)

This project demonstrates a minimal and interpretable EEG signal classification pipeline using synthetic SSVEP-like signals. The goal is to showcase an end-to-end BCI signal decoding workflow suitable for resource-constrained wearable devices.

👉 [Open in Colab ▶️](https://colab.research.google.com/github/Woongsan/eeg-demo-classifier/blob/main/demo.ipynb)

![Repo size](https://img.shields.io/github/repo-size/Woongsan/eeg-demo-classifier)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 💡 Motivation

In BCI (Brain-Computer Interface), real-time classification of SSVEP signals (like 8Hz vs. 12Hz) is essential. This demo simulates EEG signals and classifies them using a simple MLP classifier based on FFT band power.

---

## 🧱 Pipeline Overview

1. **Signal Simulation**  
   - Generate noisy EEG-like signals at 8Hz / 12Hz (256Hz sampling)

2. **Feature Extraction**  
   - FFT → Extract band power (6–14 Hz)

3. **Classification**  
   - Use lightweight MLP (PyTorch)  
   - Achieve ~100% test accuracy

4. **Visualization**  
   - Training loss curve  
   - Band power heatmap  
   - PCA decision boundary

---

## 🧪 Result Highlights

| Metric         | Value       |
|----------------|-------------|
| Test Accuracy  | ✅ 100%     |
| Feature Dim    | 9 (FFT bins)|
| Model          | 2-layer MLP |
| Inference Time | < 1ms       |

---

## 📁 Files

| File              | Description                      |
|-------------------|----------------------------------|
| `demo.ipynb`      | Full pipeline notebook (Colab-ready) |
| `requirements.txt`| Python package dependencies      |

---

## 🔄 Setup

```bash
git clone https://github.com/Woongsan/eeg-demo-classifier.git
cd eeg-demo-classifier
pip install -r requirements.txt
