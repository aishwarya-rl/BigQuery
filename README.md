  #1
  SELECT max(cumulative_confirmed) 
  FROM `bigquery-public-data.covid19_open_data.covid19_open_data`
  where country_name = 'India' 
  LIMIT 10

  ![image](https://user-images.githubusercontent.com/79004583/109800462-a304a180-7c36-11eb-9bcf-09cd90d63e65.png)

  #2
  SELECT Ave_Age_of_Mother, Ave_Pre_pregnancy_BMI
  FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality` 
  LIMIT 10
 
 ![image](https://user-images.githubusercontent.com/79004583/109800387-89635a00-7c36-11eb-9cbc-cbda77698507.png)

 
  #3
  SELECT GeoFIPS, GeoName, Earnings_per_job_avg AS earnings_2012, Year
  FROM `bigquery-public-data.sdoh_bea_cainc30.fips`
  WHERE Year='2012-01-01'
  LIMIT 10
  
  ![image](https://user-images.githubusercontent.com/79004583/109800312-6b95f500-7c36-11eb-8f19-5a7eae0b6a43.png)

  
  #4
  SELECT min (year) as min_year, max(year) as max_year 
  FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
  LIMIT 10
  
  ![image](https://user-images.githubusercontent.com/79004583/109800231-5b7e1580-7c36-11eb-9262-b03f1adae949.png)

  
  #5
  SELECT count(midyear_population) as zero_population,
  FROM `bigquery-public-data.census_bureau_international.midyear_population_5yr_age_sex`
  WHERE midyear_population = 0
  
  ![image](https://user-images.githubusercontent.com/79004583/109800170-4ef9bd00-7c36-11eb-9421-62dd669e9b46.png)

  
  #6
  SELECT country_name 
  FROM `bigquery-public-data.census_bureau_international.midyear_population_5yr_age_sex`
  group by country_name 
  order by country_name
  LIMIT 100
  
  ![image](https://user-images.githubusercontent.com/79004583/109800119-3f7a7400-7c36-11eb-9d1c-0137d848a6f0.png)

  
  #7
  SELECT region_name, max(hospitalized_patients_intensive_care) 
  FROM `bigquery-public-data.covid19_italy.data_by_region`
  group by region_name
  LIMIT 10
  
  ![image](https://user-images.githubusercontent.com/79004583/109800064-2d98d100-7c36-11eb-9f1e-7d39469ba199.png)

  
  #8
  SELECT
  FROM `bigquery-public-data.covid19_italy.data_by_province` 
  INNER JOIN `bigquery-public-data.covid19_italy.data_by_region` 
  ON `bigquery-public-data.covid19_italy.data_by_region`. region_code = `bigquery-public-data.covid19_italy.data_by_region`.region_code
  LIMIT 20
  
  ![image](https://user-images.githubusercontent.com/79004583/109799989-19ed6a80-7c36-11eb-8c74-dcc1faaf3876.png)

  
  #9
  SELECT *
  FROM `bigquery-public-data.world_bank_global_population.population_by_country` 
  WHERE country = "United Arab Emirates"
  
  ![image](https://user-images.githubusercontent.com/79004583/109799742-cf6bee00-7c35-11eb-8d7e-418e6e4622ed.png)

  
  #10
  SELECT SUM(year_2018) as total_pop_in_2018
  FROM `bigquery-public-data.world_bank_global_population.population_by_country` 
  
  ![image](https://user-images.githubusercontent.com/79004583/109799430-7ac87300-7c35-11eb-83d5-418ed0f77872.png)

