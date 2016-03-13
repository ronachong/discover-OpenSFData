# Playing With SF Open Data at Holberton School
Open Data is a concept that is becoming more popular as new technologies allow for vast collections of data and the potential to distribute information more freely. (Think Aaron Schwartz, open source philosophy, etc...). Since the Data.gov initiative was launched mid-2009, the work of developers working with open data has grown alongside the number of cities releasing public records of their data.

SF happens to be one of the earliest U.S. municipalities to adopt open data and is a leader in open data dissemination. But as great as it is to have open data, it can be hard to appreciate when it isn't easy to digest. Today our challenge is to fetch data from the API for SF OpenData (SODA), compute it, and visualize the data in a consumer-friendly and accessible way using Javascript libraries. We will also be building websites to host our visualized data.

In your group of 4, discuss what dataset from SF OpenData you would like to work with and how you would like to present the data. You should also discuss what skills levels you have and how you would like to split up tasks, since you only have 4 hours to work together.

Here are the various tasks for you to work on:

+ Retrieve the data, either by fetching data from SODA or simply downloading the file
+ Compute the data into the dataset needed by your Javascript
+ Visualize your data using a Javascript library
+ Build a website to host your visualized data

Before tackling any of the above tasks, you will need to know what your project idea is and what Javascript library you are trying to use. Your choice will inform many of the steps!

The most doable project would be to visualize your selected data with charts and graphs a la [Highcharts](http://www.highcharts.com/) or [Chart.js](http://www.chartjs.org/). But if you would like to be ambitious, feel free to aim for something else.

At the end of your 4 hours, upload your page on a Github page (if your website is static), or on a student server if need be.

## Tips and Links
1. Different Javascript libraries:
  * http://www.highcharts.com/
  * http://www.chartjs.org/
  * http://marketblog.envato.com/resources/open-source-javascript-data-chart-libraries/
  * http://www.sitepoint.com/15-best-javascript-charting-libraries/
  * http://www.fastcompany.com/3029760/the-five-best-libraries-for-building-data-vizualizations
  * https://d3js.org/

2. Examples of open data projects for you to browse:
  * DataSF's showcase of apps utilizing their data (mostly mobile apps to do with maps!): http://apps.sfgov.org/showcase/
  * Refik Anadol's [Virtual Depictions](http://thecreatorsproject.vice.com/blog/otherworldly-data-sculptures-appear-in-san-francisco) (located at Salesforce)
  * Bay Area Bike Share's [2014 Open Data Challenge](http://www.bayareabikeshare.com/datachallenge-2014)

3. Concepts you may want to acquaint yourself with:
  * [SDKs vs. APIs vs. libraries](https://www.reddit.com/r/explainlikeimfive/comments/1al2az/eli5_what_is_an_api_what_is_a_sdk_what_is_an_ide/) (note that SODA uses the term SDK imprecisely)
  * the purpose of json(strings)
  * dealing with data statically versus dynamically (see concept below)

## Dealing with data statically versus dynamically
We often use the terms "static" and "dynamic" when it comes to websites. A static website is unchanging and stays the same regardless of how we interact with it. A dynamic website has content and/or presentation that can change (courtesy of script that loads every time the site is loaded). The same static-dynamic concept can be applied to data handling. If you deal with data statically, you're using your dataset as a fixed set of values; if you deal with data dynamically, you're using it as a set of data that changes over time.

In today's project you have a choice about how to handle the data: dynamically or statically. For instance, if you wanted to have a bar chart of the number of tech workers relative to other workers living in San Francisco, and you wanted this chart to always pull from the latest data on SF Open Data, you'd want your code to fetch, parse, and compute the data every time your visualization is rendered. On the other hand, if you wanted bar charts that showed the ratio of workers at specific points in time (e.g., 5 years ago compared to now), there's really no point fetching, parsing and computing the data every time your visualization is rendered. You just need to download or pull the data to your local server, compute the numbers you want, and add it to your Javascript one time. This means that you are working with a static set of data.

![alt "diagram of data handling process"](https://raw.githubusercontent.com/ronachong/discover-SFOpenData/master/static_vs_dynamic_data_handling.png)

Clearly the process for dealing with static data is a lot less involved, so if you are considering today's time constraints, you will most likely want to handle the data in a static manner. If you feel very advanced and would like to take on a greater challenge, you could approach the data in a dynamic manner.

## Project Tasks
### 0. Grab your dataset from SF Open Data

As the title says!

You can either fetch the data from SF Open Data using the SODA API, or, (if you are visualizing static data, which you most likely are) simply use the download button to download the data onto your local server. 

The SF OpenData site: https://data.sfgov.org/

If you plan on fetching data using SODA:
DataSF Developer Resources: https://data.sfgov.org/developers
Socrata's guide to using its API: https://dev.socrata.com/consumers/getting-started.html
*Note that you can use any language you prefer to fetch the data! For Holberton students, you've had experience grabbing data from an API with Go and Javascript, but now you can use whatever language you prefer (Javascript, Python, Go, Ruby...). Just find the appropriate documentation.
Note also that the "software developer kits" provided by SODA are not super polished and it's up to you as to whether you want to use them or code your http requests from scratch.
Mark Lee's example of pulling data from SODA: http://themarklee.com/2014/04/03/pulling-json-data-open-data-api/

### 1. Compute the data
Here, when we say "compute", we really mean 2 things:

1) parse the data you've pulled to isolate the values you need for your Javascript function

2) transform the data you've parsed into a form that your Javascript is able to process (if need be)

Again, feel free to use whatever language you feel like for this part of the process.

any resources to share here? I feel like this is mostly algorithmic stuff.
probably links to methods to convert data to javascript or json stuff

### 2. Write your Javascript
In most cases, you won't have too much code to write other than the code already provided by your library.

But--of course--you will have to input your data (pass your data as parameters).

If you're trying to use data dynamically, you might have to come up with a function to request the data from the web server every time the page loads.

If you're dealing with static data, then all you have to do is import your data (now that it's been computed to a form usable by Javascript)... or simply put it in manually!



### 3. Write your HTML and CSS

Use your knowledge of HTML and CSS to put together a website which will house your nicely visualized data. You can use Bootstrap if you like, or code from scratch.
