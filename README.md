# Dimensionality Reduction for Classification – FashionMNIST

**Course:** IE4476 – Image Processing and Computer Vision  
**Student:** Jui Bhooshan Gupte   

## 📌 Overview
This project explores **Principal Component Analysis (PCA)** and **Linear Discriminant Analysis (LDA)** for dimensionality reduction on the **Fashion-MNIST dataset**. Both unsupervised (PCA) and supervised (LDA) techniques are applied, followed by classification using the **Mahalanobis distance classifier**. The goal is to reduce data complexity while maintaining classification accuracy.

## 📂 Contents
- Introduction to Dimensionality Reduction, PCA, and LDA
- Dataset details and preprocessing steps
- Methodology for PCA and LDA
- Performance analysis before and after dimensionality reduction
- Observations, conclusions, and future improvements

## 🛠️ Experimental Setup
- **Dataset:** Fashion-MNIST (70,000 grayscale images, 28×28 pixels, 10 clothing categories)
- **Preprocessing:** Normalization (0–1), flattening images to 784 features
- **Techniques:** PCA for unsupervised feature extraction, LDA for supervised classification
- **Classifier:** Mahalanobis distance

## 📊 Key Results
| Method                  | Accuracy  | Avg Prediction Time | Observations |
|------------------------|-----------|---------------------|--------------|
| Before PCA              | 99.9%     | 0.1315s              | High accuracy but slower |
| After PCA (~100 PCs)    | 99.9%     | 0.0059s              | 22× faster, same accuracy |
| LDA (multi-class)       | 81.51%    | Fast                 | High for distinct classes, overlaps cause drop |

- **PCA** retained ~90% variance with only ~100 principal components.
- **LDA** maximized class separability but struggled with visually similar categories.

## 📈 Visualizations
- **Scree plot** of explained variance by principal components.
- **PCA scatter plot** showing class clustering.
- **Confusion matrices** for PCA and LDA.

## 💡 Conclusion
- PCA significantly reduces computation time while preserving accuracy.
- LDA provides good separation for distinct classes but needs improvements for overlapping features.
- Combining PCA and LDA could further optimize classification.

## 📚 References
1. Telgaonkar, A. H., & Deshmukh, S. (2015). *Dimensionality Reduction and Classification through PCA and LDA*. IJCA, 122(17).  
2. Reddy, G. T., et al. *Analysis of Dimensionality Reduction Techniques on Big Data*. IEEE.

---

### 🖥️ How to Run
1. Install required packages:
   ```bash
   pip install numpy matplotlib scikit-learn tensorflow seaborn
