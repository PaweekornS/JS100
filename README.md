# JS100

This repository contains all materials from my term project, CPE393-Text Analytics. The purpose of this project is to display a heatmap of locations with road accidents from the JS100 official account's tweets.

### Web scraping
We have done 3 approaches for scraping the data from twitter:\
1. Twitter API v2 (fail): can call the API for only 15 mins so, we won't get enough data for our task
2. NTScraper (fail): can't use the Thai account to scrape data
3. Selenium (not a legal way but work!)

### Extracting Location
When we did the data exploration, we separated our dataset into 2 types which are hashtag and none-hashtag data. We used different approaches to extract the locations of each kind:
1. **Hashtag data**
- Almost of the tweets contains the location at the second position of # e.g. #อุบัติเหตุ ... #<location>. From these insight, we decided to use a regular expression (regex) for extracting the location.
2. **None-hashtag data**
- using thaiNER2.0 model from pythaiNLP package for extracting the location

### Data modelling and EDA
- Top 5 tags from JS100 tweet: #อุบัตเหตุ, #รถติด, #JS100, #ข่าวPNC, #JS100
- Top 5 accident locations from our extracted result: ถนนกาญจนาภิเษก, ถนนพหลโยธิน, ถนนเทพรัตน, ถนนจรัญสนิทวงศ์, ถนนพระราม2

### Heatmap creation
- using geopy package to extract the geo-coordinates from our extracted location
- using folium package for plotting the geo-coordiantes into the map
![image](https://github.com/user-attachments/assets/26e73211-b681-4d66-ba83-d601abbb384e)

## Team members
Paweekorn Soratyathorn\ 
Sawit Koseeyaumporn\
Mawin Srichat\
Pichawat Adulwiitayakorn

