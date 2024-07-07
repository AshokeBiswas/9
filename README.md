Q1. What is Matplotlib? Why is it used? Name five plots that can be plotted using the Pyplot module of Matplotlib.
Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. It is widely used for data visualization because it offers a variety of plotting capabilities and is highly customizable.

Why is it used?:

To visualize data in various forms (e.g., line charts, bar charts, scatter plots) for better understanding and analysis.
To create publication-quality plots and figures.
To enable easy integration with other libraries like NumPy, pandas, and SciPy.
Five plots that can be plotted using the Pyplot module of Matplotlib:

Line Plot
Scatter Plot
Bar Plot
Histogram
Pie Chart
Q2. What is a scatter plot? Use the provided code to generate data for x and y, and plot a scatter plot.
A scatter plot is a type of plot that displays values for two variables as a collection of points. Each point represents an observation in the dataset, with its position determined by the values of the two variables.

python
Copy code
import numpy as np
import matplotlib.pyplot as plt

np.random.seed(3)
x = 3 + np.random.normal(0, 2, 50)
y = 3 + np.random.normal(0, 2, len(x))

plt.scatter(x, y)
plt.title('Scatter Plot')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
Q3. Why is the subplot() function used? Draw four line plots using the subplot() function.
The subplot() function in Matplotlib is used to create multiple plots in a single figure. It allows you to arrange multiple plots in a grid layout, making it easier to compare different datasets side by side.

python
Copy code
import numpy as np
import matplotlib.pyplot as plt

x = np.array([0, 1, 2, 3, 4, 5])

y1 = np.array([0, 100, 200, 300, 400, 500])
y2 = np.array([50, 20, 40, 20, 60, 70])
y3 = np.array([10, 20, 30, 40, 50, 60])
y4 = np.array([200, 350, 250, 550, 450, 150])

plt.figure(figsize=(10, 8))

plt.subplot(2, 2, 1)
plt.plot(x, y1)
plt.title('Line 1')

plt.subplot(2, 2, 2)
plt.plot(x, y2)
plt.title('Line 2')

plt.subplot(2, 2, 3)
plt.plot(x, y3)
plt.title('Line 3')

plt.subplot(2, 2, 4)
plt.plot(x, y4)
plt.title('Line 4')

plt.tight_layout()
plt.show()
Q4. What is a bar plot? Why is it used? Plot a bar plot and a horizontal bar plot using the provided data.
A bar plot is a chart that presents categorical data with rectangular bars. Each bar's height or length is proportional to the values it represents. Bar plots are used to compare different categories of data.

Bar Plot:

python
Copy code
import numpy as np
import matplotlib.pyplot as plt

company = np.array(["Apple", "Microsoft", "Google", "AMD"])
profit = np.array([3000, 8000, 1000, 10000])

plt.bar(company, profit)
plt.title('Company Profits')
plt.xlabel('Company')
plt.ylabel('Profit')
plt.show()
Horizontal Bar Plot:

python
Copy code
plt.barh(company, profit)
plt.title('Company Profits')
plt.xlabel('Profit')
plt.ylabel('Company')
plt.show()
Q5. What is a box plot? Why is it used? Plot a box plot using the provided data.
A box plot (or box-and-whisker plot) is a standardized way of displaying the distribution of data based on a five-number summary: minimum, first quartile (Q1), median, third quartile (Q3), and maximum. Box plots are used to identify outliers and to understand the spread and skewness of the data.

python
Copy code
import numpy as np
import matplotlib.pyplot as plt

box1 = np.random.normal(100, 10, 200)
box2 = np.random.normal(90, 20, 200)

plt.boxplot([box1, box2], labels=['Box1', 'Box2'])
plt.title('Box Plot')
plt.ylabel('Values')
plt.show()
