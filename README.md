# Principal Component Analysis and Clustering

**Author:** Mohmad Yaqoob  
**Roll No:** DA25M017  
**Course:** Foundations of Machine Learning (M.Tech DSAI, IIT Madras)

---

## Overview

This project explores **dimensionality reduction** and **clustering** techniques on a synthetic dataset with complex structures (including nonlinear spirals). The focus is on understanding how **PCA**, **Kernel PCA**, and **clustering algorithms** behave under linear and nonlinear data scenarios.

The report includes:

- Implementation of **PCA from scratch**  
- Exploration of **Kernel PCA** with **polynomial** and **RBF (Gaussian) kernels**  
- Experiments with **K-means clustering** for different cluster counts  
- Application of **spectral clustering** using Kernel-PCA embeddings  
- Comparative analysis of clustering methods and embeddings  

---

## Key Highlights

### 1. PCA (Principal Component Analysis)

- **Objective:** Reduce dataset dimensionality while retaining maximum variance  
- **Findings:**  
  - The first principal component explained ~65% of total variance  
  - PCA captures **linear patterns** efficiently but struggles with nonlinear structures  

### 2. Kernel PCA (KPCA)

- **Objective:** Extend PCA to capture **nonlinear patterns** by mapping data into a higher-dimensional space using kernels  
- **Kernels Explored:**  
  - Polynomial kernel (degrees 2–5)  
  - RBF (Gaussian) kernel with various σ values  
- **Best Results:** RBF kernel with σ=2 provided smooth separation of nonlinear spirals without distorting the intrinsic geometry  

### 3. Clustering

- **K-means:**  
  - Applied with K = 2, 3, 4, 5  
  - Works well for roughly spherical clusters but limited for nonlinear shapes  
- **Spectral Clustering:**  
  - Applied on Kernel-PCA embeddings  
  - RBF kernel with σ=2 produced the most interpretable and distinct clusters  
  - Alternative eigenvector-based assignments highlighted the importance of **full spectral embeddings**  

---

## Visualizations

The report includes detailed figures for:

- PCA directions and variance explained  
- Kernel PCA embeddings (polynomial vs RBF)  
- K-means clusters and Voronoi diagrams  
- Spectral clustering results with varying kernel parameters  

These visualizations help **understand the geometric and statistical structure** of the dataset.

---

## Key Insights

- **Linear PCA** captures global variance but cannot separate nonlinear patterns  
- **Kernel PCA** with a suitable kernel (RBF, σ=2) uncovers intrinsic nonlinear structures  
- **K-means** is sensitive to initialization and cluster number; struggles with non-spherical clusters  
- **Spectral clustering** on KPCA embeddings effectively identifies nonlinear clusters  
- Using **full top-k eigenvector embeddings** is crucial for meaningful clustering  

---

## How to Run

1. Open the Jupyter Notebook or Python scripts included in the project  
2. Load the dataset (synthetic spiral dataset provided)  
3. Run the PCA, Kernel PCA, and clustering steps sequentially  
4. Observe visualizations and analyze cluster separations  

---

## Tools and Libraries

- **Python 3.x**  
- **NumPy** for numerical computations  
- **Matplotlib / Seaborn** for plotting  
- **Scikit-learn** (optional for comparison with built-in PCA/KPCA and clustering)  

---

## Conclusion

This project demonstrates the power of **dimensionality reduction** and **spectral clustering** in revealing hidden structures in complex datasets. Proper choice of kernel and parameters is critical for nonlinear data, and full embeddings are essential for robust and interpretable clustering.

