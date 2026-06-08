# Leukemia Gene Expression Analysis Using Heatmaps and Principal Component Analysis (PCA)
This project demonstrates an exploratory genomic analysis of microarray gene expression data from patients with Acute Myeloid Leukemia (AML), Acute Lymphoblastic Leukemia (ALL), and healthy controls. The goal is to investigate patterns of gene expression across samples and determine whether individuals cluster according to diagnosis based on their overall gene expression profiles. 
Data used include: 
- A leukemia microarray gene expression dataset obtained from Kaggle
- Gene expression measurements from AML patients, ALL patients, and healthy controls
## Methods Used (Pipeline Steps)
1. Load and preprocess gene expression data
   - Gene expression data were imported using Pandas and inspected for structure and missing values
2. Identify highly variable genes
   - Variance was calculated for each gene across all samples.
   - The 20 genes with the highest variance were selected because highly variable genes are more likely to capture biological differences between patient groups. 
3. Visualize gene expression patterns
   - A heatmap was created to visualize expression levels of the 20 highest-variance genes across all patients.
4. Standardize gene expression data
   - Gene expression values were standardized using StandardScaler so that each gene contributed equally to downstream analyses.
5. Perform Principal Component Analysis (PCA)
    - PCA was used to reduce the dimensionality of the dataset while preserving as much variation as possible.
    - The first two principal components were extracted and visualized. 
6. Visualize sample clustering
    - A scatterplot of the first two principal components was generated, with samples colored according to diagnosis.
## Interpretation of Results 
The heatmap provides an exploratory view of expression patterns among the 20 most variable genes. While variation in gene expression is evident across patients, clear disease-specific expression patterns are not immediately apparent from the visualization alone. 
The PCA analysis reduces thousands of gene expression measurements into two principal components that capture the largest sources of variation in the dataset. Samples from different diagnostic groups show substantial overlap in the PCA plot rather than forming distinct clusters. This suggests that differences between leukemia subtypes and healthy controls are not strongly captured by the first two principal components alone. 
## Future Directions
- Perform differential gene expression analysis to identify genes significantly associated with each leukemia subtype.
- Apply nonlinear dimensionality reduction techniques such as t-SNE or UMAP to explore more complex relationships in the data.
- Develop machine learning models for leukemia subtype classification using gene expression profiles.
- Conduct pathway and gene set enrichment analyses to investigate underlying biological mechanisms.
## Skills Demonstrated 
- Python (Pandas, NumpPy, Seaborn, Matplotlib, Scikit-learn)
- Genomic data preprocessing and exploratory analysis
- Principal Component Analysis (PCA)
- Biological data dimensionality reduction 
