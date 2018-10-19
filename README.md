# Spark Word Count Sample with Swift in Java 
This java program reads a text file from Amazon S3 storage and 
counts the repetition of words by using Spark compute engine.

The computation part of Java code is from [Apache Spark](https://github.com/apache/spark) 
repository.

You have to put credentials and address of your S3 file in the code.

## Build and Create Package: 
```
mvn package
```

## Run the program 

You can use [ovh-spark-submit](https://github.com/mojtabaimani/ovh-spark-submit) to run the code 
in OVH data compute platform: 

```
$ ovh-spark-submit \
--token $TOKEN \
--class JavaWordCount \
--name WordCountSample \
--executor-memory 2G \
--total-executor-cores 4 \
sparkwordcount-1.0-SNAPSHOT-fat.jar
```
