# Big-Data-Project

Please refer the steps to reproduce in the report uploaded for a better understanding of how to  run the code and what datasets to use.



### 1. Data Collection: 


- All of the original datasets can be found in the Big-Data-Project-X/data/raw/ folder.
- All of the links for downloading this data can be found in the project report located at Big-Data-Project-X/reports/. 
- The one exception, is the air quality data. This data required the creation of custom scripts to call an external API for retriveing the data. 
- Instructions for running these scripts can be found in the README contained in Big-Data-Project-X/data_collection/EPA_AQS_Air_Data/.


### 2. Data Cleaning: 


- All code for cleaning the raw data can be found in ```Big-Data-Project-X/src/cleaning_src/```
- Multiple methods were used to clean the data, including Spark Jobs, Google Collab Notebooks, and OpenRefine. 
- Exact procedures for each of these methods can be found in the README in each of their respective sub-folders. 


### 3. Data Analysis/Visualization: 

- This is split into two folders, ```Big-Data-Project-X/src/analysis_src/``` and ```Big-Data-Project-X/src/vis_src/``` 
- Each of these folders have their own respective README files, explplaining the necessary steps to run the code. 
- If the data needed extra massaging before beiing visualized, ```Big-Data-Project-X/src/analysis_src/``` was used to create aggregated data files. 
- The visualizations were created using Altair, D3, and Tableau. Extra spatial data was required to create a spatial visualizations in Tableau. This data can be found in ```Big-Data-Project-X/data/Spatial_Data_For_Tableau_Viz/```


## General info:

There is also a folder that contains the cleaned and wrangled datasets, just for reference. 

Finally, there is a PDF with the report describing this project located at ```Big-Data-Project-X/reports/```. There is also a subfolder with the figures created for the report. 


## Requirements:

All of the required python libaries are located in requirements.txt. Before running any code, open the terminal on your local machine and run:
```
python3 -m virtualenv venv
source venv/bin/activate
pip install -r requirements.txt
```

Please go to this [link]()

* [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]()

Grade | Grade Point
------------ | -------------
![image](https://github.com/rushabhkenia/Big-Data-Project/blob/main/results/Visualizations_YTD/PhotosC/Annual_TrendC.png) | A
A | Excellent




In order to run each of the Notebooks, make sure to edit the string containing the file path to the original dataset, so that it correpsonds to the file path of the dataset in YOUR local directory. Additonally, ensure that the string for the output file path is edited so that it uses YOUR local directory. 
