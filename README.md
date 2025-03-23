# StockOracle: AI-Powered Stock Prediction & Forecasting System

StockOracle is an integrated system that collects and analyzes stock market data, computes technical indicators, generates textual and sentiment insights, and applies topic modeling alongside forecasting techniques to provide comprehensive market analysis. The system is designed to support data-driven investment decisions through predictive modeling and natural language processing.

## Table of Contents
1. [Overview](#overview)
2. [Project Workflow](#project-workflow)
    - [Data Collection & Technical Indicator Calculation](#data-collection-&-technical-indicator-calculation)
    - [Textual and Sentiment Data Generation](#textual-and-sentiment-data-generation)
    - [Topic Modeling with BERTopic](#topic-modeling-with-bertopic)
    - [Sentiment Analysis and Forecasting](#sentiment-analysis-and-forecasting)
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
    - **Technical Indicators**: Calculated indicators such as SMA_50, SMA_200, and RSI using pandas_ta.