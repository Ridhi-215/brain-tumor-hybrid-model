# Brain Tumor Classification using Hybrid Deep Learning Model

## Overview

This project presents a hybrid deep learning framework for automated brain tumor classification from MRI images. The proposed model combines EfficientNet-B0 and MobileNetV3 for feature extraction, enhanced with ROI-based preprocessing, CBAM attention mechanism, and Firefly optimization for improved performance.

The model is designed to classify brain tumors into three categories:

* Glioma
* Meningioma
* Pituitary

---

## Models Implemented

The project includes the following models:

* EfficientNet-B0 (Baseline)
* MobileNetV3 (Lightweight Model)
* Hybrid Model (EfficientNet + MobileNet)
* Hybrid + ROI (Region of Interest Enhancement)
* Hybrid + ROI + CBAM (Attention Mechanism)
* Hybrid + ROI + CBAM + Firefly Optimization (**Final Model**)

---

## Dataset

* Figshare Brain Tumor MRI Dataset
* Total Images: 3064

  * Glioma: 1426
  * Meningioma: 708
  * Pituitary: 930

**Note:**
The same pipeline can be applied to other datasets (e.g., BT dataset) without modifying the architecture.

---

## Methodology

The proposed pipeline consists of the following steps:

1. Preprocessing

   * Image resizing (224×224)
   * Normalization
   * Data augmentation

2. ROI Enhancement

   * Focus on tumor-relevant regions

3. Hybrid Feature Extraction

   * EfficientNet-B0 (deep features)
   * MobileNetV3 (lightweight features)

4. Feature Fusion

   * Concatenation of both feature sets

5. Attention Mechanism

   * CBAM (Channel + Spatial Attention)

6. Optimization

   * Firefly Algorithm for hyperparameter tuning

7. Classification

   * Dense layers with softmax output

---

## Results

| Model                         | Accuracy   |
| ----------------------------- | ---------- |
| EfficientNet-B0               | ~95%       |
| MobileNetV3                   | ~93%       |
| Hybrid Model                  | ~96.9%     |
| Hybrid + ROI                  | ~96.4%     |
| Hybrid + CBAM                 | ~95.6%     |
| Hybrid + ROI + CBAM + Firefly | **~96.9%** |

---

## Visual Results

### Training Performance

* Accuracy and Loss Curves

### Confusion Matrix

* Shows class-wise prediction performance

### Grad-CAM Visualization

* Highlights important regions used by the model for prediction

---

## Project Structure

```text
brain-tumor-hybrid-model/
│
├── models/
│   ├── efficientnet_model.ipynb
│   ├── mobilenet_model.ipynb
│   ├── hybrid_model.ipynb
│   ├── hybrid_roi_model.ipynb
│   ├── hybrid_roi_cbam_firefly_model.ipynb
│
├── results/
│   ├── graphs/
│   ├── confusion_matrix/
│   ├── gradcam/
│
│
├── requirements.txt
├── README.md
```

---

## Installation

Install required libraries:

```bash
pip install -r requirements.txt
```

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/brain-tumor-hybrid-model.git
```

2. Navigate to the project folder:

```bash
cd brain-tumor-hybrid-model
```

3. Open Jupyter Notebook and run any model:

```bash
jupyter notebook
```

4. Execute cells sequentially.

---

## Key Features

* Transfer Learning
* Hybrid Feature Fusion
* Attention Mechanism (CBAM)
* ROI-based Enhancement
* Firefly Optimization
* Grad-CAM Explainability

---

## Future Work

* Evaluation on additional datasets (BT dataset)
* Integration of segmentation models (Attention U-Net)
* Real-time clinical deployment

---

## Authors

* Sindhuja Arnepalli
* Guntur Ridhi
* Indu Kukatikonda
* Roda Chinthapalli

**Faculty Mentor:**
Srinivas Arukonda  
Department of Computer Science and Engineering  
SRM University AP, India

---

## License

This project is for academic and research purposes.
