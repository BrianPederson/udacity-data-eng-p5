## Project: Capstone (5)
#### Data Engineering Nanodegree
##### Student: Brian Pederson
&nbsp;
#### Project Description
Using several datasets provided by Udacity, build a dimensional star schema data model that can be used for simulated data analysis queries related to I94 tourist data as well as weather data (average temperature). The primary (large volume) dataset consists of 12 months of US Government I94 immigration data. This is supplemented with a "conformed" dataset containing average temperatures at the grain of year, month, state which is compatible with the year, month and destination state present in the I94 dataset. The project utilizes various tools covered in the course such as PostgreSQL, Pandas, Spark, etc.   

##### Data Sources
- World Temperature Data - ../../data2/GlobalLandTemperatoresByCity.csv
- I94 immigration Data - ../../data/18-83510-I94-Data-2016/<12 monthly files>
- I94 State Codes - data/i94_states.csv
- I94 Country Codes - data/i94_countries.csv
- I94 Ports of Entry Codes - data/i94_ports_entry.csv
- I94 Visa Codes - data/i94_visas.csv
- I94 Mode Codes - data/i94_modes.csv
- Zip Code Latitude and Longitude Data - data/us-zip-code-latitude-and-longitude.csv 

Note that the latter six files are not provided by Udacity. I have included them in archive **more_data.tar.gz**.
If necessary unzip them into the data directory via something like ```tar -xvf more_data.tar.gz -C data/```

##### Data Targets (PostgeSQL tables)
- i94_f - i94 Fact Table
- i94_state_month_temp_f - State Month Temperature Fact Table
- i94_states_d - States Dimension Table
- i94_countries_d - Countries Dimension Table
- i94_ports_entry_d - Ports of Entry Dimension Table
- i94_modes_d - Modes Dimension Table
- i94_visas_d - Visas Dimention Table

##### Program files
- Capstone Project.ipynb - Jupyter Notebook containing project
- logical_model_1.jpg - Logical/Conceptual Model Image
- README.md - this descriptive file
- more_data.tar.gz - this contains the additional source table csv files that were added to the project. Install them in the data/ directory if not running the project in the original development workspace.

Note there are other notebook files present in the project workspace that were used to explore the datasets and develop schemas, data pipelines and sample queries.
- create_tables.ipynb
- data_wrangline_pandas.ipynb
- data_wrangling_sql.ipynb
- Koalas_testing.ipynb

##### How to run the project
The process assumes:
- source datasets for I94 data are located in ../../data/
- source dataset for Global Temperature is located in ../../data2/
- all other source datasets (including additional csv files) are located in data/ 
- install pyarrow. ```pip install pyarrow```
- start up ```Capstone Project.ipynb``` and execute each cell in sequence.

##### Miscellaneous Notes
1. Install pyarrow prior to running the notebook.
2. If running the project on a fresh workbook install the contents of ```more_data.tar.gz``` into data/
