# 📊 Data Visualization with Matplotlib

This project demonstrates how to create and customize high-quality graphs using **Matplotlib**, a powerful Python library for data visualization. It covers line plots, scatter plots, bar charts, pie charts, histograms, and more, along with styling, labels, legends, and saving plots.

---

## 🔹 Pyplot

`pyplot` is a submodule of Matplotlib that provides MATLAB-like functions for plotting graphs. Key points:

- Plot points with `plt.plot()` or `plt.scatter()`.
- Display the graph with `plt.show()`.
- Works seamlessly with Python lists or NumPy arrays.

Example:

```python
import matplotlib.pyplot as plt
import numpy as np

# Simple line plot
A = [7, 84, 53, 44, 69]
plt.plot(A)
plt.show()

# Plotting two variables
X = [2,5,7,11]
Y = [13,22,37,30]
plt.plot(X,Y)
plt.show()
```



🔹 Scatter Plots

Used to plot random points without connecting lines:
```Python
X = np.array([1,3,4,5,7])
Y = np.array([4,1,9,7,2])
plt.scatter(X,Y)
plt.show()
```
🔹 Line Graphs

Plot mathematical functions and relationships:
```Python
m, b = 10, 5
X = np.array([1,8,20,45])
Y = m*X + b
plt.plot(X,Y)
plt.show()
```
🔹 Customizing Graphs

You can enhance plots using:

Colors: color='green'

Markers: marker='o'

Line styles: '--', '-.', ':'

Line width: linewidth=2.5

Labels: plt.xlabel(), plt.ylabel()

Title: plt.title()

Legends: plt.legend()

Axis limits: plt.axis([xmin, xmax, ymin, ymax])

Grid: plt.grid(True)

Text: plt.text(x, y, "label")

Subplots: plt.subplot()

🔹 Multiple Functions in One Plot
```Python
t = np.arange(0., 5., 0.2)
plt.plot(t, t, 'r--', t, t**2, 'bs', t, t**3, 'g^')
plt.show()
```
🔹 Scatter Plot with Colors and Sizes
```Python
N = 50
x = np.random.rand(N)
y = np.random.rand(N)
colors = np.random.rand(N)
area = np.pi * (15 * np.random.rand(N))**2
plt.scatter(x, y, s=area, c=colors, alpha=0.5)
plt.show()
```

🔹 Pie Charts
```Python
labels = ['Asia', 'Africa', 'Europe', 'America']
sizes = [59.7, 16, 9.9, 14.4]
explode = (0, 0.1, 0, 0)  # Highlight second slice
plt.pie(sizes, labels=labels, autopct='%1.1f%%', shadow=True, startangle=90, explode=explode)
plt.axis('equal')
plt.show()
```

🔹 Histograms
```Python
mu, sigma = 100, 15
x = mu + sigma*np.random.randn(10000)
plt.hist(x, bins=50, density=True, facecolor='green', alpha=0.75)
plt.xlabel('Value')
plt.ylabel('Probability')
plt.grid(True)
plt.show()
```
🔹 Saving Plots
```Python
plt.savefig("figure.png")
```

This saves the current plot as figure.png in the working directory.

📚 Key Takeaways

Matplotlib provides versatile plotting functions for analysis.

Graphs can be styled using colors, markers, line styles, labels, and legends.

Useful for line graphs, scatter plots, pie charts, histograms, and subplots.

Graphs can be customized, scaled, and saved for reporting or presentations.
