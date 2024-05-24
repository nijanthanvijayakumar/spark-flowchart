# Handling Unexpected Null Values in Columns

## I have null values in columns that should not have null values

When working with Apache Spark, it's important to understand that Spark allows null values in columns that are defined in the schema to not contain nulls. This behavior is due to Spark not enforcing nullability and not performing any checks on that. 

A column’s nullable characteristic is essentially a contract with the Catalyst Optimizer that null data will not be produced. However, this does not prevent null values from being present in these columns. It's a healthy practice to always set a column's nullable property to true if there is any doubt about the presence of null values.

For additional context and solutions regarding handling unexpected null values in columns, consider the following resources:

- Apache Spark code related to nullability: [Spark SQL StructType](https://github.com/apache/spark/blob/v2.1.0/sql/catalyst/src/main/scala/org/apache/spark/sql/types/StructType.scala#L379-L386)
- A Medium blog post discussing Apache Spark, Parquet, and troublesome nulls: [Apache Spark Parquet and Troublesome Nulls](https://medium.com/@weshoffman/apache-spark-parquet-and-troublesome-nulls-28712b06f836)
