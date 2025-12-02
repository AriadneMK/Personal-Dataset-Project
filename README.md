# Bad Bunny Concert Locations 
## Introduction 
For this personal dataset I chose to look at tour dates for artist Bad Bunny's upcoming 2025-2026 concerts. The data came from data source JamBase, which compiles data on live performances from ticketing websites like Stubhub and Ticketmaster. After obtaining an API key, the data was directly exported from the website. 
## Data Processing 
As previously mentioned, the API key allowed me to export the data directly from the website. I first filtered for Bad Bunny concerts and then filtered for a start date of 01/01/2025. However, the data was in .json format so that I had to create a dataframe in Rstudio by uploading the direct code from the JamBase website. Once this was done I could edit the dataframe again in Rstudio to only contain information about the location of the venues (country, city, and longitude and latitude) and the dates of the concerts. This created the file that was uploaded here.  
## Exploratory Analysis 
The main feature of this graph are the clusters using the longitude and latitude coordinatees that show the location of each concert and the amount of concerts in that venue using the shading technique. 

latitude longitude.png

<img width="612" height="386" alt="latitude longitude" src="https://github.com/user-attachments/assets/d49fbe35-1c37-4c8a-a9b0-0a2dcbae3529" />


The next figure uses the same coordinates and the city/country information to show a graph with the clustering showing the different concert locations. 

map visualization.png

<img width="1455" height="753" alt="map visualization" src="https://github.com/user-attachments/assets/4da0a35d-2c82-436d-9966-531769eeec6d" />


## K-means Clustering 
Unsupervised learning was used through k-means clustering to show the different locations of concerts. This was chosen as I was exploring geographical location across the globe, with overlapping points (since there were several concert dates in the same location) and wanted a visualization that could convey this. The number of clusters chosen was 4 as I saw the groups worked best with that number. When I initially attempted to use three - which seemed more reasonable given that the countries in South America were much closer geographically than those in Western Europe and Australia - I found that the clusters in South America had merged closer even though the longitude and latitude coordinates showed a clear difference. As such I increased the number of clusters and produced a more clear graph. Through this I learned where shows were centered and how to pick the number of clusters carefully as to best represent the data. 
