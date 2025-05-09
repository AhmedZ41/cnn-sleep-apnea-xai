# 🧠 Sleep Apnea Detection with Explainable CNN (XAI)

This project explores the use of a convolutional neural network (CNN) for detecting obstructive sleep apnea (OSA) events from biosignals, with a strong focus on **explainability** using  post-hoc methods like **Grad-CAM** and **SHAP**.

> **Project**: Explainable Neural Networks in the Medical Domain  
> **Institution**: HTWG Konstanz – Ubiquitous Computing Lab  
> **Semester**: Summer Semester 2025  
> **Team Members**: Ahmed Adnan, João Pedro Cunha, Julian Ambrozy, Niklas Kaiser, Wiebke Prinz

---

## 🩺 Project Goal

To implement and evaluate a deep learning pipeline that classifies apnea events from biosignal windows and applies explainability techniques to interpret the model’s predictions in a clinical context.

---

## 📊 Datasets

We use publicly available, medically validated datasets:

- **SHHS2** – Sleep Heart Health Study (Phase 2)  
- **MESA** – Multi-Ethnic Study of Atherosclerosis

➡️ Downloadable from: [sleepdata.org](https://sleepdata.org)

**Biosignals used**:
- SpO₂ (Oxygen Saturation)
- HR (Heart Rate)
- Thoracic & Abdominal Respiratory Effort

Signals are preprocessed, downsampled to **1 Hz**, and segmented into **60-second windows**.

---

## 🧱 Model Architecture

We implement a CNN architecture inspired by:
- *de Souza et al. (2023), Frontiers in Neuroscience*  
- Structured for time-series biosignal classification

**Output:** Binary classification per window  
**Post-processing:** Apnea-Hypopnea Index (AHI) estimation

---

## 🔍 Explainability Methods

Two post-hoc explainability techniques are integrated:

### 🔸 Grad-CAM (Gradient-weighted Class Activation Mapping)
- Adapted for 1D convolutional outputs
- Visualizes signal regions contributing most to each prediction

### 🔸 SHAP (SHapley Additive Explanations)
- Quantifies per-signal and per-feature contributions
- Generates both local and global interpretability outputs

---

## 🛠️ Project Structure

```bash
sleep-apnea-cnn-xai/