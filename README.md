# Robert Meza
## Module 11: Practical Application 2

Link: [PA2.ipynb](PA2.ipynb)

Note: As instructed during office hours, the CSV file has not been uploaded directly to GitHub due to its size (>50MB). Instead, a direct link to the dataset has been included in the Jupyter Notebook for reference and access. The program has been tested and runs without any errors.

### Problem Statement

To efficiently and competitively price used cars from a dataset of approximately 420K entries, I will use data analysis tools to identify the most relevant features among the 18 available and select the most effective predictive model for estimating price. Since the goal is to predict a single continuous outcome, and based on the lectures and course content up to Module 10, my analysis will focus on regression-based models.

### Data Cleaning

I will perform the following steps to review the dataset’s columns/features and note any data quality concerns:
- Identify missing or null values in features
- Detect and remove duplicate rows
- Identify and assess outliers
- Convert data types as needed for analysis
- Remove irrelevant or redundant features

### Data Analysis

The dataset contains 426,880 entries of used car sales and 18 features describing each car, such as fuel type, transmission, and more. Based on my experience and knowledge of the used car market, I anticipate the following features will have the greatest influence on the model:
- Year
- Odometer
- Manufacturer
- State

### Evaluation

After completing Practical Application 2, I developed six models, progressing from a single feature to multiple features. In retrospect, the maximum number of features I incorporated was seven. I would like to investigate the impact on MSE when using a larger set of features.

For instance, while analyzing the manufacturer variable, I identified over forty unique values. Rather than creating one hot encoding for each category, I opted to assign a single popular variable, similar to the lecture example where day of the week was converted into binary form. I would apply a similar approach to the state variable in future iterations.

I was somewhat disappointed by the high MSE values produced by my models. Because vehicle prices are measured in the thousands, and the models were not well fitted, squaring the residuals resulted in very large error values. This reinforces my belief that incorporating additional features or segmenting the dataset by manufacturer could 
improve model performance.

A significant portion of my time was dedicated to data cleaning and preparation. I filtered the dataset to include vehicles priced between two thousand five hundred and one hundred fifty thousand dollars, which helped remove salvage vehicles and extreme outliers. Additionally, I limited the model to cars manufactured between 1980 and 2020 to exclude the period impacted by COVID related disruptions in vehicle sales.

Ultimately, I reduced the dataset to four key variables: year or age, odometer, manufacturer, and price. However, I suspect that these features alone were insufficient to accurately predict prices or achieve a satisfactory MSE. 

