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

import os
os.environ["OPENBLAS_NUM_THREADS"]="1"
A = eval(input())

max_sum = 0

for i in range(len(A)):
    s = 0
    for j in range(len(A[0])):
        s += abs(A[i][j])

    if s > max_sum:
        max_sum = s

print("{:.2f}".format(max_sum))



```
## Output:
<img width="1169" height="241" alt="Screenshot 2026-05-28 181737" src="https://github.com/user-attachments/assets/6af1bbe8-3e83-4a0a-b425-a0e41d3ca84e" />

### 2-Norm of a Matrix
<img width="823" height="330" alt="Screenshot 2026-05-28 181748" src="https://github.com/user-attachments/assets/9e2d9164-473f-4123-a872-3bafcfb6c29f" />


### Infinity Norm of a Matrix
<img width="848" height="303" alt="Screenshot 2026-05-28 181757" src="https://github.com/user-attachments/assets/db3b72ad-639b-4e87-b944-114be3d0cd09" />


## Result
Thus the program for 1-norm, 2-norm and Infinity norm of a matrix are written and verified.
