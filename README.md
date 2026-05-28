# Norm of a matrix
## Aim
To write a program to find the 1-norm, 2-norm and infinity norm of the matrix and display the result in two decimal places.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
	1. Get the input matrix using np.array()   
    2. Find the 2-norm of the matrix using np.linalg.norm()
	3. Print the norm of the matrix in two decimal places.
## Program:
```
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

A = eval(input())

cols = len(A[0])
max_sum = 0

for j in range(cols):
    s = 0
    for i in range(len(A)):
        s += abs(A[i][j])
    if s > max_sum:
        max_sum = s

print("{:.2f}".format(max_sum))





# 2-Norm of a Matrix

'''
Program to find 2-norm of a matrix.
Developed by: G.Sushanth
RegisterNumber: 212225230088
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

A = eval(input())

m = len(A)
n = len(A[0])

B = [[0 for j in range(n)] for i in range(n)]

for i in range(n):
    for j in range(n):
        s = 0
        for k in range(m):
            s += A[k][i] * A[k][j]
        B[i][j] = s

trace = B[0][0] + B[1][1]
det = B[0][0] * B[1][1] - B[0][1] * B[1][0]

eigen = ((trace + (trace**2 - 4*det) ** 0.5) / 2) ** 0.5

print("{:.2f}".format(eigen))



# Infinity Norm of a Matrix





```
## Output:
### 1-Norm of a Matrix
<br>
<br>
<br>

### 2-Norm of a Matrix
<br>
<br>
<br>

### Infinity Norm of a Matrix
<br>
<br>
<br>

## Result
Thus the program for 1-norm, 2-norm and Infinity norm of a matrix are written and verified.
