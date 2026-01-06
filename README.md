# flight-price-prediction

Project Overview

This project aims to predict flight ticket prices using machine learning techniques based on various flight-related features such as airline, source, destination, duration, stops, and journey date.

Flight ticket prices fluctuate due to multiple factors, making them difficult to estimate manually. By analyzing historical flight data, this project builds a data-driven predictive model that can estimate ticket prices accurately.

This project demonstrates a complete data science workflow, from raw data analysis to model evaluation.

Dataset Description

The dataset contains historical flight booking information with multiple attributes that influence ticket prices.

Target Variable:

Price → The final ticket price of the flight (in INR)

Input Features:

Each row represents a single flight with the following details:

Feature	Description
Airline	Name of the airline
Date_of_Journey	Date when the journey starts
Source	Departure city
Destination	Arrival city
Route	Flight route
Dep_Time	Departure time
Arrival_Time	Arrival time
Duration	Total travel time
Total_Stops	Number of stops
Additional_Info	Extra flight information

What This Dataset Tells Us

Flight prices are not fixed and depend on multiple variables.

Airline brand, number of stops, and journey date have a strong impact on price.

Non-stop flights are generally more expensive.

Ticket prices increase during peak travel seasons.

Machine learning models can effectively learn these patterns and predict prices.

Step-by-Step Explanation of the Notebook
Importing Required Libraries

All essential Python libraries are imported to handle data processing, visualization, and machine learning tasks.

Loading the Dataset

The dataset is loaded using Pandas, allowing structured access to rows and columns.

This step helps in:

Understanding dataset size

Checking column names

Inspecting data types

Exploratory Data Analysis (EDA)

EDA is performed to understand the data better:

Checking missing values

Understanding feature distributions

Identifying outliers

Studying price variations across airlines and routes

EDA helps us decide which features are important and how to preprocess them.

Data Cleaning & Feature Engineering

Since machine learning models require numerical data:

Date_of_Journey is split into day and month

Duration is converted into total minutes

Dep_Time & Arrival_Time are converted into hour and minute

Categorical features (Airline, Source, Destination) are converted using encoding

Unnecessary columns are removed

This step transforms raw data into model-ready format.

Feature Selection

Relevant features that directly impact flight prices are selected, while redundant or less useful columns are dropped.

Splitting the Dataset

The dataset is divided into:

Training data → Used to train the model

Testing data → Used to evaluate model performance

This ensures the model can generalize well to unseen data.

Model Building

A machine learning regression model is trained to:

Learn relationships between features

Predict flight prices accurately

Regression is chosen because price is a continuous numerical value.

Model Evaluation

The model is evaluated using performance metrics such as:

Mean Absolute Error (MAE)

Mean Squared Error (MSE)

R² Score

These metrics help measure prediction accuracy and reliability.
