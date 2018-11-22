# Spark Word Count Sample with Amazon S3 in Java 
This java program reads a text file from Amazon S3 storage and 
counts the repetition of words by using Spark compute engine. The s3a://irs-form-990/index_2011.csv is a public file in Amazon S3 for test. 

The computation part of Java code is from [Apache Spark](https://github.com/apache/spark) 
repository.

You have to put credentials and address of your S3 file in the code. You need to generate access key and secret key in you Amazon account dashboard. 

## Build and Create Package: 
```
mvn package
```

## Run the program 

You can use [ovh-spark-submit](https://github.com/mojtabaimani/ovh-spark-submit) to run the code 
in OVH data compute platform: 

```
$ source openrc.sh

$ ovh-spark-submit \
--class JavaWordCount \
--name WordCountSample \
--executor-memory 2G \
--total-executor-cores 4 \
sparkwordcount-1.0-SNAPSHOT-fat.jar
```

For running this jar file by using ovh-spark-submit in a cluster of spark, you need to use fat jar file (the jar file that has -fat at the end of the name), because all dependencies should be included in the jar file.
