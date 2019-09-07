# Grouping MRT Stations</br>利用K-means Clustering替北捷站點進行分類</br>


Use MRT hourly data to run Kmeans analysis based on entrance and exit number of people for each station 
</br>
Please visted [Medium](https://medium.com/urban-matters/%E6%8D%B7%E9%81%8B%E5%88%86%E6%99%822-f351661ce609) for reference.

Continue on the project [_MRT_Cleaning_Visualizing_](https://github.com/ShihWen/MRT_Cleaning_Visualizing), here the data will be reshaped and divied into entrance and exit for each station, and run K-means clustering in order to explore deeper relation between stations in terms of people flow.</br>

Below is the processing flow:
</br>
![](https://github.com/ShihWen/MRT_Kmeans/blob/master/image/flow_chart.png)
</br>
Steps

1. Refine the data using functions in MRT_cleaning_visualizing.ipynb, which will be used as raw data for K-means, </br>where the data for each stations has been transfered from 7*21 table to a list and normalized.
![](https://github.com/ShihWen/MRT_Kmeans/blob/master/image/raw_data.png)
2. Run K-means analysis with those hourly number of people as variables by _MRT_K-means_Analysis.ipynb_, which will generate:
    * k_pack_IN/OUT csv file for raw data of entrance and exit separately
    * cluster_group_IN/OUT csv file showing which stations belong to which cluster group
    * line graph and heat map grouped by cluster
    * df_cluster.csv showing the entrance and exit group for each station
3. Visualize the result in terms of clusters by heat map and line graph:

|entrance cluster 0|entrance cluster 1|entrance cluster 2|entrance cluster 3|
| ------------- |:-------------:| :-----:| :-----:|
| ![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_in_heatmap_0_3.png)|![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_in_heatmap_1_3.png)|![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_in_heatmap_2_3.png)|![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_in_heatmap_3_3.png)|

|exit cluster 0|exit cluster 1|exit cluster 2|exit cluster 3|
| ------------- |:-------------:| :-----:| :-----:|
| ![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_out_heatmap_0_3.png)|![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_out_heatmap_1_3.png)|![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_out_heatmap_2_3.png)|![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_out_heatmap_3_3.png)|

Line graph for entance:
![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_in_lineGraph.png)
Line graph for exit:
![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/All_out_lineGraph.png)

4. Visualize the result in terms of single station via _MRT_K-means_StationDashboard.ipynb_, which generates dashboard for all stations under the folder created by _MRT_K-means_Analysis.ipynb_:
![](https://github.com/ShihWen/MRT_Kmeans/blob/master/notebook_illustration/single_plot/1_2/BL12%20Plot.png)

5. Spacialize the result using QGIS:

|entrance cluster 0|entrance cluster 1|
| ------------- |:-------------:|
| ![](https://github.com/ShihWen/MRT_Kmeans/blob/master/image/inward_3.png)|![](https://github.com/ShihWen/MRT_Kmeans/blob/master/image/inward_1.png)|

|entrance cluster 2|entrance cluster 3|
| ------------- |:-------------:|
| ![](https://github.com/ShihWen/MRT_Kmeans/blob/master/image/inward_4.png)|![](https://github.com/ShihWen/MRT_Kmeans/blob/master/image/inward_2.png)|
