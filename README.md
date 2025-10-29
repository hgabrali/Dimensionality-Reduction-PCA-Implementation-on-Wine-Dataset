
# Dimensionality Reduction: PCA Implementation on Wine Dataset 🍷


* A Masterschool Unsupervised Learning Mini-Project

## 🔬 Project Overview

This repository documents a foundational exercise in **Dimensionality Reduction** using **Principal Component Analysis (PCA)**. The objective is to distill a complex, high-dimensional chemical dataset into a minimal set of components to facilitate visualization and rigorously analyze information preservation.

The project utilizes the **Wine Dataset** from the `sklearn.datasets` module, which comprises **178 samples** characterized by **13 distinct chemical features** (e.g., alcohol, malic acid, ash).

---

## 🎯 Key Goals

* **Dimensionality Reduction:** Successfully project the 13-dimensional feature space down to **2 principal components (PCs)**.
* **Visualization Efficacy:** Demonstrate the effectiveness of PCA by visualizing cluster separation using only the first two PCs.
* **Variance Interpretation:** Quantify the information loss/retention by evaluating the **Explained Variance Ratio**.

---

## 🛠️ Technical Workflow

### Task 1: Data Ingestion and Preparation

* **Loading:** Import the Wine dataset using `sklearn.datasets.load_wine`. Features are stored in $\text{X}$ and cultivar classes (target) in $\text{y}$.
* **Standardization:** Apply **`StandardScaler`** to $\text{X}$. This preprocessing step is mandatory to ensure all features contribute **equitably** to the PCA transformation, preventing high-magnitude features from dominating the variance calculation.

### Task 2: PCA Application and Transformation

This step involves initializing the PCA model and projecting the standardized data onto the new, lower-dimensional space.

* **Reduction:** Reduce the dataset to **2 principal components** (`n_components=2`).
* **Transformation:** Transform the scaled data into the new, lower-dimensional space, storing the result in **`X_pca`**.

**👉 Action:** Insert a new Code Cell below to initialize PCA and perform the transformation.

### Task 3: Visualization and Interpretation

* **Visual Confirmation:** Generate a scatter plot of **PC1 vs. PC2**. Points are colored based on their actual wine class ($\text{y}$) to visually assess how well the intrinsic cluster structure is preserved in 2D.
* **Variance Evaluation:** Print the **cumulative explained variance ratio** captured by the first 2 PCs. This metric directly quantifies the percentage of the dataset's total information retained after the reduction.

---

### ➕ Bonus Challenge (Advanced Evaluation)

* **Extended Reduction:** Re-run the PCA with **`n_components=5`**.
* **Comparative Analysis:** Calculate the new cumulative explained variance ratio. The analysis compares the trade-off: **how much additional information is captured by the 5 PCs compared to the efficiency of using only 2 PCs?**
