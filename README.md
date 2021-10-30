# Assignment 2: CMPE-255 Dimensionality Reduction
__Name__: Shivam Tomar  
__Student Id__: 015218203  
__Email__:shivam.tomar@sjsu.edu


### Asignment
This assignment showcase following Dimensionality Reduction algorithms using scikit library:
1. PCA
2. SVD
3. LLE
4. ISOMAP
5. t-SNE
6. UMAP

### Datasets
Following data sets are used

1. **Tabular Dataset**: __MPG__ dataset from sns. It contains mpg and other data for various car brands.
2. **Image Dataset**: It is the digits images dataset loaded from _scikit.datasets_.

### Comparison of Algorithms

These Algorithms can be divided into 2 groups based on the type of data they are suitable for.

**Group 1).** PCA and SVD: Suitable for Lienar data.  
**Group 2).** LLE, ISOMAP, t-SNE and UMAP: Suitable for Manifold data.  

1. PCA: PCA is a popular dimensionality reduction technique with the dense data and works well on Linear data. Using PCA for dimensionality reduction involves zeroing out one or more of the smallest principle components. Resulting in the lower dimension projection of the data that preserves the maximum data variance.
2. SVD: SVD also works on the Linear data. It works very well with the sparse data. SVD uses matrix factorization for dimensionality reduction. SVD is way to find Eigen vectors or to do Matrix factorization.
Important points of SVD and PCA:
The new components created by SVD/PCA are less interpretable.
The may lead to information loss.
They requires data to be Normalized/Standardized before applying >the algorithm.
They work only on numeric data.
3. LLE: LLE creates an embedding of the dataset and attempt to preserves relationship between the neighbourhoods in the dataset. LLE works very well on Manifold data. LLE uses variery of tangent linear patches to model the manifold. LLE can be thought of as applying the PCA on each of these neighborhood locally, producing an linear hyperplane and then comparing the results globally to find the best non linear embedding. LLE doesn't perform well on the very large dimension of data.
4. ISOMAP: ISOMAP creates embedding of the dataset and attempts to preserve relationship in the dataset. ISOMAP converts data to lower dimension in a way that maintains geodesic distances(optimized distance along the discovered manifold). Unlike LLE ISOMAP performs very well on very large dimensions of data.
5. t-SNE: TSNE stands for t-distributed Stochastic Neighbor Embeddings. The algorithm converts relationships in the original space into t-distributions or normal distributions with small sample sizes and relatively unknown standard deviation. This makes t-SNE very sesitive to the local structure.
6. UMAP: UMAP is similar to t-SNE but with probably higher processing speed. It can be applied to sparse matrices thus no need to apply PCA or SVD as preprocessing step.
