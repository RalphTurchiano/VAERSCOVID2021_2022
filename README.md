# VAERSCOVID2021_2022
VAERS DATA PLUS COVID VACCINE RATES MERGED FOR 2021 AND 2022  

Downloaded CSV's VAERS DATA VAERS Symptoms VAERS Vaccine for all of 2021 and 2022  

https://vaers.hhs.gov/data/datasets.html
Downloaded COVID-19_Vaccination_Trends.csv for 2021 and 2022 from COVID-19 Vaccination Trends in the United States,National and Jurisdictional 
https://data.cdc.gov/Vaccinations/COVID-19-Vaccination-Trends-in-the-United-States-N/rh2h-3yt2
Merged VAERS DATA VAERS Symptoms VAERS Vaccine on VAERS_ID inner
Concatenated Years 2021 and 2022 inner
Isolated the Rows for Vaccine Type COVID19
Dropped rows with reported COVID Vaccine Dates prior to 2019
Mask Created for rows start_date = '11/11/2019' to end_date ='12/30/2022'
Filled missing NAN NUMDAYS by taking the median of NUMDAYS
Filled missing NAN AGE_YRS by taking the median of AGE_YRS
Fixed Missing Vaccine Dates Dates by subtracting Time Delta NUMDAYS from ONSET_DATE
Isolated Columns  'VAX_DATE','VAERS_ID', 'SYMPTOM1', 'SYMPTOM2', 'SYMPTOM3', 'SYMPTOM4', 'SYMPTOM5', 'VAX_TYPE', 'VAX_MANU','VAX_DOSE_SERIES', 'AGE_YRS', 'SEX', 'SYMPTOM_TEXT', 'DIED', 'DISABLE','RECOVD', 'ONSET_DATE', 'NUMDAYS', 'BIRTH_DEFECT'
Isolated dates rows from COVID-19_Vaccination_Trends.csv for 2021 and 2022
Isolated Admin rows from COVID-19_Vaccination_Trends.csv
Isolated Columns Date, Administered_Daily, Administered_Cumulative ,  Administered_7_Day_Rolling_Average
Merged OUTER Refined VAERS CSV Files with COVID-19_Vaccination_Trends on VAX_DATE inner with ffill 
Replaced Missing information in VAX_DOSE_SERIES: UNK, SEX: UNK, DIED: N, RECOVD: UNK, BIRTH_DEFECT: UNK, 'DISABLE: UNK
After Converting for Dates, simplified data types through convert_dyoes
For Data Mining created two Refined CSV files 
'COVIDVAERS_WITH_DUPLICATES2021_2022.csv' has all rows including duplicated VAERS_ID's for text mining
'COVIDVAERS_NO_DUPLICATES2021_2022.csv' removed duplicated VAERS_ID kept first
 
