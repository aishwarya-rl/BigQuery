#1
SELECT max(cumulative_confirmed) 
FROM `bigquery-public-data.covid19_open_data.covid19_open_data`
where country_name = 'India' LIMIT 10



#2
SELECT Ave_Age_of_Mother, Ave_Pre_pregnancy_BMI
FROM `bigquery-public-data.sdoh_cdc_wonder_natality.county_natality` LIMIT 10
 
 #3
  SELECT GeoFIPS, GeoName, Earnings_per_job_avg AS earnings_2012, Year
  FROM `bigquery-public-data.sdoh_bea_cainc30.fips`
  WHERE Year='2012-01-01'
  LIMIT 10
  
  #4
  SELECT min (year) as min_year, max(year) as max_year 
  FROM `bigquery-public-data.sdoh_bea_cainc30.fips` 
  LIMIT 10
  
  #5
  SELECT count(midyear_population) as zero_population,
  FROM `bigquery-public-data.census_bureau_international.midyear_population_5yr_age_sex`
  WHERE midyear_population = 0
  
  #6
  SELECT country_name 
  FROM `bigquery-public-data.census_bureau_international.midyear_population_5yr_age_sex`
  group by country_name 
  order by country_name
  LIMIT 100
  
  #7
  SELECT region_name, max(hospitalized_patients_intensive_care) 
  FROM `bigquery-public-data.covid19_italy.data_by_region`
  group by region_name
  LIMIT 10
  
  #8
  SELECT
  FROM `bigquery-public-data.covid19_italy.data_by_province` 
  INNER JOIN `bigquery-public-data.covid19_italy.data_by_region` 
  ON `bigquery-public-data.covid19_italy.data_by_region`. region_code = `bigquery-public-data.covid19_italy.data_by_region`.region_code
  LIMIT 20
  
  #9
  SELECT *
  FROM `bigquery-public-data.world_bank_global_population.population_by_country` 
  WHERE country = "United Arab Emirates"
  
  #10
  SELECT SUM(year_2018) as total_pop_in_2018
  FROM `bigquery-public-data.world_bank_global_population.population_by_country` 
  
  ![image](https://user-images.githubusercontent.com/79004583/109799430-7ac87300-7c35-11eb-83d5-418ed0f77872.png)

