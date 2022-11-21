# Web Scraping Mars Data
Data Bootcamp week 11 - web scraping

## Overview
This exercise involved scraping web data for NASA's mission to Mars. 

The guided homework portion of the exercise involved using HTML, CSS, and Chrome Developer tools to scrape data from websites, and then automating that process with Splinter and BeautifulSoup.

The independent challenge portion of the exercise involved two deliverables: scraping titles and preview text from news articles about Mars and scraping Mars weather data from a table.

## Process

### Deliverable 1: Scrape Titles and Preview Text from News Articles about Mars
As saved in [this file](https://github.com/larabjork/mars-scraping/blob/main/mars_data_challenge_part_1.ipynb), Splinter and BeautifulSoup were used to scrape article information from [redplanetscience.com](https://redplanetscience.com). These results were exported to a JSON object. The following image shows a portion of that object:

![Excerpt of JSON object](LINK)

### Deliverable 2: Scrape and Analyze Mars Weather Data
As saved in [this file](https://github.com/larabjork/mars-scraping/blob/main/mars_data_challenge_part_2.ipynb), two methods were used to scrape data from [this page](https://data-class-mars-challenge.s3.amazonaws.com/Mars/index.html).
Data was first scraped using Pandas' read_html function, and then the same task was performed using Splinter and BeautifulSoup. The Splinter-BeautifulSoup data was used for the rest of the exercise, and the resulting dataframe is shown below.

![Mars weather dataframe](LINK)


## Analysis
Deliverable 2 also included four questions about Mars Weather

* How many months exist on Mars?
Using the Pandas describe function to find the maximum value for the "month" column of the dataframe shows that there are 12 months on Mars.

![Summary of Mars data from month column](LINK)

* What are the coldest and the warmest months on Mars, based on average minimum temperature by month? 
Using the Pandas groupby function to aggregate the data, then calculating the mean minimum temperature shows that on Mars, the coldest month is Month 3, and the warmest month is Month 8, as shown in the following bar chart.

![Average minimum daily temperature by month](LINK)

* Which months have the lowest and the highest atmospheric pressure on Mars? 
Using the Pandas groupby function to aggregate the data, then calculating the mean atmospheric pressure shows that on Mars, the lowest atmospheric pressures are in Month 6, and the highest atmospheric pressures are in Month 9, as shown in the following bar chart.

![Average atmospheric pressure by month](LINK)

* About how many terrestrial (Earth) days exist in a Martian year? 
By plotting the average minimim daily temperature on Mars against the terrestrial (Earth) date as shown below, I was able to see peaks and valleys in the data that presumably approximate seasonal/annual variation. Looking at the span from the lowest values for 2014 and for 2016, I estimated that a Martian year is approximately 1.8 Earth years, which calculates to ~657 terrestrial days in a Martian year.

![Mars temperature versus Earth date](