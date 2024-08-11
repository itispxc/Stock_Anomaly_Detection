# Anomaly Detection in Stock Prices using Unsupervised Learning

This project demonstrates the application of unsupervised learning techniques to detect anomalies in stock price data. The goal is to identify unusual price movements or patterns that could indicate potential trading opportunities or risk factors.

## Table of Contents

- [Introduction](#introduction)
- [Data](#data)
- [Methodology](#methodology)
    - [Feature Engineering](#feature-engineering)
    - [Anomaly Detection Algorithms](#anomaly-detection-algorithms)
- [Results](#results)
- [Usage](#usage)
- [Requirements](#requirements)

## Introduction

Anomaly detection is crucial in financial markets for identifying unusual trading activities, potential market manipulation, or emerging trends. This project utilizes three unsupervised learning algorithms:

- Isolation Forest
- One-Class SVM
- Autoencoders

## Data

The project uses historical stock price data for Apple Inc. (AAPL) fetched using the `yfinance` library. The data includes daily closing prices, volume, and other relevant features for the past year.

## Methodology

### Feature Engineering

- Moving Averages (MA10, MA50): Calculated to capture short-term and long-term price trends.
- Relative Strength Index (RSI):  A momentum indicator that measures the magnitude of recent price changes to evaluate overbought or oversold conditions.

### Anomaly Detection Algorithms

- **Isolation Forest:** Isolates anomalies by randomly selecting features and partitioning the data, assuming anomalies are easier to isolate.
- **One-Class SVM:**  Learns a boundary around "normal" data points and identifies data points falling outside this boundary as anomalies.
- **Autoencoders:** Neural networks trained to reconstruct input data. Anomalies are detected by identifying instances where the reconstruction error is high.

## Results

The project outputs the average percentage change in stock price one day after the detected anomalies for each algorithm. The results are printed to the console.

A plot visualizing the closing prices and the detected anomalies is also generated.

## Usage

1. Ensure you have the required libraries installed 
2. Run the Python script. 
3. The script will download data, train the models, and output the results.

## Requirements

- Python 3.7+
- yfinance
- numpy
- pandas
- matplotlib
- scikit-learn
- tensorflow
