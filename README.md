# Call Center Optimization

The objective is to create a robust ML system leveraging call center data to enhance the efficacy of marketing campaigns targeting term deposit sales for a leading European banking institution. The strategy involves constructing an ML model capable of prioritizing customers based on their probability of responding positively to the term deposit offer. By generating a ranked list of prospects, the aim is to elevate the success rate by optimizing the ratio of successful sales to the total number of outreach attempts.

## Model Performance

## Notebooks Description

- **Data Preprocessing:**

The data preprocessing pipeline is designed for CSV-format data. It incorporates essential steps such as encoding categorical variables, handling missing values, and optimizing memory usage.

- **Exploratory Data Analysis:**

The dataset undergoes thorough examination, encompassing the analysis of variable distributions, scrutiny of outliers, and exploration of internal correlations.

- **Modeling:**

An ensemble of Random Forest Classifiers, called *Ecosystem Classifier*, is constructed using Bayesian optimization. Initially, a loss function is optimized using Bayesian techniques across a predefined number of runs. The chosen loss function prioritizes maximizing the F1 Score through cross-validation, with a focus on optimizing True outputs, thus employing Macro averaging. Throughout each optimization run, a Random Forest classifier is trained, and the best-performing parameters from each run are preserved. Subsequently, top-performing models are selected based on their cross-validation scores, serving as weights. Finally, an instance of the Ecosystem Classifier is constructed, encapsulating these selected models along with their respective weights.

- **Ecosystem Classifier:**

The EcosystemClassifier class, which serves as a voting classifier composed of Random Forests, is instantiated.

- **Model Evaluation:**

An analysis is carried out on the outcomes derived from testing the Ecosystem model. The primary aim of this model is to deliver a prioritized roster of potential customers for engagement in the marketing campaign, determined by their likelihood of subscribing to a term deposit. Evaluation is accomplished through lift curve and gain curve analyses.
