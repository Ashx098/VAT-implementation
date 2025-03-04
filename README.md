# VAT Algorithm Implementation 🚀

## 📌 Overview
This repository contains an implementation of the **Visual Assessment of Cluster Tendency (VAT) Algorithm**, along with **comparisons against K-Means and DBSCAN clustering methods**. We applied VAT to **real and synthetic datasets**, evaluated its effectiveness, and validated our findings using **Hopkins Statistic, PCA, and t-SNE**.

---

## 📂 **Project Structure**

---

## 📊 **Datasets Used**
We tested VAT on both **real-world and synthetic datasets**:

| **Dataset** | **Description** |
|------------|----------------|
| **Iris** | Flower dataset (3 species) |
| **Mall Customers** | Customer segmentation (income, spending score) |
| **Spotify (500x500)** | Music track features (danceability, energy, valence, tempo) |
| **Blobs** | Synthetic dataset with clear clusters |
| **Moons** | Two crescent-shaped overlapping clusters |
| **Circles** | Concentric circular clusters |
| **Gaussian Mixture (GMM)** | Overlapping probabilistic clusters |

---

## ⚡ **Implementation Details**
### 🔹 **1. VAT Algorithm**
- Implements **Prim’s-based MST reordering** to visualize cluster tendency.
- Generates **VAT images** to detect potential cluster structures.

### 🔹 **2. Hopkins Statistic**
- Evaluates **if the dataset has natural clustering tendencies**.

### 🔹 **3. K-Means Clustering**
- Uses **Elbow Method** to determine the **optimal number of clusters (K)**.
- Compares **K-Means cluster assignments vs. VAT observations**.

### 🔹 **4. DBSCAN Clustering**
- Applied to **Moons & Circles**, where K-Means fails.
- **Detects arbitrarily shaped clusters** using density-based clustering.

### 🔹 **5. PCA & t-SNE Analysis**
- Used to **verify VAT’s findings** when clusters were unclear.
- Applied to **Spotify dataset** to check if clusters exist.

---

## 📈 **Results & Findings**
| **Dataset** | **VAT Observations** | **Best Clustering Method** |
|------------|----------------------|----------------------|
| **Iris** | Strong cluster structure | ✅ K-Means (K=3) |
| **Mall Customers** | Cluster tendency detected | ✅ K-Means (K=5) |
| **Spotify** | No clear clusters | ❌ No strong clustering |
| **Blobs** | Clear, well-separated clusters | ✅ K-Means (K=3) |
| **Moons** | Two groups detected | ✅ DBSCAN |
| **Circles** | K-Means fails | ✅ DBSCAN |
| **GMM** | Overlapping clusters | ✅ K-Means (K=3) |


