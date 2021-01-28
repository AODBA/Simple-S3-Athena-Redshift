# Simple-S3-Athena-Redshift

Application/Pipeline used for easy discovery of data.

This will enable data analists a way to easy explore new datasources without dealing with the tech aspects of ingestion the data source into Athena or Redshift.


## System Architecture

![System Architecture](https://github.com/AODBA/Simple-S3-Athena-Redshift/blob/main/Simple-Athena-Redshift.png?raw=true "System Architecture")


I will be using python [AwsWrangler](https://aws-data-wrangler.readthedocs.io/en/stable/index.html) for most of the code base. 


## Use Cases:

Expose CSV file as a Athena/Redshift table with ease, the analist only need to upload the file/files to an s3 bucket.

### Provide Schema - a dict should be provided
eg: 
```
{
  "column_name_1": "data_type",
  "column_name_2": "data_type"
}
```
 If you have the schema in the format, you will need to upload it in the same folder path as the data files with as a `.schema`.
 
 Reffer to [Athena Data Types](https://docs.aws.amazon.com/athena/latest/ug/data-types.html) for designing the .schema file

### Infer Schema - default option if no `.schema` file is provided
When the schema is infered the data needs to have a Header so the column should reflect the actuall column names.
Also the data types will be generic.

Expose Parquet file as a Athena/Redshift table with ease, the analist only need to upload the file/files to an s3 bucket.

### Provide Schema - a dict should be provided
eg: 
```
{
  "column_name_1": "data_type",
  "column_name_2": "data_type"
}
```
If you have the schema in the format, you will need to upload it in the same folder path as the data files with as a `.schema`.

Reffer to [Athena Data Types](https://docs.aws.amazon.com/athena/latest/ug/data-types.html) for designing the .schema file

### Infer Schema - default option if no `.schema` file is provided
When the schema is infered the data needs to have a Header so the column should reflect the actuall column names. 
Also the data types will be generic.

