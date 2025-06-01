# LLM-Based-Code-Generation-on-Energy-Dataset

Author: Shivam Pal

LLM Used: Groq API Integration

Dataset: UCI Household Power Consumption Dataset

Completion Date: 1 June 2025

## Project Overview
This project demonstrates the effective use of Large Language Models for automated code generation in data analysis tasks. Using natural language queries, we generate pandas code to analyze real-world energy consumption data and extract meaningful insights.

## Objectives
- Convert natural language queries into executable pandas code using LLMs
- Analyze household energy consumption patterns
- Generate data visualizations and statistical insights
- Demonstrate best practices for LLM-assisted programming

## Dataset
Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption)

Description: This dataset contains measurements of electric power consumption in one household with a one-minute sampling rate over a period of almost 4 years.

## Setup Instructions

```
pip install pandas numpy matplotlib seaborn jupyter
```

## Example LLM Interaction
Natural Language Query: "Find the average voltage for each day of the first week of February 2007?"

LLM Generated Code:
```
# Filter data for February 2007
feb_2007 = df[(df.index >= '2007-02-01') & (df.index < '2007-03-01')]

# Filter data for the first week of February 2007
first_week_feb_2007 = feb_2007[(feb_2007.index.dayofweek < 7) & (feb_2007.index.day <= 7)]

# Group by day and calculate average voltage
avg_voltage_per_day = first_week_feb_2007['Voltage'].resample('D').mean()

print(avg_voltage_per_day)

```
