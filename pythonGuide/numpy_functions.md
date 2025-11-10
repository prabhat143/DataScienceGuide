Sure! Below is a **clear, structured list of important NumPy functions with short, practical examples**.
This will help you understand *how* they are used, not just what they are.

---

# ✅ **1. Array Creation — With Examples**

### **`np.array()`**

```python
import numpy as np
a = np.array([1, 2, 3])
```

### **`np.zeros()`**

```python
np.zeros((2, 3))
# [[0. 0. 0.]
#  [0. 0. 0.]]
```

### **`np.ones()`**

```python
np.ones(4)
# [1. 1. 1. 1.]
```

### **`np.full()`**

```python
np.full((2,2), 7)
# [[7 7]
#  [7 7]]
```

### **`np.arange()`**

```python
np.arange(0, 10, 2)
# [0 2 4 6 8]
```

### **`np.linspace()`**

```python
np.linspace(0, 1, 5)
# [0.  0.25 0.5 0.75 1. ]
```

### **`np.eye()`**

```python
np.eye(3)
# Identity matrix
```

---

# ✅ **2. Array Manipulation — With Examples**

### **`reshape()`**

```python
np.array([1,2,3,4,5,6]).reshape(2, 3)
```

### **`ravel()` (flatten)**

```python
np.ravel([[1,2],[3,4]])
# [1 2 3 4]
```

### **`concatenate()`**

```python
np.concatenate([[1,2], [3,4]])
# [1 2 3 4]
```

### **`vstack()` / `hstack()`**

```python
np.vstack([[1,2], [3,4]])
```

### **`transpose()`**

```python
np.transpose([[1,2,3],[4,5,6]])
```

---

# ✅ **3. Mathematical Operations**

### Elementwise operations

```python
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

np.add(a, b)      # [5 7 9]
np.subtract(a, b) # [-3 -3 -3]
np.multiply(a, b) # [4 10 18]
```

### **Exponentials & logs**

```python
np.exp(1)      # e^1
np.log(10)     # natural log
```

### **Trigonometry**

```python
np.sin(np.pi/2)   # 1.0
```

---

# ✅ **4. Statistical Functions**

### **`sum()`**

```python
np.sum([1,2,3])  # 6
```

### **`mean()`**

```python
np.mean([1,2,3,4]) # 2.5
```

### **`std()` & `var()`**

```python
np.std([1,2,3])  # standard deviation
```

### **`argmax()` / `argmin()`**

```python
np.argmax([1,5,3]) # 1
```

---

# ✅ **5. Logical & Comparison**

### **`where()`**

```python
arr = np.array([1, 5, 10])
np.where(arr > 5, "big", "small")
# ['small', 'small', 'big']
```

### **`np.any()` / `np.all()`**

```python
np.any(arr > 8)   # True
np.all(arr > 0)   # True
```

---

# ✅ **6. Sorting and Searching**

### **`sort()`**

```python
np.sort([3,1,2])
# [1 2 3]
```

### **`unique()`**

```python
np.unique([1,2,2,3,3])
# [1 2 3]
```

With counts:

```python
vals, counts = np.unique([1,2,2,3,3], return_counts=True)
# vals = [1 2 3]
# counts = [1 1 2]
```

---

# ✅ **7. Random Module**

### **Random integers**

```python
np.random.randint(1, 10, size=5)
```

### **Random float matrix**

```python
np.random.rand(2, 3)
```

### **Random choice**

```python
np.random.choice([10,20,30])
```

---

# ✅ **8. Linear Algebra**

### **Dot product**

```python
a = np.array([1,2])
b = np.array([3,4])
np.dot(a, b)    # 11
```

### **Matrix multiplication**

```python
A = np.array([[1,2],[3,4]])
B = np.array([[5,6],[7,8]])
np.matmul(A, B)
```

### **Inverse**

```python
np.linalg.inv([[1,2],[3,4]])
```

### **Eigenvalues**

```python
np.linalg.eig([[1,2],[2,1]])
```

---

# ✅ **9. File I/O**

### Save & load `.npy`

```python
np.save("data.npy", arr)
arr2 = np.load("data.npy")
```

### Save & load text

```python
np.savetxt("data.txt", arr)
arr2 = np.loadtxt("data.txt")
```

---
