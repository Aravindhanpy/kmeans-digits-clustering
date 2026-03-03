# K-Means Clustering on Digits Dataset

##  Project Overview
This project applies **K-Means clustering** to the sklearn Digits dataset to group handwritten digit images (0–9) without using labels during training.

The goal is to evaluate how well unsupervised learning can identify digit patterns.

---

##  Dataset
- Source: `sklearn.datasets.load_digits()`
- Samples: 1797 images
- Features: 64 (8×8 pixel images flattened)
- Classes: 10 digits (0–9)

---

##  Methodology

1. Data scaling using `StandardScaler`
2. K-Means clustering (k=10)
3. Multiple initializations (`n_init=10`)
4. Mapping clusters to true labels using majority voting
5. Evaluation using:
   - Inertia
   - Silhouette Score
   - Accuracy (after label mapping)
6. PCA for 2D visualization

---

##  Results

- Clustering Accuracy: ~70%
- Silhouette Score: ~0.15–0.20 (varies slightly per run)

Even without supervision, K-Means is able to group similar handwritten digits with reasonable performance.

---

##  Visualization

Cluster centers (digit prototypes)
PCA Visualization

---
##  Key Learnings

- Initialization impacts clustering stability.
- K-Means struggles with overlapping classes (e.g., 3 vs 8).
- Dimensionality reduction helps interpret high-dimensional clustering.

---

## 🚀 How to Run

1. Clone the repository:
