# bigquery_test
Business Analytics Assignment

SELECT Employer_contrib_pension_and_insurance FROM `bigquery-public-data.sdoh_bea_cainc30.fips`  
where 
Employer_contrib_pension_and_insurance<= 20000
LIMIT 100

SELECT MAX(Percapita_income_maintenance_benefits), GeoName  FROM `bigquery-public-data.sdoh_bea_cainc30.fips`  
GROUP BY  GeoName
LIMIT 100

SELECT SUM(Farm_proprietors_income) FROM `bigquery-public-data.sdoh_bea_cainc30.fips`  
LIMIT 100

SELECT GeoName, Employer_contrib_govt_and_social_insurance  FROM `bigquery-public-data.sdoh_bea_cainc30.fips`  
where 
GeoName LIKE '%FL'
LIMIT 100

SELECT Farm_proprietors_income, Farm_proprietors_employment,  FROM `bigquery-public-data.sdoh_bea_cainc30.fips`  
where 
GeoName LIKE '%FL'
LIMIT 100

SELECT GeoFIPS, GeoName, Income_maintenance_benefits FROM `bigquery-public-data.sdoh_bea_cainc30.fips`  
order by 
Income_maintenance_benefits desc 
LIMIT 100

SELECT GeoName, GeoFIPS, avg(Employer_contrib_pension_and_insurance), avg(Employer_contrib_govt_and_social_insurance) FROM `bigquery-public-data.sdoh_bea_cainc30.fips`  
GROUP BY 
GeoName, GeoFIPS
order by 
GeoFIPS
LIMIT 100

SELECT GeoFIPS, GeoName, Employer_contrib_govt_and_social_insurance  FROM `bigquery-public-data.sdoh_bea_cainc30.fips`  
where 
GeoName not LIKE '%FL'
LIMIT 100

SELECT GeoFIPS, GeoName, Percapita_personal_income  FROM `bigquery-public-data.sdoh_bea_cainc30.fips`  
where 
Percapita_personal_income between 20000 and 50000
order by 
Percapita_personal_income 
LIMIT 100 









