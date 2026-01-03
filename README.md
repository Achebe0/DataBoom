🌍 Climate-Aware Data Center Site Selection
Overview

This project builds a data-driven pipeline to evaluate and rank global cities for future data center suitability by considering real climate change data with geographic city data and a machine learning model.

The goal is not to predict the single “best” city with certainty, but to demonstrate how climate trends and infrastructure-related signals can be translated into a quantitative decision support system for long-term infrastructure planning.
AI is here to stay and as demands for Artificial Intelligence increase, we must consider the data centers that power this. Without an ideal location we may not be using it to its fullest extent or quite possibly make a poor investment choice!

Project Goals

Incorporate real climate data (CSV-based, NASA-style global climate records)

Aggregate climate signals into interpretable features (averages, trends, volatility)

Combine climate factors with location data from a global cities dataset

Train a machine learning model to produce a relative suitability score (0–100)

Rank cities based on predicted long-term data center suitability

Data Sources

climate.csv

Global land–ocean temperature records

Columns cleaned and converted to numeric form

Used to extract climate trends and volatility signals

worldcities.csv

Global city dataset with latitude and longitude

Used as the geographic basis for ranking candidate locations

Feature Engineering

The model uses a combination of:

Climate-Derived Features (from real data)

Average temperature

Long-term temperature trend (linear slope)

Temperature volatility

Infrastructure & Risk Proxies (explicit assumptions)

These are placeholders, clearly marked as proxies:

Energy cost index

Grid stability

Fiber connectivity score

Flood risk

Land cost index

These variables represent what real-world infrastructure data would replace in a production system.

Model

Architecture: Fully connected neural network (PyTorch)

Loss: Mean Squared Error (MSE)

Output: Suitability score normalized to 0–100

Scaling: Standardized inputs (StandardScaler)

The model is trained to learn relative rankings, not absolute ground truth.

Output

The system produces:

Model performance metrics (MSE, R²)

A ranked list of cities by predicted suitability score
