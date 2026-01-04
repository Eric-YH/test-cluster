# Text Clustering with Sentence Embeddings

Cluster and visualize text documents using **Sentence-BERT embeddings + HDBSCAN + UMAP**.

---

## Workflow

1. **Sentence Embeddings**
   - Model: `sentence-transformers/all-MiniLM-L6-v2` (dim=384)
   - Fast, CPU-friendly, supports English & Chinese (can swap models)
   - Generates dense semantic vectors for each sentence

2. **Clustering**
   - Algorithm: **HDBSCAN** (density-based)
   - Finds clusters of semantically similar texts
   - Handles noise points (`-1` label)

3. **Dimensionality Reduction & Visualization**
   - **UMAP** reduces embeddings to 2D for plotting
   - Visualizes clusters and noise points
   - Helps interpret semantic groupings

---

## Key Points

- Works on small and medium datasets
- Unsupervised: no labels required
- Captures semantic similarity better than keyword matching
- Noise points indicate outliers or unique content
- Tunable hyperparameters:
  - `min_cluster_size` & `min_samples` (HDBSCAN)
  - `n_neighbors` & `min_dist` (UMAP)

---

## Tools

- **sentence-transformers** (MiniLM embeddings)
- **HDBSCAN** (density-based clustering)
- **UMAP** (dimensionality reduction)
- **NumPy / Pandas** (data handling)
- **Matplotlib** (visualization)
