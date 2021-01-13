# Introduction to Google BigQuery
This file contains text you can copy and paste for the examples in Cloud Academy's _Managing Your Google Cloud Infrastructure_ course.  

### Introduction
[Free GCP Trial](https://cloud.google.com/free) 

### Running a Query
```
SELECT *
FROM
 `bigquery-public-data.usa_names.usa_1910_2013`
ORDER BY number DESC LIMIT 10
```
```
SELECT *
FROM
 `bigquery-public-data.usa_names.usa_1910_2013`
WHERE gender = 'F'
ORDER BY number DESC LIMIT 10
```

### Loading Data
[Baby names data](http://www.ssa.gov/OACT/babynames/names.zip)  
[Jeopardy data](http://datascienceplus.com/wp-content/uploads/2015/08/JEOPARDY_CSV.csv)  
[Google Cloud SDK installation instructions](https://cloud.google.com/sdk/docs/install)
```
bq mk public
bq load --autodetect public.jeopardy JEOPARDY_CSV.csv
```

### Streaming Data
[BigQuery API documentation](https://cloud.google.com/bigquery/docs/reference/rest/v2/tabledata/insertAll)  

### Exporting Data
```
bq extract
```
```
gs://ca-example/games*.csv.gz
```

# Summary
[Bigquery documentation](https://cloud.google.com/bigquery/docs)  
support@cloudacademy.com  
