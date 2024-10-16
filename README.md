# Big Data Analytics with Hadoop, MongoDB, and Apache Spark + Sentiment Analysis and Time Series Forecasting

## Project Overview

This project demonstrates the integration of Hadoop, MongoDB, and Apache Spark for handling large-scale data, including storage, processing, and machine learning techniques. The focus is on sentiment analysis and time-series forecasting using models such as ARIMA and LSTM.

## Key Components:

- **HDFS Storage**: Scalable and fault-tolerant storage using Hadoop Distributed File System (HDFS).
- **MongoDB Storage**: Flexible NoSQL database for managing semi-structured tweet data.
- **Apache Spark Processing**: In-memory processing with Spark SQL for querying large datasets.
- **SQL & Python Integration**: SQL for data cleaning and manipulation; Python for orchestration and advanced analytics.
- **Sentiment Analysis**: Preprocessing tweets to determine sentiment (positive, negative, neutral) for use in predictive models.
- **Time-Series Forecasting**: ARIMA and LSTM models for predicting sentiment trends over time.
- **YCSB Benchmarking**: Performance benchmarking of SQL and MongoDB databases using YCSB across different workloads.

## Notebooks:

This project is organized into three notebooks:

1. **Part 1 - Big Data (Terminal + SQL Queries), short EDA**: Initial data exploration, terminal-based commands, and basic exploratory data analysis (EDA).
2. **Part 2 - EDA, Preprocessing, and Sentiment Analysis**: Advanced EDA, text preprocessing, and sentiment analysis preparation.
3. **Part 3 - Time Series + Dashboard**: Time-series forecasting with ARIMA and LSTM models, along with dashboard visualizations following Tuftes’ principles.

## Data Preprocessing for Sentiment Analysis:

- **Text Cleaning**: Removed unnecessary characters and standardized the format of tweets.
- **Tokenization**: Text tokenized into individual words for analysis.
- **Stop Words Removal**: Removed uninformative words to improve sentiment analysis.
- **Lemmatization**: Reduced words to their base forms for consistency.
- **Sentiment Scores**: Assigned sentiment scores (positive, negative, or neutral) for use in time-series models.

These preprocessing steps ensured the dataset was clean, structured, and ready for machine learning models.

## Sentiment Analysis and Time Series Forecasting:

### Sentiment Analysis:

Sentiment analysis was performed on both raw and preprocessed tweet data to understand the emotions expressed. The sentiment scores enriched the dataset, facilitating the use of time-series models to forecast sentiment trends.

### Time-Series Forecasting:

### ARIMA Model:

- Applied to raw sentiment data to forecast future trends.
- Forecasted for multiple time periods (1-step, 3-step, 7-step, 28-step), showing stable sentiment patterns over time.
- Evaluated using RMSE, proving ARIMA’s effectiveness for short- to mid-term forecasts.

### LSTM Model:

- Trained on preprocessed text data, capturing long-term dependencies in sequential data.
- TF-IDF was used to vectorize text data for model training.
- The model was evaluated using loss and validation loss metrics, achieving consistently low error rates and strong generalization to unseen data.

**Forecasting Performance:**

- **1-day forecast**: Minor variations but overall consistency.
- **3-day forecast**: Slight fluctuations with patterns similar to 1-day forecasts.
- **7-day forecast**: Stable trends, demonstrating robustness over a week.
- **28-day forecast**: Stable with small fluctuations, showing effective long-term forecasting.

## YCSB Benchmarking Results:

- Comparative analysis of MySQL and MongoDB performance under different workloads (read-heavy, write-heavy, etc.).
- MongoDB exhibited better consistency under read-heavy workloads, while MySQL excelled in handling transactional queries.

## Dashboard:

The project includes a dashboard that adheres to **Tuftes’ principles** for effective data visualization:

- **Clarity**: Clear and labeled graphs present the forecast results.
- **Simplicity**: Focuses on key metrics like RMSE and essential visualizations without unnecessary elements.
- **Integrity**: Displays accurate and transparent results, showing both actual data and model forecasts alongside training performance.

## Usage:

- **Data Storage**: Use HDFS and MongoDB for data storage and Spark SQL with Python for querying and analysis.
- **Forecasting**: Implement ARIMA and LSTM models for sentiment trend forecasting, and tune models for better accuracy.

## Conclusion:

This project leverages Hadoop, MongoDB, and Apache Spark to create an efficient, scalable solution for big data storage, processing, and analysis. The application of sentiment analysis and time-series forecasting models (ARIMA and LSTM) demonstrates practical use cases of machine learning in understanding and predicting sentiment trends.

## Future Enhancements:

- Implement systematic hyperparameter tuning for ARIMA and LSTM models to optimize accuracy.
- Improve the dashboard with interactive features like tooltips and sliders for enhanced user experience.

## Installation and Setup:

### 1. Hadoop Setup:

- Initialize YARN and HDFS:
    
    ```bash
    bash
    Copy code
    start-yarn.sh
    start-dfs.sh
    
    ```
    
- Upload data to HDFS:
    
    ```bash
    bash
    Copy code
    hadoop fs -put [data.csv] /hdfs/path
    
    ```
    

### 2. MongoDB Setup:

- Start MongoDB server:
    
    ```bash
    bash
    Copy code
    mongod --bind_ip [IP]
    
    ```
    
- Import data into MongoDB:
    
    ```bash
    bash
    Copy code
    mongoimport --db [db_name] --collection [collection_name] --file [file.csv]
    
    ```
    

### 3. Apache Spark Setup:

- Set up Spark session for data processing:
    
    ```python
    python
    Copy code
    from pyspark.sql import SparkSession
    spark = SparkSession.builder.appName("App").getOrCreate()
    
    ```
    

### 4. Python Dependencies:

Install required Python libraries:

```bash
bash
Copy code
pip install pandas matplotlib pyspark pymongo

```

## References:

- Apache Hadoop Documentation
- MongoDB Manual
- Apache Spark Documentation
- Relevant papers on time-series forecasting and big data analytics
