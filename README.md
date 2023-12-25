# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. get the size of the system(n)
2. initialize matrices for the augmented system and the solution
3. perform gaussian elimination to convert the matrix to upper triangle form
4. perform backsubstitution
 

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: MARXIN LIJO M
RegisterNumber: 23013468
*/
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-1,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ")

```

## Output:

![Screenshot 2023-12-25 113942](https://github.com/MARXINLIJO/Gaussian/assets/145742540/382c4bb1-f986-411e-9a5f-72490811f321)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

