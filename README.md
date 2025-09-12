# Manuscript Illumination Classification with Deep Learning

## Overview
This repository contains an experimental deep learning project that applies **computational tools** to the analysis of medieval manuscript illuminations.  
The project uses a **custom dataset of ~100 images** from a richly decorated manuscript, featuring trees, birds, and other ornamental motifs.

The goal is to train a model that can recognize visual similarities between new manuscript images and the training set, demonstrating the potential of AI in art historical research.

---

## Dataset
- **Size**: ~100 images  
- **Content**: Illumination details (trees, birds, decorative patterns)  
- **Split**: 
  - 90% for training  
  - 10% for testing  

Note: Large-scale public datasets of medieval manuscripts are not readily available.  
- A related dataset exists on Kaggle (*Class_Images_Meieval*), but it contains images closer to the **14th–15th centuries** and does not fully represent earlier manuscripts.

---

## Model
- **Base model**: [VGG16](https://arxiv.org/abs/1409.1556)  
- **Approach**: Transfer learning (fine-tuning on custom dataset)  
- **Task**: Classify whether a new image is **similar** (≥50% similarity to learned patterns) or **not similar**.  

### Results
- **Training**: 90 images  
- **Testing**: 10 images  
- **Accuracy**: ~78%  

While the dataset is small, the result provides a solid baseline and shows the potential of combining computational methods with manuscript studies.

---

## How it Works
1. Dataset prepared from manuscript illuminations  
2. Images split into training (90%) and testing (10%) sets  
3. Pre-trained VGG16 model loaded  
4. Model fine-tuned on custom dataset  
5. Predictions: Given a new image, the model checks for similarity with training patterns  

---

## Requirements
- Python 3.x  
- TensorFlow / Keras  
- NumPy  
- Matplotlib  
- scikit-learn  

Install dependencies:
```bash
pip install -r requirements.txt
