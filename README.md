# Tableau_citibike_NJ_Domaica

The requirements of this project asked for visualization and analysis  around the largest bike sharing program in the United States.
Data for program is publicly available and can be foung on the Citi Bike Data webpage:

LINK: https://www.citibikenyc.com/system-data

There are 2 sets of data available. The program has 2 locations in New York and Jersey City
After several downloads, played with data and try and error attempts, I have decided to use for the analysis Jersey City data for the whole year 2019.

Main reason is that for NY I have collected data and after doing proper extraction, cleansing, etc the load files where up to +3 GB of data which made my exercise painful. 

Jersey City datasets are more manageable than NY ones.


## Main technologies used to deploy this project

- 'Python' programming language including 'pandas' package.
- 'Tableau' as visual analytics platform or visualization tool.


## Main folder for solution is called: 'Tableau_citibike_NJ_Domaica'

Inside that root folder, we can find 3 files:

- 'README.md' -> Markdown with project explanation.
- 'citibike_ETL_NJ_2019_v1.ipynb'  notebook file used by Jupyter Notebook with code for Extraction, Transformation and Load to prepare files containing data for the project.
- 'DOMAICA_NJ_citibike_2019_v1.twbx' -> Tableau packaged workbook file as a data file created with Tableau Desktop program containing the full analysis charging data file 'FINALALL2019-citibike-NJ.csv'

### - Subfolders 

And 3 additional folders:

- 'instructions'.- Folder containing initial instructions for exercise.
- 'instructions/Images' .- Subfolder with some images used for readme.md explanations.
- 'data2019NJ'.- downloaded zip files with data for analysis
- 'Final_resources_NJ'.- up to 14 .csv files in different subfolders with monthly data. Final file 'FINALALL2019-citibike-NJ.csv' after ETL transformation containing saved data.

## Processing of data & analysis using jupyter. 'citibike_ETL_NJ_2019_v1.ipynb'


### 1st Step.- DATA PROCESSING

#### EXTRACTION
Downloaded 12 csv files from Citi Bike Data webpage for year 2019 and decided to do analysis for Jersey City (New Jersey) instead of New York.

![alt text](https://github.com/domaica/Tableau_citibike_NJ_Domaica/blob/main/Instructions/Images/csv.png)


#### TRANSFORMATION

1./ Cleaning records like trips with origin and end in same station with 1 minutes 30 seconds or less to avoid include mistakes or broken bike 

2./ Converting trip duration records (measured in seconds) to minutes

3./ Rename some columns

4./ Rename some content (f.ex gender stored as 0,1,2 instead of 'male', 'female', 'unknown')

![alt text](https://github.com/domaica/Tableau_citibike_NJ_Domaica/blob/main/Instructions/Images/rename_content.png)

5./ Change object types to be able to operate with them.

6./ Calculate 'age' substracting from year where record was updated (2019) the corresponding 'birth year'

![alt text](https://github.com/domaica/Tableau_citibike_NJ_Domaica/blob/main/Instructions/Images/age.png)


7./ Additional things as create age segments through bins, new columns to identify trips, etc.

#### LOAD

Save results in csv file.

![alt text](https://github.com/domaica/Tableau_citibike_NJ_Domaica/blob/main/Instructions/Images/final%20csv.png)


### 2nd Step.- ANALYSIS. 'DOMAICA_NJ_citibike_2019_v1.twbx'

It has been created with tableau desktop. It contains Multiple sheets, dashboards and a story. Please refer to it for analysis and results.

I've been unable to link it to Tableau Public and publish it in internet. Whenever i tried to open the file as .twbx with Tableau Public, the system produces an error like it has to exist previouly in tableau public. 

![alt text](https://github.com/domaica/Tableau_citibike_NJ_Domaica/blob/main/Instructions/Images/error.png)


I cannot send it from Tableau desktop to Tableau public because the only 2 ways I can do it are:

1./ Reproduce the whole work step by step recreating every sheet, dashboard and story, which is long and unpractical.
2./ Get additional "Tableau Server" software.

So I will leave it as a github link.


### - Webpage published in following link:

https://github.com/domaica/Tableau_citibike_NJ_Domaica


