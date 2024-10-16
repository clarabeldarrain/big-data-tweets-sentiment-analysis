# Big Data Analytics with Hadoop, MongoDB, and Apache Spark

## Project Overview
This project demonstrates the use of Hadoop, MongoDB, and Apache Spark for handling large-scale data, integrating storage, processing, and machine learning techniques. We explore big data management, data preprocessing, and time-series forecasting models such as ARIMA and LSTM for sentiment analysis.

## Key Components:
1. **HDFS Storage**: Utilizes Hadoop Distributed File System (HDFS) for scalable and fault-tolerant data storage.
2. **MongoDB Storage**: Uses MongoDB as a NoSQL database for handling semi-structured data, such as tweets, allowing for efficient querying and flexible data management.
3. **Apache Spark Processing**: Implements Apache Spark for in-memory processing, utilizing Spark SQL for querying large datasets.
4. **SQL & Python Integration**: SQL is used for data cleaning and manipulation, while Python handles orchestration between Hadoop, MongoDB, and Apache Spark, as well as advanced data analytics.
5. **Time-Series Forecasting**: Includes both ARIMA and LSTM models to forecast sentiment trends over time, providing insights into future sentiment fluctuations.
6. **YCSB Benchmarking**: Benchmarking SQL and MongoDB databases using YCSB to compare performance under different workloads.

## Project Structure:
- **Data Storage**: Efficient storage using HDFS and MongoDB for structured and semi-structured data.
- **Data Processing**: Processing and querying with Apache Spark and Spark SQL.
- **Machine Learning Models**: ARIMA and LSTM models implemented for time-series sentiment forecasting.
- **Benchmarking**: Performance comparison of SQL and NoSQL databases using YCSB.

## Usage:
- **Data Storage**: 
  - Store data using HDFS and MongoDB.
  - Query and process data using Spark SQL and Python scripts.
  
- **Forecasting**:
  - Implement ARIMA and LSTM models for time-series sentiment forecasting.
  - Tune models using hyperparameters for improved accuracy.

## YCSB Benchmarking Results:
- Detailed comparison of MySQL and MongoDB performance under varying workloads (e.g., read-heavy, write-heavy) using YCSB. MongoDB demonstrated better consistency, especially under read-heavy workloads, while MySQL excelled in transactional queries.

## Dashboard:
- Follows Tuftes’ principles to present clear, simple, and effective visualizations of the forecasting results and model performance.

## Conclusion:
This project combines powerful big data technologies to provide an efficient and scalable solution for data storage, processing, and analysis. The application of machine learning models to sentiment analysis showcases the practical use of these tools in forecasting and data-driven decision-making.

## Future Enhancements:
- Implement hyperparameter tuning for ARIMA and LSTM models.
- Optimize dashboard visualizations with interactive features.

## Installation and Setup:
1. **Hadoop Setup**: 
   - Initialize YARN and HDFS with `start-yarn.sh` and `start-dfs.sh`.
   - Upload data to HDFS using `hadoop fs -put`.
   
2. **MongoDB Setup**:
   - Start the MongoDB server with `mongod --bind_ip`.
   - Import data into MongoDB collections using the `mongoimport` command.

3. **Apache Spark**:
   - Set up Spark and use `SparkSession` for processing data.

4. **Python Dependencies**:
   - Install Python libraries:
     ```bash
     pip install pandas matplotlib pyspark pymongo
     ```

## References:
- Apache Hadoop, MongoDB, Apache Spark Documentation
- Relevant academic papers on time-series forecasting and big data analytics
