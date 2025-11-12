---
name: Homework 5 Visualizations
tools: [Python, HTML, vega-lite, Altair]
description: Some visualizations with the Licenses Dataset
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Homework 5

Doing visualizations with the business licenses dataset!

## Visualization 1: Bar chart with dropdown to select License Status

<br>

<vegachart schema-url="{{ site.baseurl }}/assets/json/hw5_chart1.json" style="width: 100%"></vegachart>

<br>

This visualization displays the different professional license types in the dataset, with each bar representing a unique license type (such as DETECTIVE BOARD, COSMO, DENTAL, etc.) and showing the total count of licenses. It has an interactivity feature that lets users filter on license status through a dropdown. I used a horizontal stacked bar chart with quantitative encoding for the x-axis (the total number of licenses) and nominal encoding for the y-axis (the license type). The bars are colored by States using the tableau20 color scheme. I chose to color by states because I wanted to see if states used license statuses that other states don't use (for example, the DECEASED license status appears to only be used by the state of Illinois). I chose this color scheme because it has obviously different colors, making it easy to tell the different license statuses at just a glance, which is friendlier on the audience. On the analysis side, I performed data transformations like removing null and empty state values and grouping the data using pandas groupby() to count each license type and status combination. This aggregation step was crucial for creating accurate stacked bars and improving chart performance, and without it, I was getting an error when I tried to make my Altair chart. I wanted to make this specific visualization because I felt like it was something I was personally curious about when I initially looked through the business licenses dataset, and I found it hard to tell what licenses were in each category just from glancing at the dataset. I wanted to get an estimate of how many licenses were in each status, and I think my interactivity on this visualization gives the audience the power to do that. Finally, I saved the chart as a json to my assets and I was able to put it on this page.

<br>


## Visualization 2: Bar chart with dropdown to select State

<br>

<vegachart schema-url="{{ site.baseurl }}/assets/json/hw5_chart2.json" style="width: 100%"></vegachart>

<br>

The second visualization explores how different license types are distributed across states, (inspired by my findings about the license statuses only being used by certain states, I wondered if there were license types that some states didn't have) colored by their license status. This chart uses the same encoding types as the first visualization: quantitative encoding for the count on the x-axis and nominal encoding for license types on the y-axis. However, the coloring scheme here was done on License Status, using the category20 color scheme to ensure clear differentiation between active, expired, and other license statuses. I chose to color on license status because I felt like it would be helpful for users to also see how many active licenses are in the state. The interactivity feature I implemented in this visualization is a dropdown that allows users to filter the data by state. This interactivity lets users focus on specific states of interest and compare license type distributions across different states without being overwhelmed by all the observations. This was inspired by a similar idea as what was behind my first visualization, where I just wished to be able to see state information from the dataset, but that was definitely something I could not accomplish just from skimming through the dataset's rows and columns. The filtering allows patterns to show through (for example, the audience can easily see that Kentucky (KY) has less licenses than Illinois (IL)) The same data transformations from the first visualization were applied here, with the additional step of grouping by state to enable the state-based filtering functionality.

<br>

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/annabelle-zhang/data-visualizations/blob/main/hw5.ipynb" text="The Analysis" %}
</div>