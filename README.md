# Grouping MRT Stations</br>利用K-means Clustering替北捷站點進行分類</br>
Use MRT hourly data to run Kmeans analysis based on entrance and exit number of people for each station 
</br>
Please visted [Medium](https://medium.com/urban-matters/%E6%8D%B7%E9%81%8B%E5%88%86%E6%99%822-f351661ce609) for reference.

Continue on the project [MRT_Cleaning_Visualizing](https://github.com/ShihWen/MRT_Cleaning_Visualizing), here the data will be reshaped and divied into entrance and exit for each station, and run K-means clustering in order to explore deeper relation between stations in terms of people flow.</br>

Below is the processing flow:
</br>
</br>
<img src="https://github.com/ShihWen/MRT_Kmeans/blob/master/image/flow_chart.png" alt="alt text"  height="250">
</br>
1. Refine the data using functions in MRT_cleaning_visualizing.ipynb, which will be used as raw data for K-means, where the data for each stations has been transfered from 7*21 table to a list and normalized.
</br>
</br>
2. Run K-means analysis with those hourly number of people as variables.
</br>
</br>
3. Visualize the result in terms of clusters:
</br>
| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

