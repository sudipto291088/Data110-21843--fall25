# Introduction to Google Colab

[Google Colab](https://colab.research.google.com) (short for *Colaboratory*) is a free, cloud-based Jupyter Notebook environment provided by Google. It lets you write and run Python code in your browser with no local installation.

---

## Quick Start Checklist

- Open a new notebook: **File → New notebook**
- Run a cell: **Shift + Enter**
- Add text (Markdown) cell: **+ Text**
- Save to Drive: **File → Save a copy in Drive**
- Switch to GPU (optional): **Runtime → Change runtime type → Hardware accelerator: GPU**

---

## Table of Contents

- [Why Use Google Colab?](#why-use-google-colab)
- [Key Features](#key-features)
  - [Cells](#cells)
  - [Running Code](#running-code)
  - [Hardware Options](#hardware-options)
- [Working with Files](#working-with-files)
- [Python Essentials in Colab](#python-essentials-in-colab)
  - [Basic Python](#basic-python)
  - [NumPy for arrays and math](#numpy-for-arrays-and-math)
  - [Matplotlib for plotting](#matplotlib-for-plotting)
  - [Pandas for data analysis](#pandas-for-data-analysis)
- [Extra Tools](#extra-tools)
- [Keyboard Shortcuts](#keyboard-shortcuts)
- [Best Practices](#best-practices)
- [Common Pitfalls](#common-pitfalls)

---

## Why Use Google Colab?

- **No installation required**: Everything runs in the cloud.  
- **Free GPU/TPU access**: Useful for heavy computation (ML, simulation).  
- **Google Drive integration**: Save and share notebooks like Google Docs.  
- **Reproducibility**: Code, results, and explanations live in one document.  

---

## Key Features

### Cells

- **Code cells**: For writing and running Python code.  
- **Text (Markdown) cells**: For notes, explanations, and formatting. Markdown supports **bold**, lists, and LaTeX math.

Example code cell:
```python
print("Hello, world!")
```

Equation example in Markdown:  
$E = mc^2$

---

### Running Code

- Run current cell: **Shift + Enter**  
- Insert code cell above/below: **Ctrl/Cmd + M, A** or **Ctrl/Cmd + M, B**  
- Restart runtime (clears memory): **Runtime → Restart runtime**

---

### Hardware Options

Switch hardware accelerator:
```
Runtime → Change runtime type → Hardware accelerator: None / GPU / TPU
```

---

## Working with Files

- **Upload a file** from your computer (left sidebar → Files → Upload).  
- **Mount Google Drive** to read/write files stored in Drive:
```python
from google.colab import drive
drive.mount('/content/drive')
```

---

## Python Essentials in Colab

### Basic Python
```python
x = 5
y = 10
print(x + y)
```

### NumPy for arrays and math
```python
import numpy as np
arr = np.array([1, 2, 3])
arr * 2
```

### Matplotlib for plotting
```python
import matplotlib.pyplot as plt

xs = [1, 2, 3, 4]
ys = [10, 20, 25, 30]

plt.plot(xs, ys)
plt.xlabel("x")
plt.ylabel("y")
plt.title("Simple Line Plot")
plt.show()
```

### Pandas for data analysis
```python
import pandas as pd

# Example dataset available in new Colab notebooks:
df = pd.read_csv("sample_data/california_housing_train.csv")
df.head()
```

---

## Extra Tools


- **Install new libraries** as needed:
```python
!pip install seaborn
```

---

## Keyboard Shortcuts

- Convert to **Markdown** cell: `Ctrl/Cmd + M, M`  
- Convert to **Code** cell: `Ctrl/Cmd + M, Y`  
- Run cell: `Shift + Enter`  
- Insert cell **above**: `Ctrl/Cmd + M, A`  
- Insert cell **below**: `Ctrl/Cmd + M, B`  
- Delete cell: `Ctrl/Cmd + M, D` (twice)  
- Undo delete cell: `Ctrl/Cmd + M, Z`  

---

## Best Practices

1. **Work incrementally**: Keep code in small, testable cells.  
2. **Document clearly**: Use Markdown to explain goals, methods, and results.  
3. **Visualize**: Use plots and tables to validate and communicate results.  
4. **Organize data**: Keep project files in predictable folders (e.g., `/content/drive/MyDrive/your-project/`).  
5. **Back up notebooks** to GitHub or Drive regularly.  

---

## Common Pitfalls

- **Runtime resets**: Colab VMs are temporary; files in `/content` disappear after reset. Mount Drive or push to GitHub to persist.  
- **Library versions**: The default environment updates; pin versions when stability matters.  
- **Large uploads**: Prefer Drive or cloud storage links instead of repeated manual uploads.  

---

## More

[Youtube Video: Google Colab Tutorial for Beginners | Get Started with Google Colab](https://www.youtube.com/watch?v=RLYoEyIHL6A)
