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
<iframe src="../assets/chart1.html" width="100%" height="100%"></iframe>

This chart visualizes the count of occurrences for each state in the dataset. The x-axis represents the states, while the y-axis shows the count of data points for each state. Each bar is color-coded according to the state it represents, allowing viewers to easily distinguish between the different states at a glance.

x-axis: 
The state:N encoding specifies that the x-axis will represent categorical (nominal) data, specifically the names of different states.

y-axis: 
The count():Q encoding aggregates the data, providing a quantitative count of occurrences for each state. The count() function counts how many records exist for each unique state value, which is a suitable representation when dealing with categorical data.

Color: 
The color = 'state:N' encoding assigns a different color to each state, helping to visually separate the bars and make the chart easier to interpret. Each state gets a unique color, which is effective in emphasizing the individual states.

Data Transformations:
In the analysis, the primary transformation applied was the use of count() to aggregate the data by state. The count() transformation groups the data by the state variable and computes the total number of records for each state. This transformation allows for a clear representation of how frequently each state appears in the dataset, and helps summarize the data into meaningful counts for visualization. The chart focuses primarily on counting the occurrences per state, which directly translates to the bar heights in the chart.


<h2>Viz 2: Average Precipitation Probability</h2>
<iframe src="../assets/chart2.html" width="100%" height="100%"></iframe>

Example comes from this [great blog post right here](https://blog.4dcu.be/programming/2021/05/03/Interactive-Visualizations.html) that was also used in [our test import script](https://github.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/blob/main/week01/test_imports_week01.ipynb).

We can use a vegachart HTML tag like so:

In theory, you can also use [Jekyll hooks](https://jekyllrb.com/docs/plugins/hooks/) to do it, but I haven't figured out a way that looks nice yet.


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/vega/vega/blob/main/docs/data/cars.json" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/test_generate_plots.ipynb" text="The Analysis" %}
</div>
