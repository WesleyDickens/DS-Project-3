# Optimizing Flu Shot Campaigns
## Overview
This project aims to optimize flu shot campaigns by identifying individuals less likely to receive a flu shot using data-driven models. By targeting traditionally under-vaccinated population segments, the project seeks to enhance the efficiency of marketing efforts for flu vaccination.

## Business and Data Understanding
### Stakeholder Audience
The primary stakeholders for this project include healthcare organizations, government bodies responsible for public health, and marketing teams focusing on health awareness campaigns.

### Dataset Choice
The dataset used in this project is from the United States CDC's National Center for Health Statistics, specifically the National 2009 H1N1 Flu Survey. This data was collected via phone calls and encompasses behavioral and demographic information pertinent to flu vaccination.

## Modeling
### Data Cleaning and Preparation
Our data cleaning consisted of removing columns related to H1N1 vaccines and awareness as they were not relevant to the analysis of Seasonal flu vaccines. 

To prepare the data we onehot-encoded the categorical/demographic variables. 

### Applied Models
#### K-Nearest Neighbors (KNN)
<p> Predictive accuracy: 53% </p>

Challenges: Lower generalization ability due to sensitivity to high-dimensional feature spaces and noise.

![knn](https://github.com/WesleyDickens/DS-Project-3/assets/8894178/fa8294e1-dfa9-4075-9ee9-db8da6bbf4fb)

#### Decision Tree
<p> Predictive accuracy: 76% </p>

Limitation: Tendency to overfit complex datasets, leading to poor generalization.

![tree](https://github.com/WesleyDickens/DS-Project-3/assets/8894178/b9c63071-7eb7-4fa2-aa56-967fadee876b)

#### Logistic Regression
<p> Initial accuracy: 77% with a 12% false positive rate. </p>

<p> Hyperparameter tuning: Utilized Grid Search with a C value of 1, L2 regularization, and Newton-CG solver. </p>
Tuned model accuracy: 78%.

![logistic](https://github.com/WesleyDickens/DS-Project-3/assets/8894178/09154eda-9fa5-4903-89ca-852e823b52c4)
![download (1)](https://github.com/WesleyDickens/DS-Project-3/assets/8894178/2c9ef218-2fe5-4063-ae67-522410c00701)
![download (2)](https://github.com/WesleyDickens/DS-Project-3/assets/8894178/2d6d1a4e-442d-4def-8f4f-47ce49e424bf)

## Evaluation
The Logistic Regression model, post-tuning, emerged as the most effective with a prediction accuracy of 78%. 

Notably, the most effective predictor for flu vaccination is a doctor's recommendation, while the most significant inverse predictor is age, with individuals aged 18-34 being less likely to be vaccinated.

<img width="490" alt="Screenshot 2024-01-26 at 11 00 06 AM" src="https://github.com/WesleyDickens/DS-Project-3/assets/8894178/139e373c-2648-4b80-8a6a-fb1b95976df5">


## Conclusion
The analysis and modeling efforts provide valuable insights into optimizing flu shot campaigns. The findings underscore the importance of doctor recommendations and highlight age as a critical factor in vaccination likelihood. These insights can guide targeted marketing strategies to increase flu vaccination rates, especially among younger demographics.

