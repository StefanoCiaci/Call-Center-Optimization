# Call Center Optimization

The goal is to develop a sophisticated ML framework that utilizes data from a leading European bank's call center to **boost the success of marketing campaigns** aimed at promoting term deposits. The core of this strategy is to build a ML model that effectively identifies customers most likely to accept a term deposit offer, thereby prioritizing them for contact. This prioritization process is designed to improve the efficiency of the marketing efforts by increasing the proportion of successful sales relative to the number of outreach attempts made.

## Model Performance

![Alt text](/Charts/lift_chart.png?raw=true)

The model has demonstrated a notable capability in distinguishing potential customers who are more inclined to subscribe to a term deposit, achieving over **16%** accuracy for the top 10% of prospects, with a peak accuracy of **25%**. This performance significantly surpasses the baseline success rate of **7%**.

![Alt text](/Charts/gain_chart.png?raw=true)

The model's deployment markedly enhances the efficiency of marketing outreach, boasting a **+150%** improvement in effectiveness within the top 10% tier of potential customers identified. Remarkably, by engaging with only **31%** of the prospect pool, the model ensures that **50%** of the possible term deposit subscriptions are captured.

The model exhibits a marked enhancement in performance compared to a conventional Random Forest Classifier. Specifically, it boosts the efficiency of customer identification within the top 20% segment of highly ranked prospects by an impressive **20%**. This improvement underscores the advanced model's superior capability in prioritizing potential customers more effectively than the simpler Random Forest approach, leading to a more strategic allocation of marketing efforts and resources.

An additional feature of this model is its feature importance analysis capability, which offers profound insights into the data and supports strategic decision-making. Notably, account balance is the most influential factor, contributing 45% to the model's decisions, followed by the customer's age, which accounts for 25%.

## Comprehensive Notebooks Overview

- **Data Preprocessing:**

This segment outlines the preprocessing routine for data in CSV format, which includes encoding categorical variables, addressing missing values, and enhancing memory efficiency.

- **Exploratory Data Analysis (EDA):**

EDA is conducted to thoroughly investigate the dataset, analyzing variable distributions, identifying outliers, and exploring correlations among variables.

- **Modeling:**

The model, dubbed the **Ecosystem Classifier**, is an ensemble of Random Forest Classifiers fine-tuned through Bayesian optimization. This process involves optimizing a loss function—focused on maximizing the F1 Score via cross-validation—for True predictions using Macro averaging. The highest-performing Random Forests are then compiled, with their cross-validation scores determining their weights in the final Ecosystem Classifier.

- **Ecosystem Classifier:**

This section introduces the EcosystemClassifier, a composite voting classifier built from selected Random Forest models, each weighted according to their performance.

- **Model Evaluation:**

The evaluation focuses on the model's ability to generate a ranked list of potential customers for the marketing campaign, based on their likelihood of subscribing to a term deposit. This is achieved through detailed analyses using lift and gain curves, showcasing the model's practical value in enhancing marketing success rates.
