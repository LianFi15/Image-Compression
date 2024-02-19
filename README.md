
# Image Compression

This project implements image processing techniques using Singular Value Decomposition (SVD) and matrix approximation. It includes functions for extracting color channels, performing SVD, and approximating images with varying levels of precision (k-values). The main script applies these functions to a sample image, saving and analyzing the results.


## Why Use Image Compression?

Image compression using matrix approximation, such as Singular Value Decomposition (SVD), reduces storage space and transmission bandwidth. By approximating the image matrix with a lower-rank version, we retain essential visual information while significantly lowering the storage complexity from O(mn) to O(k(m+n)) where k is best rank-k approximation.
This compression is crucial for efficient storage, transmission, and processing of images.
## Singular Value Decomposition (SVD)

SVD is a factorization of a matrix into three other matrices, offering insights into the inherent structure of the original matrix.

### Formula:

For an $m \times n$ matrix $A$, SVD is represented as:

$A = U \Sigma V^T $

Where:
- $U$ is an $m \times m$ orthogonal matrix (left singular vectors),
- $\Sigma$ is an $m \times n$ diagonal matrix with singular values on the diagonal,
- $V^T$ is an $n \times n$ orthogonal matrix (right singular vectors).

Singular values ($\sigma$) in $\Sigma$ are non-negative and arranged in descending order.

### Decomposition:

1. **Matrix $U$:**
   - Columns represent orthonormal eigenvectors of $AA^T$.

2. **Diagonal Matrix $\Sigma$:**
   - Diagonal elements are singular values ($\sigma$).

3. **Matrix $V^T$:**
   - Columns represent orthonormal eigenvectors of $A^TA$.

### Application:

- SVD is widely used in various applications, such as image compression, noise reduction, and data analysis.

**Example Usage:**
```python
import numpy as np

# Perform SVD on a matrix A
U, \Sigma, V^T = np.linalg.svd(A)

```
## Low rank Matrix Approximation

The best rank-k approximation to a matrix $A$ with $rank(A) \ge k$ , is given by :

$$A_k= \left(\sum_{i=1}^k \sigma u_i v_i^T \right)$$

We'll explore the optimal k value in this project.

## Example

I used a photo of my dog, the result are as you can see below