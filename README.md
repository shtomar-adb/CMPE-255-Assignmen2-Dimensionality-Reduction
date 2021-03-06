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

### Analysis of Data distribution after applying various Dimensionality Reduction algorithms.

1. **PCA**
- **Tabular Data**: After plotting the data between first two dimensions after dimensionality reduction we will find that data is Linearly distributed.
- **Image Data**: The image data is not Linearly distributed. It has uniform distribution.  

2. **SVD**
- **Tabular Data**: Unlike PCA the distribution of data after dimensionality reduction is non linear. It is uniform. Although first two component of reduced data contains about the similar data variance which is about 90%.
- **Image Data**: Image data distribution of SVD and PCA is very similar and is uniformly distributed in both cases.

3. **LLE**
- **Tabular Data**: The data is distributed in the form of dense patches of neighbors.
- **Image Data**: The data is distributed as patches of neighbor but most of them are clustered at center.

4. **ISOMAP**
- **Tabular Data**: The data is distributed as patches of close neighbors and the data with patches is distributed uniformally instead of being clustered like LLE.
- **Image Data**: Image data distribution is similar to LLE, but more uniformly distributed then LLE.

5. **t-SNE**
- **Tabular Data**: The data is distributed in the form of patches of neighboring points. The patches are better isolated then ISOMAP and are more balanced in terms of data points in them.
- **Image Data**: The data distribution is in the form of patches of neighboring points where patches are very well distributed and are not overlapping each other and patches are not centered at same location. 

6. **UMAP**
- **Tabular Data**: The data distribution looks very similar to the t-SNE where patches are well separated from each other.
- **Image Data**: Data distribution looks very similar to t-SNE where patches of neighboring points are well ditributed and not overlapping each other. The patches are not centered at same location.
