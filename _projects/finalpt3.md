---
layout: default
title: Coast-to-Coast Budget Analysis
permalink: /final/
name: Final Part 3
tools: [Python, HTML, vega-lite, Altair]
description: visualizations for the last part of my final :)
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# Coast-to-Coast Budget Analysis

By: Annabelle Zhang

Note: I wasn't able to get the visualizations to work properly with vegalite and I had to save them as HTML files. So for the best viewing experience, please use light mode!

<br>
## Inspiration

When I did my first analysis on the City of Urbana's Budget Data, I realized that the planned budget increased every year. Whether it be plans for revenue (how much the city of Urbana thought that they would be able to make from taxes/government grants) or plans for expenses (how much the city planned to spend), the budget grew yearly. You can affirm this for yourself by toggling between the revenues and expenses for Urbana in the visualization I made below. Another interesting feature of this visualization is that for the most part, the city overestimated their budget - the actual balance (earned or spent) was almost always below the predicted value. I wondered if this was also consistent for other cities, and if other cities also had the overestimating effect that Urbana has. Unfortunately, the datasets that I was able to access mostly only had data on the budget, and not how much the city actually spent, so I couldn't test if all the other cities overestimated. However, to test the growing yearly budget observation, I decided to look at three other cities; Los Angeles, Chicago, and New York (coast to coast!). 

I wanted to choose bigger cities because I also have a theory on why the yearly budget for Urbana is growing. Urbana is a college town, and every year the city welcomes new people in the form of an incoming class for the University of Illinois Urbana-Champaign. This population boosting effect could be accounted for though, since Urbana also loses some residents in the form of a graduating class for UIUC. But I think that overall, incoming classes will grow the population, and since Urbana is slowly getting bigger, the city plans for its budget also growing. I know that people often move to New York and Chicago for jobs, so I guessed that New York and Chicago could also be considered growing cities. I added in Los Angeles because I also wanted to look at a city on the west coast, and although I'm not too knowledgeable about the job market in LA, I know UCLA is there, and that's a big public university, so maybe it could have a similar effect that I believe UIUC to be having on Urbana. To sum it up, my theory is that budget grows with population, and I wanted to see if budget grows for these other cities.

<br>

<iframe src="{{ site.baseurl }}/assets/html/final_chart.html" width="100%" height="550" frameborder="0"></iframe>

Below is a visualization I made using the dataset for New York City, New York, and I was actually able to test actual spending vs planned spending here. Although I didn't have a column for how much the city spent in the fiscal year, I did have a column for how much the city spent in the previous fiscal year. So for example, by hovering over the bars at the 2017 tick mark on the x-axis, we can see that in 2016, NYC spent 58,486 million dollars, and they planned to spend 62,524 million dollars in 2017. This is helpful because we can compare the purple bar of one year to the blue bar of the next year to see spending and planned spending of the initial year. The trends we saw for Urbana hold up for NYC as well, as planned spending is mostly greater than actual spending, and planned spending grows every year.

Note: for NYC, Chicago, and LA, the dataset didn't separate their budget into revenue and expenses, so I'm just assuming that they only list their expenses.

<iframe src="{{ site.baseurl }}/assets/html/final_chart1.html" width="100%" height="550" frameborder="0"></iframe>

Beneath this caption is a visualization I made of the yearly budget in Los Angeles, California. This dataset had a lot more years than the NYC and Urbana dataset, and it shows budget from 2010 to 2025. We see a lot more fluctuation in planned budget for LA, and it isn't consistently increasing like NYC and Urbana. I wanted to keep this visualization as a bar chart for consistency with my Urbana and NYC visualizations (although this data would probably be better represented as a line chart).

<iframe src="{{ site.baseurl }}/assets/html/final_chart2.html" width="100%" height="550" frameborder="0"></iframe>

This visualization I made shows the changes in budget for all four cities with normalization and compared to a baseline of their budgets in 2023. I was only able to find three years of budget for Urbana, so I can only show the changes of a two-year period for the four cities. Additionally, my source for the Chicago budget split their data by year, so I had to concatenate three datasets together. To create this visualization, I also only used the expenses budget of Urbana, because the datasets for the other cities didn't have a revenue budget (at least to my knowledge). I chose to normalize this visualization and also only show the changes in budget because the gap in budget for a city like NYC (90 billion at its peak) compared to Urbana's 100 million dollar budget would have created a visualization that we can't gain any insights from. The line for Urbana would be miles below the line for Champaign. If you want, you can take a look at my visualization code (button at the bottom right) to see how I made a budget index for each city and measured their growth. Urbana shows the greatest growth out of all the cities, but this makes sense since I'm measuring each city's growth against itself. For NYC, when their budget increases by 10 billion dollars, that's still only an eighth of their 2023 budget (80 billion). But when Urbana has a 30 million dollar increase, that's almost double its 2023 budget of 70 million dollars. Other than Los Angeles, my observation holds and budget grows yearly for the three cities. However, according to the US Census Bureau, "Los Angeles, California, returned to the list of top gainers for the first time since 2016, adding over 31,000 residents in 2024, making it third among the nation’s largest-gaining cities. A more complete picture of the 100 cities and towns with the largest population gains nationwide is shown in a map highlighting place-level increases". Clearly the population increased from 2024 to 2025, but there is a decrease in LA's budget from 2024 to 2025. This could be due to chance, but my initial theory could also be wrong, and population growth doesn't necessarily dictate city budget growth.

<iframe src="{{ site.baseurl }}/assets/html/final_chart4.html" width="100%" height="500" frameborder="0"></iframe>


<div class="left">
{% include elements/button.html link="https://data.illinois.gov/Local-Government/City-Of-Urbana-City-Budget-and-Spending-last-3-yea/dqkx-dat5/about_data" text="Urbana Data" %}
{% include elements/button.html link="https://catalog.data.gov/dataset/budget-2025-budget-ordinance-appropriations" text="Chicago 2025 Data" %}
{% include elements/button.html link="https://catalog.data.gov/dataset/budget-2024-budget-ordinance-appropriations" text="Chicago 2024 Data" %}
{% include elements/button.html link="http://catalog.data.gov/dataset/budget-2023-budget-ordinance-appropriations" text="Chicago 2023 Data" %}
{% include elements/button.html link="https://catalog.data.gov/dataset/mayors-management-report-spending-and-budget" text="New York Data" %}
{% include elements/button.html link="https://data.lacity.org/Administration-Finance/Open-Budget-Appropriations-Fiscal-Years-2010-2025/5242-pnmt/about_data" text="Los Angeles Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/annabelle-zhang/is445-analysis/blob/main/analysis.ipynb" text="Visualization Code" %}
</div>

<br> <br> <br> <br>

<br>
### Citations

US Census Bureau:

U.S. Census Bureau. (2025, January). Vintage 2024 population estimates [Press release]. https://www.census.gov/newsroom/press-releases/2025/vintage-2024-popest.html

Data: 

City of Urbana. (n.d.). City of Urbana city budget and spending last 3 years. Illinois Data Portal. Retrieved December 8, 2025, from https://data.illinois.gov/Local-Government/City-Of-Urbana-City-Budget-and-Spending-last-3-yea/dqkx-dat5/about_data

City of Chicago. (n.d.). Budget 2025: Budget ordinance appropriations. Data.gov. Retrieved December 8, 2025, from https://catalog.data.gov/dataset/budget-2025-budget-ordinance-appropriations

City of Chicago. (n.d.). Budget 2024: Budget ordinance appropriations. Data.gov. Retrieved December 8, 2025, from https://catalog.data.gov/dataset/budget-2024-budget-ordinance-appropriations

City of Chicago. (n.d.). Budget 2023: Budget ordinance appropriations. Data.gov. Retrieved December 8, 2025, from http://catalog.data.gov/dataset/budget-2023-budget-ordinance-appropriations

City of New York. (n.d.). Mayor's management report: Spending and budget. Data.gov. Retrieved December 8, 2025, from https://catalog.data.gov/dataset/mayors-management-report-spending-and-budget

City of Los Angeles. (n.d.). Open budget appropriations fiscal years 2010-2025. Los Angeles Open Data. Retrieved December 8, 2025, from https://data.lacity.org/Administration-Finance/Open-Budget-Appropriations-Fiscal-Years-2010-2025/5242-pnmt/about_data