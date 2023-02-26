# iata-case-study
I have implemented a solution as per your requirements for that i have created 3 lambda functions cloudformation script with following details:
 
 ## Lambda Functions 
 * downloadCsvFile : Ingrate data from Http and Download it to S3 bucket.After downloading un-compressed it to s3 prefix raw and moving it prefix archive.
 * convertcsvtoparquet : Reading data from raw prefix and converting it to parquet with country partition.
 * triggergluecrawler : After writing data in partition we need to extract the metadata to query our data in athena .We have created a crawler using cloudformation.
 
 **All of lambda functions code is attached in ZIP format**
 
 ## Cloudformation 
  
 * S3 Bucket creation 
 * Role Definitions 
 * Lambda functions Definitions 
 * Glue Database creation 
 * Crawler creation 
 
 ** Currently i am facing issue on crawler creation my account don't have access to create a crawler and i already raised this issue with Support**
 

 ## How we can make it better  

 * Write this job in Spark to get the in-memory and fast processing edge because lambda have limited memory and execution time .
 * Need to define some orchestration process to execute this pipeline event base or schedule base. 
 * For Data quality we need to add some data quality checks after integration by using library like **Great Expectations**.
 * We need to add logging mechanism for tracking history by create a table.
 * We need to add some alert base notification if a job is failed by using SNS .
 
 

