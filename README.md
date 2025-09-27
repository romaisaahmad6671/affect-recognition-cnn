# Affect Recognition with CNNs

This repository contains the implementation and evaluation of two baseline CNNs (**VGG16** and **EfficientNetB0**) for **facial affect recognition**.  
Both **categorical emotion classification** and **dimensional affect regression** (valence and arousal) are explored using transfer learning.


---

## Features

- Multi-task learning: **expression classification** + **valence–arousal regression**  
- **Transfer learning** with ImageNet-pretrained weights  
- Comprehensive metrics:
  - Accuracy, F1-score, Cohen’s Kappa
  - ROC-AUC, PR-AUC
  - RMSE, CORR, SAGR, CCC (for regression)  
- **Performance comparison** of VGG16 vs EfficientNetB0 (accuracy + timing)  
- **Qualitative results**: correct vs incorrect classifications  

---

##  Results

### Quantitative Metrics

| Model           | Accuracy | F1-macro | Kappa  | ROC-AUC | PR-AUC | MSE Valence | MSE Arousal | RMSE Valence | RMSE Arousal | CORR Valence | CORR Arousal | SAGR Valence | SAGR Arousal | CCC Valence | CCC Arousal |
|-----------------|----------|----------|--------|---------|--------|-------------|-------------|--------------|--------------|--------------|--------------|--------------|--------------|-------------|-------------|
| **EfficientNetB0** | 0.2963   | 0.2931   | 0.1957 | 0.7226  | 0.2944 | 0.1961      | 0.1273      | 0.4428       | 0.3568       | 0.3417       | 0.3305       | 0.7113       | 0.7913       | 0.2234      | 0.2278      |
| **VGG16**       | 0.2988   | 0.2952   | 0.1986 | 0.6906  | 0.2592 | 0.2832      | 0.1782      | 0.5322       | 0.4221       | 0.1266       | 0.1555       | 0.6262       | 0.7462       | 0.1176      | 0.1422      |

 **Key Findings:**
- EfficientNetB0 achieved **lower RMSE** and **higher correlation (CORR, CCC)** than VGG16.  
- EfficientNetB0 was also **faster in inference**, making it more suitable for real-time applications.  
- VGG16 achieved slightly higher raw accuracy, but with weaker regression consistency.  


---

## ⚙️ How to Run

1. Clone the repo:
```bash
git clone https://github.com/YOUR-USERNAME/affect-recognition-cnn.git
cd affect-recognition-cnn
