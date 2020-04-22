---
title: "Covid19 Dashboard"
date: 2020-04-21T15:22:17+08:00
draft: false
---

Hi everyone. I have created a simple and straightforward Tableau dashboard about COVID-19. The dashboard focuses on Malaysia data, but there is an overview of worldwide cases. The dashboard consists of two pages, the first page showing a world map with tooltips displaying the number of cases, deaths and recovered in each country. At the top of the map, there is the information of total cases, total deaths and total recovered worldwide. Below the map, there is a table with countries, cases, deaths and recovered cases. There is also a filter by country, to filter the page to get single or multiple countries.

{{< resize-image src="covid1.png" alt="Dashboard Page 1" >}}

The next page of the dashboard focussing on Malaysia COVID-19 cases. Like the first page, there is a map of Malaysia. By hovering into different states, users can see the number of cases, deaths and recovered in each state. There are 3 line charts daily of total case, deaths and recovered in Malaysia. From this chart, we can observe the daily numbers of each case in Malaysia. Then, we have a table of state, total case, total death and mortality rate for each state. The mortality rate is defined as the number of death in a population. It is calculated from the number of death divided by the number of cases of COVID-19. Users can sort the table by clicking at the header name. 

{{< resize-image src="covid2.png" alt="Dashboard Page 2" >}}

On data collection, I am using python with BeautifulSoup package to crawl data from https://www.worldometers.info/coronavirus/ and stored them in a csv file. For data on Malaysia cases, I crawled the data from various sites such as https://www.outbreak.my/ and <https://www.thestar.com.my/news/nation/2020/03/23/covid-19-current-situation-in-malaysia-updated-daily>. The code can be found here https://github.com/nooraizad/Basic-Web-Scrapper. The csv files later will be used at Tableau to create the visualisation. 

For data refresh, I run the script daily. The script is run every day at 9:00 pm Malaysian time. I am looking method to run the script automatically, and then the data source will be consumed by Tableau automatically. Based on my findings, I can achieve this by setting up a pipeline in Azure Data Factory, host my Python script there and setup a schedule so that the pipeline will be run daily. I will be starting to explore Azure Data Factory and will share the findings. 
The dashboard that I have created is simple and straightforward. But I believed it has the critical measurement that we would like to know about the COVID-19. I might add more features and measurement in the future. Any idea and suggestion are welcome. 

Kaggle is hosting COVID-19 Open Research Dataset Challenge. The competition challenge data scientist to provide meaningful insight about COVID-19. I think every data scientist should join the competition and contribute to the community on the findings. Together, we fight this pandemic by staying at home and play our role as a data scientist to help provide results and insight that will be beneficial to everyone. I am joining the competition and will be sharing my findings in my future post.

Until next time, cheers.
 

