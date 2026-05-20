# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Read the input matrix A and, if required, the constant matrix/vector B as floating-point NumPy arrays.

2.Perform LU decomposition/factorization of matrix A to obtain:

3.Permutation matrix P or pivot indices
         Lower triangular matrix L
         Upper triangular matrix U

4.If a system of equations AX=B is given, use the LU factors to solve for the solution matrix/vector X.
Display the matrices L and U, and print the solution X if it is computed. 

## Program:
(i) To find the L and U matrix
```
/*
Program to find the L and U matrix.
Developed by: LAVANYA G
RegisterNumber: 212225230148
*/
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

import numpy as np
from scipy.linalg import lu

A=np.array(eval(input()),dtype=float)
P,L,U=lu(A)

print(L)
print(U)
```
(ii) To find the LU Decomposition of a matrix
```
/*
Program to find the LU Decomposition of a matrix.
Developed by: LAVANYA G
RegisterNumber: 212225230148
*/
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
# To print X matrix (solution to the equations)
import numpy as np
from scipy.linalg import lu_factor,lu_solve

A=np.array(eval(input()),dtype=float)
B=np.array(eval(input()),dtype=float)

lu,piv=lu_factor(A)
X=lu_solve((lu,piv),B)

print(X)

```

## Output:

L and U matrix:

<img width="1272" height="827" alt="Screenshot 2026-05-20 133641" src="https://github.com/user-attachments/assets/9fb9b4a6-08ee-4cb6-914f-2914fce62d6d" />


LU Decomposition:

<img width="1246" height="756" alt="image" src="https://github.com/user-attachments/assets/d8aa62b5-1dbc-4151-8004-26117b34aabd" />



## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

