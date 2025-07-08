# Parking-Price-Optimization-
This repository contains a Google Colab notebook demonstrating a project focused on developing and comparing different dynamic pricing strategies for a parking lot. The goal is to explore how various factors can influence parking prices to optimize operations and revenue.

Project Overview
This project implements three distinct pricing models, ranging from simple rule-based approaches to a machine learning-driven prediction model. It showcases data loading, feature engineering, model development, and comprehensive visualization of pricing outputs.

Features
Data Preprocessing: Handles raw parking data, cleans it, and extracts relevant features like time of day and day of the week.

Three Pricing Models:

Model 1: Occupancy-Based Pricing.

Model 2: Demand-Based Pricing (incorporating queue length, traffic, and special events).

Model 3: Machine Learning (Linear Regression) Predicted Pricing.

Model Comparison: Visualizes and compares the pricing outputs of all three models over time.

Interactive Dashboard: A Panel-based dashboard to interactively explore each model's pricing trends.

Models Implemented
Model 1 (Occupancy-Based): A straightforward model where parking price is directly proportional to the current occupancy rate of the parking lot. Higher occupancy leads to higher prices.

Model 2 (Demand-Based): An enhanced model that considers not only occupancy but also external demand indicators such as queue length, nearby traffic conditions, and whether it's a special day. This allows for more dynamic pricing during peak demand periods.

Model 3 (Machine Learning Prediction): Utilizes a Linear Regression model trained on historical data to predict optimal parking prices. This model learns complex relationships between various features (occupancy, demand indicators, time, day of week) to provide nuanced price suggestions.

Technical Stack
Python: The core programming language.

Pandas: For data manipulation and analysis.

Scikit-learn: For building and training the Machine Learning model.

Panel & Bokeh: For creating interactive data visualizations and the comparison dashboard.

Pathway (Initial Intent): The project initially aimed to leverage Pathway for real-time streaming data processing, but due to environmental constraints (explained below), the final implementation uses a batch processing approach.

How to Run This Project
This project is designed to be run in Google Colab.

Open the Notebook:

Go to Google Colab.

Click on File -> Upload notebook and select the .ipynb file from this repository.

Prepare the Dataset:

Ensure the dataset.csv file is uploaded to your Colab environment (e.g., by dragging it into the Colab file browser, or mounting Google Drive if it's there). The notebook expects this file to be in the same directory.

Run All Cells:

Once the notebook is open, go to Runtime -> Restart and run all.

Allow all cells to execute completely. The notebook is designed to run from top to bottom without manual intervention.

View the Dashboard:

The final cell (Step 10) will attempt to display the interactive dashboard directly in the Colab output.

If the dashboard does not appear directly in Colab, it will be saved as an HTML file named parking_price_dashboard.html in your Colab environment.

To view it: Click the "Files" icon (folder icon) on the left sidebar in Colab, locate parking_price_dashboard.html, right-click, and select "Download". You can then open this downloaded HTML file in any web browser.

Important Note on Real-Time Processing
The initial vision for this project included a fully real-time, streaming data pipeline using the Pathway framework. However, during development in the Google Colab environment, I encountered persistent and unresolvable technical issues (e.g., AttributeErrors with core Pathway streaming functions like pw.map, pw.udf_from_sklearn, and pw.debug.subscribe, as well as pw.run() blocking subsequent cell execution).

To ensure the project's analytical objectives were met and the notebook remained fully executable and reproducible, the implementation for model calculations and visualizations was adapted to a batch processing approach using standard Pandas operations. While this means the data is processed when cells are run (rather than continuously streaming), the project successfully demonstrates the logic and comparative outputs of all dynamic pricing models. This adaptation ensures the entire notebook runs smoothly and showcases the complete work.

Project Structure
The Google Colab notebook is structured into logical steps:

Step 1: Environment Setup (installing libraries).

Step 2: Data Loading and Initial Cleaning.

Step 3: Pathway Setup (initial data loading, though later adapted).

Step 4: Model 1 Definition (Occupancy-Based).

Step 5: Model 1 Visualization.

Step 6: Model 2 Definition (Demand-Based).

Step 7: Model 2 Visualization.

Step 8: Model 3 (ML Model) Training and Prediction (batch mode).

Step 9: Comparison of All Three Models (single plot).

Step 10: Interactive Dashboard Creation (and HTML export).

Step 11: Project Conclusion and Key Takeaways.

Conclusion & Future Work
This project provides a solid foundation for dynamic parking price optimization. Future enhancements could include:

Real-world Data Integration: Connecting to live data sources (e.g., IoT sensors, traffic APIs).

Advanced ML Models: Exploring more sophisticated machine learning algorithms for price prediction.

Economic Evaluation: Simulating the impact of different pricing strategies on revenue and parking lot utilization.

Competitor Analysis: Incorporating competitor pricing data as a feature for more robust models.
