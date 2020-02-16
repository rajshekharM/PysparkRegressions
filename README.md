# PysparkRegressions
Pyspark
Using python and Google Colab notebooks , we can use APache Spark for Big Data Processing , similar to Python ML model examples

Some differences :

1.  Apache spark uses different kind of input data frames , for input data to model

2.  Need to give all input features not as seperate rows of a table or dataframe, but as a single vector - that is - all rows merged into a single spark.sql.dataframe type - using this command : 

featureassembler = VectorAssembler(inputCols=["Avg Session Length","Time on App","Time on Website","Length of Membership"],outputCol="Independent Features")

output = featureassembler.transform(dataset)

//where dataset is the csv --> dataframe converted table (actual dataset with all the header rows names)

3. Need to load Linearregressor or other ML models from pyspark library 

Eg : from pyspark.ml.regression import LinearRegression, RandomForestRegressor
