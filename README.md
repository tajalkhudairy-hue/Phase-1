# Phase 1 – Data Cleaning (Ames Housing Dataset)

In this phase, I started working with the **Ames Housing dataset**, which contains information about house sales and their features.

First, I loaded the dataset using **pandas** and explored the data to understand its structure. I checked the first few rows, the number of rows and columns, and the data types of each column.

Then I analyzed the dataset to identify:

* Missing values
* Duplicate rows
* Basic descriptive statistics

After exploring the dataset, I focused on cleaning the data. I converted some columns such as **PID** and **MS SubClass** to strings because they represent identifiers or categories rather than numerical values.

Next, I handled missing values by:

* Filling numerical columns with the **median**
* Filling categorical columns with **"None"**

I also removed duplicate rows to ensure the dataset does not contain repeated records.

Since the target column in this dataset is **SalePrice**, I handled outliers by capping the values at the **99th percentile**. This helps reduce the effect of extreme values without removing the data completely.

Finally, I created a function called **clean_data()** that performs all the cleaning steps and includes simple checks to verify that:

* SalePrice has no missing values
* There are no duplicate rows
* The minimum sale price value is reasonable

This cleaned dataset will be used in the next phases for feature engineering and data analysis.
