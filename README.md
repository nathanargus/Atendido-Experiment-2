# ECE2112 Programming Problems

This repository contains Python scripts for solving various programming problems in ECE2112. Below is an overview of each script included.

### 1. Normalization Problem 

###### This problem involves normalizing a 5x5 array of random numbers using basic data preprocessing techniques. Specifically, it requires centering the data by subtracting the mean and scaling it by dividing by the standard deviation, following the normalization formula $𝑍 = (𝑋 - mean) / σ$. The goal is to generate a random 5x5 array, compute its mean and standard deviation, apply the normalization process to adjust the data, and then save the resulting normalized array to a file named X_normalized.npy.

**Function:**

```python

import numpy as np

# Generate a random 5x5 ndarray
X = np.random.rand(5, 5)

# Calculate the mean and standard deviation
mean_X = X.mean()
std_X = X.std()

# Print the mean and standard deviation for reference
print("Mean:", mean_X)
print("Standard Deviation:", std_X)

# Normalize X using the formula Z = (X - mean)/ standard deviation
X_normalized = (X - mean_X) / std_X

# Print both the original and normalized array
print("\nOriginal Array:\n", X)
print("\nNormalized Array:\n", X_normalized)

# Save the normalized array to a file
np.save('X_normalized.npy', X_normalized)

```

**Output:**

![image](https://github.com/user-attachments/assets/ee5fa0bf-823c-4401-920c-43d52a9efffc)



 ### 2. Divisible by 3 Problem

###### This problem requires creating a 10x10 NumPy array where each element is the square of the first 100 positive integers. After constructing this array, the task is to identify all the elements that are divisible by 3. Once these elements are found, they need to be saved into a file named div_by_3.npy. The goal is to generate the squared values, apply a condition to filter out those divisible by 3, and store the result in a file for later use.

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

# Print the array and all the elements divisible by 3
print("10x10 Array:\n", A)
print("\nElements Divisible by 3:\n", div_by_3)

# Save the result as div_by_3.npy
np.save('div_by_3.npy', div_by_3)

```

**Output:**

![image](https://github.com/user-attachments/assets/8aeef91f-6b4f-41ac-a30a-79f84babf91a)
