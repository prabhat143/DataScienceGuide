Swapping values in NumPy can be done in several useful ways depending on what you want to swap:

✅ Swap **two elements**
✅ Swap **rows**
✅ Swap **columns**
✅ Swap **axes**
✅ Swap **array values using boolean conditions**

Below are all the common methods **with examples**.

---

# ✅ 1. Swap Two Elements

### **Swap values using simultaneous assignment**

```python
import numpy as np

arr = np.array([10, 20, 30, 40])
arr[1], arr[3] = arr[3], arr[1]

print(arr)
```

**Output:**

```
[10 40 30 20]
```

---

# ✅ 2. Swap Rows in a 2D Array

### **Swap row 0 and row 2**

```python
arr = np.array([
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
])

arr[[0, 2]] = arr[[2, 0]]

print(arr)
```

**Output:**

```
[[7 8 9]
 [4 5 6]
 [1 2 3]]
```

---

# ✅ 3. Swap Columns in a 2D Array

### **Swap column 0 and column 1**

```python
arr[:, [0, 1]] = arr[:, [1, 0]]

print(arr)
```

---

# ✅ 4. Swap All Instances of Two Values

### Example: swap all `1` with `3`

```python
arr = np.array([1, 3, 1, 3, 2])
arr = np.where(arr == 1, -999, arr)  # temp
arr = np.where(arr == 3, 1, arr)
arr = np.where(arr == -999, 3, arr)

print(arr)
```

Better method using a temporary copy:

```python
arr = np.array([1,3,1,3,2])
tmp = arr.copy()

arr[arr == 1] = 3
arr[arr == 3] = 1
```

---

# ✅ 5. Swap Using Boolean Masks

Example: swap all values > 5 with values < 3
(This is rare but useful.)

```python
arr = np.array([1,2,6,7])

mask1 = arr > 5
mask2 = arr < 3

arr[mask1], arr[mask2] = arr[mask2], arr[mask1]

print(arr)
```

---

# ✅ 6. Swap Axes (Dimensions)

You can swap dimensions of an array:

### **Using `np.swapaxes()`**

```python
arr = np.array([[1,2,3],[4,5,6]])

np.swapaxes(arr, 0, 1)
```

### Using `arr.T` (Transpose)

```python
arr.T
```

---

# ✅ 7. Swap Adjacent Elements

Example: swap every pair of elements:

```python
arr = np.array([10,20,30,40])
arr = arr.reshape(-1, 2)[:, ::-1].flatten()

print(arr)
```

Output:

```
[20 10 40 30]
```

---

# ✅ 8. Swap Blocks / Slices

Example: swap the left half and right half:

```python
arr = np.array([1,2,3,4,5,6])
n = len(arr)

arr = np.concatenate((arr[n//2:], arr[:n//2]))

print(arr)
```

