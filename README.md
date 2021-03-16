
# Matrix computation and operation in C
## Features
 1. This is a simple implementation of matrix computation and opearation.  
 2. can choose numeric data type (ex. double or float.).  
 3. It almost does NOT rely on the other libraries, it's light.  


## How to use  
 you need to define data type of variables in matrix.  
def_ElementType_mat corresponeds to data type, 

* if you want to use double, use below definition on headder file.  
```
#define def_ElementType_mat double
```

* If you want to create 12 x 24 matrix, 
```
int row = 12;
int col = 24;
_stMatrix* matrix;
matrix = fMat_New(row, col);
```

* How to access each elements is, 
```
int row_access = 3;
int col_access = 4;
def_ElementType_mat element_value;
_stMatrix* matrix = fMat_New(row, col);

element_value = fMat(matrix, row_access, col_access)
```

* How to set constant values on elements in matrix is,
```
fMat_UnitMatrix(matrix);
fMat_SetConst(matrix, 3);
fMat_Zero(matrix);
fMat_UnitMatrix(matrix);
```

* How to multiply A matrix with B matrix is (C = AB),
```
int d1 = 3;
int d2 = 5;
int d3 = 6;

_stMatrix* A = fMat_New(d1, d2);
_stMatrix* B = fMat_New(d2, d3);
_stMatrix* C1 = fMat_New(d1, d3);
_stMatrix* C2 = NULL;

fMat_Mlt(C1, A, B);
C2 = fMat_Mlt2(A, B);
```

* How to get inverse matrix is,
```
_stMatrix* A = fMat_New(3, 3);
_stMatrix* A_inv = fMat_InverseMatrix_Gauss2(A);
```

* How to release memories on matrix is,
```
fMat_Delete(matrix);
```





## Functions and explanations.

### Functions
|Function name|Explanations|Arguments|
|:---|:---|:---|
||||
||||
||||
||||
