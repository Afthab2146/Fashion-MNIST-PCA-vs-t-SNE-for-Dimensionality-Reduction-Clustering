# Fashion-MNIST-PCA-vs-t-SNE-for-Dimensionality-Reduction-Clustering
This project compares PCA and t-SNE on Fashion-MNIST (unsupervised). It shows how PCA explains variance and reduces dimensions, while t-SNE reveals clear nonlinear clusters. KMeans clustering on t-SNE demonstrates natural groupings of clothing types more effectively than PCA.

##📖 Overview
This project applies **dimensionality reduction** techniques to the [Fashion-MNIST dataset]  
We compare **PCA (Principal Component Analysis)** and **t-SNE (t-Distributed Stochastic Neighbor Embedding)**, and then apply **KMeans clustering** to visualize how well the data groups in lower dimensions.

---

## 🔑 Workflow

1. **Load & Preprocess Data**
   - Use `fashion_mnist` dataset (60k grayscale clothing images, 28x28).
   - Flatten into 784 features per image.
   - Apply `StandardScaler` to normalize values.

2. **PCA (Principal Component Analysis)**
   - Reduce 784 features → 50 dimensions.
   - Plot **explained variance** to see how many components capture most information.
   - Show 2D PCA scatter plot.

3. **t-SNE (t-Distributed Stochastic Neighbor Embedding)**
   - Reduce 784 features → 2D space.
   - Captures **non-linear relationships** between samples.
   - Reveals clear clusters of clothing types.

4. **KMeans Clustering on t-SNE**
   - Run KMeans with 10 clusters (since Fashion-MNIST has 10 classes).
   - Color the t-SNE scatter plot by cluster ID.
   - Observe how clusters naturally form, without labels.

---

## 🤔 Why t-SNE is Better than PCA Here?

- **PCA**:
  - Linear projection.
  - Preserves global variance.
  - Good for compression but struggles to separate overlapping classes.
  - Fashion-MNIST PCA scatter looks like a blur with overlapping classes.

- **t-SNE**:
  - Non-linear projection.
  - Focuses on **local similarities** (neighbors remain neighbors).
  - Captures complex, curved decision boundaries.
  - Produces distinct clusters that match natural clothing categories.

👉 **In short:**  
PCA shows how much variance we can keep,  
t-SNE shows meaningful clusters in 2D.

---

## 📊 Results

- PCA (2D): overlapping blobs, hard to separate classes.  
- t-SNE (2D): clear clusters emerge.  
- KMeans on t-SNE: cluster assignments align well with natural categories.
