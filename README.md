# Numpy & Pandas

## 🔍 Library Overview

Before we dive in, here's a quick intro to the two core libraries we’ll use:

###  NumPy
- **The fundamental package for numerical computing in Python.**
- **Key features:**
  - **Arrays:** Homogeneous, N-dimensional arrays (faster and more memory-efficient than Python lists)  
  - **Vectorized ops:** Element-wise arithmetic without explicit loops  
  - **Linear algebra & random:** Built-in support for matrix operations and pseudo-random number generation  

###  Pandas
- **A powerful data analysis and manipulation library built on top of NumPy.**  
- **Key features:**
  - **DataFrame:** 2D tabular data structure with labeled axes (rows & columns)  
  - **IO tools:** Read/write CSV, Excel, SQL, JSON, and more  
  - **Series:** 1D labeled array, great for time series and single-column tables  
  - **Grouping & aggregation:** Split-apply-combine workflows for summarizing data  



### 1. What  
> **What you will learn in this section.**  
> By the end of this notebook, you will be able to:  
> - Create and manipulate NumPy arrays of different shapes and dtypes  
> - Perform element-wise arithmetic and universal functions
> - Index, slice, and reshape arrays for efficient computation  

---

### 2. Why  
> **Why this topic matters.**  
> NumPy arrays are the foundation of nearly all scientific computing in Python.  
> They provide:  
> - **Speed:** Vectorized operations run much faster than Python loops  
> - **Memory efficiency:** Compact storage of homogeneous data  
> - **Interoperability:** A common data structure for libraries like Pandas, SciPy, and scikit-learn  

---

### 3. How  
> **How to do it.**  
> Follow these step-by-step examples:

```python
import numpy as np

# 1) Create arrays
a = np.array([1, 2, 3, 4])
b = np.arange(0, 10, 2)          # [0, 2, 4, 6, 8]
c = np.zeros((2, 3), dtype=int)  # 2×3 array of zeros

# 2) Element-wise arithmetic
sum_ab = a + b[:4]               # adds element by element
prod_ab = a * b[:4]              # multiplies element by element

# 3) Universal functions
sqrt_b = np.sqrt(b)              # square root of each element
exp_a  = np.exp(a)               # eᵃ for each element

# 4) Indexing & slicing
row = b[2:5]                     # slice subarray
c[0, :] = row                    # assign a row

# 5) Reshape & combine
d = np.linspace(0, 1, 6).reshape(2, 3)
stacked = np.vstack([c, d])      # vertical stack of two 2×3 arrays


```

