# Support Vector Machines on Non-Linearly Separable Data

This repository contains a hands-on machine learning project that explores how linear and non-linear Support Vector Machines (SVMs) perform on custom 2D data that is **not linearly separable**. The notebook demonstrates the full pipeline from dataset generation to model evaluation, decision boundary visualization, and margin analysis using both 2D and 3D plots.

---

## Files

- `hw5.ipynb`: Main Jupyter Notebook with data generation, model training (linear and non-linear SVMs), decision surface visualizations, performance evaluation, and interpretability analyses.
- `plots/`: Folder created for saving 2D/3D visualizations of decision boundaries and support vectors. *(optional, can be added manually)*

---

## Dataset

- **Type**: Custom generated 2D dataset using NumPy.
- **Classes**: Binary classification (Class 0 and Class 1).
- **Properties**: 
  - Not linearly separable in ℝ².
  - Easily separable in higher-dimensional space via kernel methods.
- **Generation**: Two circular clusters (inner/outer ring) were generated using radius-based logic.

---

## What’s Inside?

### Q1: Data Generation and Visualization
- A 2D toy dataset is generated that is **not linearly separable**.
- Scatter plot shows the two classes and highlights their circular spatial pattern.

### Q2: Linear SVM
- Linear SVM is trained on the toy dataset.
- Support vectors and decision boundary are visualized.
- Misclassified samples are identified and highlighted.
- Margin size and the decision equation \( \vec{w} \cdot \vec{x} + b = 0 \) are shown.
- Failure analysis included to explain why linear SVM struggles.

### Q3: Non-Linear SVM with RBF Kernel
- Radial Basis Function (RBF) kernel is selected to map data to a higher-dimensional space.
- 3D surface plot shows the non-linear decision surface.
- Mathematical mapping via feature transform \( \phi(x_1, x_2) = (x_1, x_2, x_1^2 + x_2^2) \) is demonstrated.

### Q4: 2D Decision Boundary of Non-Linear SVM
- 2D contour plot of RBF SVM decision regions.
- Support vectors and classification results are clearly annotated.
- Mathematical decision function and margins are also included as LaTeX-rendered text on the plot.

---

## How to Run

1. Clone the repository and open `hw5.ipynb` in Jupyter Notebook or JupyterLab.
2. Run each cell in order to generate the dataset, train the models, and visualize the results.

---

## Requirements

Install the required Python libraries with:

```bash
pip install numpy matplotlib scikit-learn seaborn
