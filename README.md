# Automated Graph Customization Library 

## Project Name: `projecteasygraph`
## Description:
Effective data visualization is critical in data analysis and marketing, as it facilitates quick understanding of complex data sets, pattern identification, anomaly detection, and overall data behavior. To streamline this process, I have developed an automated library for creating custom graphs. This Python library leverages the plotly.graph_objects module to automate the creation of various types of graphs, including bar charts, histograms, line plots, scatter plots, and box plots. The library is highly customizable, allowing users to tailor the visualizations to their specific needs. 

## Features:
* Bar Graphs: Create vertical or horizontal bar graphs with customizable axes titles and orientation. Suitable for comparing categorical data across one or multiple variables.
* Histograms: Generate stacked or side-by-side histograms to visualize the distribution of data. Both vertical and horizontal orientations are supported.
* Line Graphs: Plot single or multiple line graphs to track changes over time or continuous data points. Customizable titles and labels enhance clarity.
* Scatter Plots: Develop scatter plots to examine relationships between variables. Support for multiple y-columns allows for detailed comparison.
* Box Plots: Create box plots for statistical analysis of data distribution. Supports plotting along x or y-axis for flexibility.

## Installation: pip install projecteasygraph
## Usage: Here are some examples of how to use the projecteasygraph library to create different types of graphs:

Bar Graph
import pandas as pd
from easy_graph_exam import bar_graph

data = {'Category': ['A', 'B', 'C'],
        'Value1': [10, 15, 7],
        'Value2': [12, 18, 10]}
df = pd.DataFrame(data)

fig = bar_graph(data=df, x_column='Category', y_column=['Value1', 'Value2'],
                title='Sample Bar Graph', xaxis_title='Category', yaxis_title='Values')
fig.show()


Histogram
from easy_graph_exam import histogram_graph

data = {'Scores': [10, 20, 20, 40, 50, 50, 50, 60]}
df = pd.DataFrame(data)

fig = histogram_graph(data=df, columns='Scores',
                      title='Sample Histogram', axis_title='Scores')
fig.show()


Line Graph
from easy_graph_exam import line_graph

data = {'Year': [2018, 2019, 2020, 2021],
        'Sales': [150, 200, 250, 300]}
df = pd.DataFrame(data)

fig = line_graph(data=df, x_column='Year', y_column='Sales',
                 title='Sales Over Time', xaxis_title='Year', yaxis_title='Sales')
fig.show()


Scatter Plot
from easy_graph_exam import dispersion_graph

data = {'Height': [150, 160, 170, 180],
        'Weight': [50, 60, 70, 80]}
df = pd.DataFrame(data)

fig = dispersion_graph(data=df, x_column='Height', y_column='Weight',
                       title='Height vs Weight', xaxis_title='Height', yaxis_title='Weight')
fig.show()


Box Plot
from easy_graph_exam import box_plots

data = {'Category': ['A', 'B', 'C'],
        'Values': [10, 20, 30]}
df = pd.DataFrame(data)

fig = box_plots(data=df, y_column='Values', title='Sample Box Plot',
                yaxis_title='Values')
fig.show()

## Conclusion
The easy_graph_exam library simplifies the process of creating insightful and customizable visualizations, making it an invaluable tool for data analysis and marketing projects. By automating graph creation, users can focus on interpreting data and making data-driven decisions more efficiently.
