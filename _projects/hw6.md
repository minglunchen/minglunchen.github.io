---
name: Altair Project
tools: [Python, HTML, Altair]
image: assets/pngs/altair1.png
description: This is a project that uses altair for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Altair visualization

<h2>Viz 1: State Count</h2>
<iframe src="../assets/chart1.html" width="100%" height="400px"></iframe>

This chart shows how many times each state appears in the dataset. The x-axis represents the states, and the y-axis shows how many records exist for each state. Each bar is colored differently based on the state it represents, making it easy to tell the states apart at a glance.

x-axis / y-axis:

The x-axis displays the states, which are categories (also called nominal data). The y-axis shows a count of how many records there are for each state. The count() function is used to count the number of records for each unique state. This method is helpful for visualizing data that is grouped by categories, like states.

Color:

The color of each bar is used to assign a unique color to each state. This helps to visually separate the bars and makes the chart easier to read. By using different colors for each state, viewers can easily see which bar corresponds to which state.

Data Transformations:

The main data transformation used in this chart is the count() function, which groups the data by state and counts how many records belong to each state. This transformation helps us understand how often each state appears in the dataset and determines the height of each bar in the chart.


<h2>Viz 2: Average Precipitation Probability</h2>
<iframe src="../assets/chart2.html" width="100%" height="400px"></iframe>

This visualization shows the relationship between states and their average probability of precipitation. The chart uses bars to represent the average precipitation probability for each state. The height of each bar reflects the average precipitation probability for that state. There's also a line that shows the overall average precipitation probability across all states. The chart is interactive, allowing users to select specific regions (states) along the x-axis using a brush tool. When a region is selected, the bars in that area become fully visible, while the others fade out.

x-axis / y-axis:

The x-axis shows the states, which are categories (nominal data). The y-axis shows the average precipitation probability for each state. The mean() function is used to calculate the average precipitation probability for each state based on all the data points.

Opacity:

The opacity of the bars changes depending on whether they are part of the selected region. If a user selects a group of states, the bars in that region become fully visible (100% opacity), while the bars outside the selection become slightly transparent (70% opacity). This helps emphasize the selected states and makes the other states less noticeable.

Color Scheme:

The chart doesn't use color to distinguish the bars, but the opacity and the color of the rule line help to make the chart easier to interpret. The rule line is given a distinct red color (firebrick) to make it stand out, so users can easily compare the overall average precipitation probability with the individual states.

Data Transformations:

The main transformation applied to the data is calculating the average precipitation probability for each state. This is done by grouping the data by state and computing the average precipitation probability for each one. This helps to summarize the data in a clear way and makes it easier to understand the overall trends.

Interactivity:

The chart is interactive, meaning users can select a region of states along the x-axis (using a brush tool). When a region is selected, the opacity of the bars in that area changes to 100%, while the rest of the bars fade to 70% opacity. This makes it easier to focus on a specific part of the data. The interactivity encourages users to explore the data and compare different states or groups of states, making the chart more engaging and helpful for analysis.


