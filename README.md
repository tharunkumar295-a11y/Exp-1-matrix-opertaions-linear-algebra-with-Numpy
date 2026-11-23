# Experiment-1-Matrix-opertaions-linear-algebra-with-Numpy

## Aim

Introduce matrix operations used in ML: transpose, inverse, solve linear systems, eigen decomposition. 

## Algorithm

Direct use of numpy.linalg routines; relate to linear regression normal equations.

## DETAILED EXPLANATION:

1. import numpy as np — load NumPy for arrays and linear algebra. 
2. A = np.array(...) — define a 2×2 matrix A. 
3. b = np.array(...) — define vector b for solving A x = b. 
4. print("Matrix A:", A) — show matrix for reference. 
5. A.T — compute transpose (rows ↔ columns). 
6. np.linalg.inv(A) — compute inverse of A (exists only if A is invertible). 
7. np.linalg.eig(A) — compute eigenvalues and eigenvectors; eigenvalues help 
understand variance directions (PCA). 
8. np.linalg.solve(A,b) — numerically solve linear system more stably than 
inv(A).dot(b). 

## Program & Output

import numpy as np 

A = np.array([[2.0, 1.0],[1.0, 3.0]]) 

b = np.array([1.0, 2.0]) 

print("Matrix A:\n", A) 

print("\nTranspose A^T:\n", A.T) 

print("\nInverse A^-1:\n", np.linalg.inv(A)) 

eigvals, eigvecs = np.linalg.eig(A) 

print("\nEigenvalues:", np.round(eigvals,4)) 

x = np.linalg.solve(A,b) 

print("\nSolve A x = b --> x:", np.round(x,4))

<img width="581" height="342" alt="image" src="https://github.com/user-attachments/assets/f3e50aa4-4f6a-4709-ada5-ed6877ba0234" />

## Result

Students see concrete matrix computations and how to solve linear systems; relate solve() to normal equations in linear regression.

# THEORY

Linear algebra (matrix inversion, eigen-decomposition) underpins PCA, linear models, and many optimization problems. Conditioning/invertibility matters. 

