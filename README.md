# 🤖 Unsupervised Machine Learning

> Hands-on exploration of clustering algorithms and dimensionality reduction using Python & scikit-learn.

---

## 📖 About This Project

This notebook was built as part of a machine learning course assignment covering **Chapter 6: Unsupervised Learning**. It walks through the core ideas of clustering and dimensionality reduction from theory to working, visualised code — all runnable in Google Colab with zero setup.

---

## 🗂️ Notebook Contents

| Part | Topic | Methods Used |
|------|-------|-------------|
| Part 1 | Conceptual Questions | Written answers |
| Part 2 | Hierarchical Clustering | `AgglomerativeClustering`, Dendrogram (Ward linkage) |
| Part 3 | K-Means Challenge | `KMeans`, Elbow Method, Silhouette Score |
| Part 4 | Alternative Clustering | `DBSCAN` (density-based) |
| Part 5 | Dimensionality Reduction | `PCA` — 5 features → 2 components |

---

## 📊 Key Concepts Covered

**Unsupervised Learning** — Finding hidden patterns in unlabelled data without any predefined output to guide the model.

**Clustering Analysis** — Grouping data points so that items within the same cluster are more similar to each other than to those in other clusters.

**Hierarchical Clustering** — Builds a tree of clusters (dendrogram) by iteratively merging the closest groups. No need to specify K upfront — the tree tells you.

**K-Means** — Partitions data into K groups by minimising within-cluster variance. Fast and intuitive, but requires choosing K in advance and assumes spherical clusters.

**DBSCAN** — Groups points based on density. Naturally identifies noise/outliers and can find clusters of arbitrary shape — no need to specify the number of clusters.

**PCA (Principal Component Analysis)** — Reduces high-dimensional data to fewer axes (principal components) that capture the most variance, enabling visualisation and faster modelling.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3+-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-1.24+-013243?style=flat&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-11557c?style=flat)
![SciPy](https://img.shields.io/badge/SciPy-1.11+-8CAAE6?style=flat&logo=scipy&logoColor=white)
![Colab](https://img.shields.io/badge/Google%20Colab-Ready-F9AB00?style=flat&logo=googlecolab&logoColor=white)

```
scikit-learn    →  KMeans, DBSCAN, AgglomerativeClustering, PCA, make_blobs
scipy           →  linkage, dendrogram (hierarchical clustering)
matplotlib      →  all visualisations
numpy           →  data generation & numerical ops
```

---

## 🚀 How to Run

### Option 1 — Google Colab (Recommended)

1. Click the badge below or go to [colab.research.google.com](https://colab.research.google.com)
2. Select **File → Upload notebook**
3. Upload `Chapter6_Unsupervised_ML.ipynb`
4. Click **Runtime → Run all**

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com)

### Option 2 — Local (Jupyter)

```bash
# Clone the repo
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

# Install dependencies
pip install scikit-learn scipy matplotlib numpy

# Launch Jupyter
jupyter notebook Chapter6_Unsupervised_ML.ipynb
```

---

## 📸 Visualisations

The notebook produces the following plots:

- 🌲 **Dendrogram** — Ward linkage tree with optimal cut-line at k=4
- 🔵 **Hierarchical Clusters** — 4-colour scatter of agglomerative results
- 📈 **Elbow + Silhouette plots** — Objective metric comparison for K=2 through 8
- 🔢 **K-Means at K=2, 4, 7** — Side-by-side showing under/over-clustering
- 🌀 **DBSCAN vs K-Means** — Direct visual comparison with noise points marked
- 📐 **PCA Before vs After** — Raw feature pairs vs reduced 2D projection
- 📊 **Explained Variance Bar** — Cumulative variance captured per component

---

## 💡 Key Findings

- The dataset contains **4 natural clusters**, confirmed by both the dendrogram gap and the silhouette peak at K=4.
- **DBSCAN** identified the same clusters without being told K, and correctly flagged borderline points as noise instead of forcing them into a group.
- **PCA** retained ~90% of total variance in just 2 components, making the cluster structure immediately visible in a 2D scatter plot.
- For unknown data with no labels, **PCA is the best first step** — it reveals whether structure exists before committing to any clustering strategy.

---

## 📁 File Structure

```
📦 Chapter-6-Unsupervised-ML/
 ┣ 📓 Chapter6_Unsupervised_ML.ipynb   ← Main notebook (all code + answers)
 ┗ 📄 README.md                        ← This file
```

---

## 📚 References & Resources

- [scikit-learn Clustering Guide](https://scikit-learn.org/stable/modules/clustering.html)
- [scikit-learn PCA Documentation](https://scikit-learn.org/stable/modules/decomposition.html#pca)
- [SciPy Hierarchical Clustering](https://docs.scipy.org/doc/scipy/reference/cluster.hierarchy.html)
- [Towards Data Science — K-Means Explained](https://towardsdatascience.com/k-means-clustering-algorithm-applications-evaluation-methods-and-drawbacks-aa03e644b48a)

---

*Part of my machine learning coursework — building in public 🚀*
