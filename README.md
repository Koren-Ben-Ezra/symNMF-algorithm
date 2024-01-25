## Academic Course Project
As part of an academic course, I embarked on the implementation of a clustering algorithm known as Symmetric Non-negative Matrix Factorization (symNMF). symNMF offers a robust solution for clustering tasks, addressing real-world challenges in data analysis and interpretation.

## Practical Applications of symNMF Algorithm
The symNMF algorithm offers practical solutions beyond traditional clustering methods like K-means. For instance, in the healthcare industry, symNMF can be employed to analyze patient data for disease clustering. By operating on symmetric non-negative matrices, symNMF accurately identifies clusters of patients exhibiting similar symptoms or disease progression, aiding in personalized treatment plans and medical research. Its flexibility extends to financial data analysis, where symNMF can uncover patterns in market trends for investment portfolio optimization, enhancing decision-making processes for financial institutions.

## How to Use the Project
To utilize the symNMF project effectively, users can leverage its intuitive Python interface (symnmf.py) for seamless integration into their data analysis pipelines. By specifying parameters such as the number of clusters, users can customize symNMF to their specific clustering objectives. Whether analyzing similarity matrices, computing degree matrices, or deriving normalized similarity matrices, symNMF offers a user-friendly platform for advanced clustering tasks. Furthermore, users can compare the clustering performance of symNMF against industry-standard algorithms like K-means, gaining deeper insights and making informed decisions based on their data analysis outcomes.



## How to Use the Project
To use symNMF module for your clustering tasks, follow these simple steps:

#### 1. Downloading the Project
Clone or download the symNMF project repository from GitHub to your local machine.
#### 2. Setting Up the Environment
Ensure you have Python installed on your system, along with necessary libraries such as NumPy and SciPy.
#### 4. Integration into Your Project
Import the symnmf.py module into your Python project to access the symNMF functionalities.
#### 5. Specifying Parameters
Customize the symNMF algorithm by specifying parameters such as the number of clusters (k) and the desired goal (goal). The available goals include:
* symnmf: Perform the full symNMF clustering algorithm and output the resulting matrix H.
* sym: Calculate and output the similarity matrix A.
* ddg: Calculate and output the Diagonal Degree Matrix D.
* norm: Calculate and output the normalized similarity matrix W.
#### 6. Calling Functions
Call the relevant functions from symnmf.py based on your specific clustering objectives. For example:
* To perform symNMF clustering: symnmf(k, 'symnmf', file_name)
* To calculate the similarity matrix: symnmf(k, 'sym', file_name)
* To compute the Diagonal Degree Matrix: symnmf(k, 'ddg', file_name)
* To derive the normalized similarity matrix: symnmf(k, 'norm', file_name)
#### 7. Analyzing Results
Analyze the output matrices generated by symNMF to gain insights into your dataset's underlying structures. Compare the clustering performance against industry-standard algorithms like K-means using metrics such as silhouette score.
By following these steps, you can seamlessly integrate the symNMF project into your data analysis pipeline and unlock the full potential of clustering in your applications.



### Appendix: Special Mathematical Matrices
#### 1. Similarity Matrix (A)
The similarity matrix, denoted as A, is a square matrix used to quantify the similarity between data points in a dataset. Each element a<sub>ij</sub> represents the similarity between data points i and j, typically computed using a similarity measure such as the Euclidean distance or cosine similarity.

#### 2. Diagonal Degree Matrix (D)
The diagonal degree matrix, denoted as D, is a diagonal matrix where each diagonal element d<sub>ii</sub> represents the degree of vertex i in a graph. In the context of symNMF, the degree of a vertex corresponds to the sum of similarities between the vertex and all other vertices in the dataset.

#### 3. Normalized Similarity Matrix (W)
The normalized similarity matrix, denoted as W, is a matrix obtained by normalizing the similarity matrix A. In symNMF, the normalized similarity matrix is computed as W = D<sup>-1/2</sup>AD<sup>-1/2</sup>, where D<sup>-1/2</sup> is the inverse square root of the diagonal degree matrix D.

#### 4. Graph Laplacian (W)
The graph Laplacian, also denoted as W, is a matrix representation of a graph's Laplacian operator. In the context of symNMF, the graph Laplacian matrix is used to capture the graph structure encoded in the normalized similarity matrix W.

#### 5. Decomposition Matrix (H)
The decomposition matrix, denoted as H, is a non-negative matrix that results from the symNMF algorithm. H is of size n×k, where n is the number of data points and k is the number of clusters. Each row of H represents the association scores of a data point with each cluster.
