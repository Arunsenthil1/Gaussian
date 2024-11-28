# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import nump and sys.
2. Get the values from the user.
3. Find the empty agumented marix and apply gauss elimination
4. Solve the marix to get the answer.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: ARUN S
RegisterNumber: 24900219
*/
```
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
#back substitution
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,x[i]),end=" ")
```


## Output:
![Screenshot 2024-11-28 204247](https://github.com/user-attachments/assets/a3dfab80-1549-4f06-99e3-233c0635ff40)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

