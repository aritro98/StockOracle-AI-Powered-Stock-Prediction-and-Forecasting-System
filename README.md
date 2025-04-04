# StockOracle: AI-Powered Stock Prediction & Forecasting System

StockOracle is an integrated system that collects and analyzes stock market data, computes technical indicators, generates textual and sentiment insights, and applies topic modeling alongside forecasting techniques to provide comprehensive market analysis. The system is designed to support data-driven investment decisions through predictive modeling and natural language processing.

## Table of Contents
1. [Overview](#overview)
2. [Project Workflow](#project-workflow)
3. [Key Features](#key-features)
4. [Technologies Used](#technologies-used)
5. [Installation and Setup](#installation-and-setup)
6. [Usage](#usage)
7. [Results](#results)
8. [Future Scope](#future-scope)

## Overview
StockOracle integrates multiple modules to assist investors in making informed decisions:
- **Data Ingestion & Preprocessing**: Efficient extraction, cleaning, and structuring of raw stock data.
- **Trend Prediction**: Applies linear regression models to forecast short-term price movements and issue actionable recommendations.
- **Topic Modeling**: Applies BERTOPIC to analyze financial text data and extract prevailing themes or topics.
- **Forecasting**: Leverages Facebook's Prophet model to predict future stock trends over customizable periods.
- **Interactive Dashboard**: A web-based UI built with Dash and Plotly that displays historical data, predictions, and topic insights interactively.

## Project Workflow
- **Data Collection & Technical Indicator Calculation**
    - **Data Source**: Collected historical stock data for 10 companies using the yfinance library over 5 years (from `2020-01-17` to `2025-01-16`).
    - **Technical Indicators**: Calculated key indicators such as `SMA_50`, `SMA_200`, and `RSI` using pandas_ta.
    - **Dataset**: Processed data is saved in the CSV file `stock_data_5_years`.
    - **Implementation**: Documented in the `Stock_Trends.ipynb` notebook.
- **Textual and Sentiment Data Generation**
    - **Dataset Creation**: Generated textual descriptions and sentiment scores from the `stock_data_5_years` CSV file.
    - **Output**: The refined textual and sentiment data is stored in the CSV file `refined_textual_data`.
    - **Implementation**: Detailed in the `Textual_Data.ipynb` notebook.
- **Topic Modeling with BERTopic**
    - **Topic Representation**: Applied the BERTopic model on the `refined_textual_data` CSV to extract key topics.
    - **Insights & Visualization**: Insights are generated in the `Topic_Representation.ipynb` notebook and are visualized in `Topic_Visualization.html`.
- **Sentiment Analysis and Forecasting**
    - **Final Analysis**: Combines sentiment analysis with forecasting techniques to deliver actionable market insights.
    - **Implementation**: Managed by the `Sentiment_Analysis_and_Forecasting.py` script.

## Key Features
- **Comprehensive Data Collection**:
    - Fetches historical data for 10 companies.
    - Calculates technical indicators (SMA_50, SMA_200, RSI).
- **Data Preprocessing & Sentiment Extraction**:
    - Converts raw data into refined datasets.
    - Extracts sentiment from textual data for market mood analysis.
- **Advanced Topic Modeling**:
    - Uses BERTOPIC to uncover underlying themes in financial texts.
    - Provides visual insights on topic distribution.
- **Forecasting & Predictive Analysis**:
    - Applies forecasting techniques for long-term stock predictions.
    - Combines technical analysis with sentiment signals for recommendations.

## Technologies Used
- **Python**: Primary language for data analysis and application logic.
- **yfinance**: To collect historical stock market data.
- **pandas_ta**: For calculating technical indicators like SMA and RSI.
- **Pandas**: For data manipulation and preprocessing.
- **BERTopic**: For topic modeling and extraction of textual insights.
- **Prophet**: For time-series forecasting (integrated within the sentiment analysis script).
- **Jupyter Notebooks**: For step-by-step data processing.
- **Dash/Plotly**: For interactive dashboard visualizations.

## Installation and Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/StockOracle-AI-Powered-Stock-Prediction-and-Forecasting-System.git
   ```
2. Navigate to the project directory:
   ```bash
   cd StockOracle-AI-Powered-Stock-Prediction-and-Forecasting-System
   ```
3. Install Dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage
1. Data Processing and Indicator Calculation: Run `Stock_Trends.ipynb` in Jupyter Notebook to fetch data and compute technical indicators.
2. Textual Data Generation: Execute `Textual_Data.ipynb` to produce the `refined_textual_data` CSV containing textual and sentiment data.
3. Topic Modeling: Open and run `Topic_Representation.ipynb` to apply the BERTOPIC model and review the topic visualization in `Topic_Visualization.html`.
4. Sentiment Analysis & Forecasting: Run the final analysis script:
   ```bash
   python Sentiment_Analysis_and_Forecasting.py
   ```

## Results
- **Data Quality & Indicator Accuracy**:
    - Successfully collected and processed 5 years of stock data for 10 companies.
    - Computed reliable technical indicators (SMA_50, SMA_200, RSI) that correlate with market trends.
- **Textual and Sentiment Insights**:
    - Generated a refined textual dataset with corresponding sentiment scores.
    - Enhanced market analysis by combining numerical data with sentiment insights.
- **Effective Topic Modeling**:
    - BERTopic successfully identified key topics in financial texts.
    - Provided clear visualizations that reveal underlying market themes, contributing to deeper insight into market sentiment.
- **Robust Forecasting Performance**:
    - Forecasting techniques produced actionable predictions on future stock price trends.
    - Integration of sentiment analysis with forecasting yielded improved recommendation accuracy (BUY, SELL, HOLD).

## Contributors & Contributions
- Neeladri Bandopadhyay: Data Processing & Extraction
- Arito Dutta: Stock Trend Prediction
- Lopamudra Mukherjee: Stock Price Forecasting & Documentation
- Harsh Kumar Singh: Dashboard & Sentiment Analysis

## Future Scope
- Improved Forecasting: Explore advanced forecasting models for enhanced prediction accuracy.
- Real-Time Data Integration: Incorporate live data feeds for dynamic market analysis.
- Expanded Sentiment Analysis: Refine sentiment extraction to capture market moods more accurately.
- Dashboard Development: Build an interactive dashboard for comprehensive real-time visualization.
