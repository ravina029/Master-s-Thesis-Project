# 🎓 Master's Thesis  
## Stability and Accuracy of Permutation-Invariant Embedding Schemes

---

## 📌 Overview

This thesis investigates the **theoretical foundations of permutation-invariant representations**, which are essential for modeling unordered data such as sets, point clouds, and graphs.

The work focuses on designing embedding schemes that are both:
- **Expressive (injective)**  
- **Stable (bi-Lipschitz continuous)**  

while maintaining **low computational complexity**.

---

## 🎯 Problem Statement

Key challenges in permutation-invariant learning:

- Designing embeddings that preserve **all input information (injectivity)**  
- Ensuring **robustness to perturbations (stability)**  
- Reducing **embedding dimensionality** for practical deployment  

---

## 💡 Core Contributions

### 1. ❌ Fundamental Limitation of Sum-Based Embeddings
- Proved that **power-sum (DeepSets-style) embeddings are not bi-Lipschitz**  
- Extended result:  
  - Any embedding based on **smooth or piecewise smooth aggregation fails stability**

👉 **Implication:** Widely used architectures have inherent stability limitations

---

### 2. 📉 General Impossibility Result
- Proved that:
  > Any permutation-invariant function differentiable at structured points is **not bi-Lipschitz**

👉 Establishes a **broad theoretical limitation**, not restricted to specific models

---

### 3. ✅ Sorting-Based Embeddings (Positive Result)
- Analyzed embeddings of the form:
  \[
  \beta_A(X) = \downarrow (AX)
  \]

- Showed:
  - These embeddings are **bi-Lipschitz**
  - Stability depends on **singular values of transformation matrix A**

---

### 4. 🚀 Improved Injectivity Bound
Reduced required embedding dimension:

| Work | Required Dimension |
|------|------------------|
| Balan et al. | \(1 + (d-1)n!\) |
| Dym & Gortler | \(2nd + 1\) |
| **This Work** | **\(D > n(d - 1)\)** |

👉 Enables **more practical and scalable representations**

---

### 5. 📊 Lipschitz Bounds
Derived tighter stability bounds:

- Upper bound: \(M = \sigma_1(A)\)  
- Lower bound: \(\sigma_{d,k}(A) \le m \le \sigma_d(A)\)

👉 Connects **linear algebra properties** to **model stability**

---

## 🧪 Experimental Findings

### Stability
- Improves with embedding dimension (**D**)  
- Saturates with increasing sample size (**n**)  
- Stable even beyond theoretical guarantees  

---

### Accuracy
- Achieves near-perfect performance for moderate **D**  
- Sensitive to embedding dimension (**d**)  
- Shows **stability–accuracy mismatch**

---

### Key Observations
- **D is the dominant factor** controlling stability and accuracy  
- **Data efficiency:** strong performance with small datasets  
- **Parameter sensitivity:** instability with respect to *d*  
- Possible **overfitting or dataset simplicity** at high accuracy levels  

---

## 🔍 Key Insights

- ❌ Sum-based aggregation → **inherently unstable**  
- ✅ Sorting-based embeddings → **stable and theoretically grounded**  
- ⚠️ Gap between **theoretical guarantees and empirical performance**  
- 📈 Structural parameter **D** governs behavior  

---

## ⚠️ Limitations

- Lack of statistical validation (no variance analysis)  
- Sensitivity to embedding dimension  
- Evaluation limited to synthetic data  

---

## 🔮 Future Directions

- Improve robustness across embedding configurations  
- Analyze theory–practice discrepancy  
- Extend to:
  - Graph neural networks  
  - Real-world datasets  
- Applications in:
  - Trustworthy AI  
  - Robust representation learning  

---

## 🔗 Research Output

- Contributed theoretical results to:  
  *Neural Injective Functions for Multisets, Measures and Graphs via a Finite Witness Theorem*  

🔗 https://doi.org/10.48550/arXiv.2306.06529  

---

## 🧠 Research Relevance

- Trustworthy AI  
- Robust Machine Learning  
- Set & Graph Representation Learning  
- Geometric Deep Learning  

---

## 🎯 Takeaway

This work informs my research direction toward:

> Designing **stable, interpretable, and reliable representation learning methods** for real-world AI systems.
