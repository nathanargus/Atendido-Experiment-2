# ECE2112 Programming Problems

This repository contains Python scripts for solving various programming problems in ECE2112. Below is an overview of each script included.

### 1. Normalization Problem

**Function:**

```python

import numpy as np

# Create a random 5x5 ndarray
X = np.random.rand(5, 5)

# Calculate the mean and standard deviation
mean_X = X.mean()
std_X = X.std()

# Normalize X using the formula Z = (X - mean)/ standard deviation
X_normalized = (X - mean_X) / std_X

# Save the normalized array as X_normalized.npy
np.save('X_normalized.npy', X_normalized)

# Print both the original and normalized arrays
print("Original Array:\n", X)
print("\nNormalized Array:\n", X_normalized)

```

**Output:**
'Original Array:
 [[0.01788081 0.0075502  0.53642402 0.98887735 0.93201881]
 [0.04576152 0.11913864 0.05390981 0.05567566 0.12082548]
 [0.6686522  0.58767294 0.16052042 0.28445319 0.00313501]
 [0.52798297 0.49895919 0.41616869 0.50602564 0.94085923]
 [0.83667781 0.54992898 0.74279367 0.44279465 0.19972011]]

Normalized Array:
 [[-1.23801065 -1.27064539  0.40008438  1.82939928  1.64978131]
 [-1.14993458 -0.91813384 -1.12419386 -1.11861548 -0.91280506]
 [ 0.81779754  0.5619814  -0.78740746 -0.39589978 -1.28459312]
 [ 0.37341882  0.28173175  0.02019383  0.30405488  1.67770848]
 [ 1.34859594  0.44274699  1.05201286  0.1043061  -0.66357434]]'



 ### 2. Divisible by 3 Problem

**Function:**

```python

import numpy as np

# Create an array with the first 100 positive integers
int = np.arange(1, 101)

# Square each each element to create a 10x10 array and reshape to 10x10 ndarray
A = int ** 2
A = A.reshape(10, 10) 

# Determine all elements divisible by 3
div_by_3 = A[A % 3 == 0]

# Save the result as div_by_3.npy
np.save('div_by_3.npy', div_by_3)

# Print the array and all the elements divisible by 3
print("10x10 Array:\n", A)
print("\nElements Divisible by 3:\n", div_by_3)

```

**Output:**
'10x10 Array:
 [[    1     4     9    16    25    36    49    64    81   100]
 [  121   144   169   196   225   256   289   324   361   400]
 [  441   484   529   576   625   676   729   784   841   900]
 [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]
 [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]
 [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]
 [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]
 [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]
 [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]
 [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]]

Elements Divisible by 3:
 [   9   36   81  144  225  324  441  576  729  900 1089 1296 1521 1764
 2025 2304 2601 2916 3249 3600 3969 4356 4761 5184 5625 6084 6561 7056
 7569 8100 8649 9216 9801]'
