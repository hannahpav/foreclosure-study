# Classification Methods for Predicting and Understanding Factors of Housing Foreclosures in India
## Abstract

This report explores different methods to predict foreclosure on bank loans. This is done by fitting the available data on this subject to 7 model types: decision trees, random forests, boosted trees, logistic regression, K - nearest neighbors, neural networks and support vector machines. The optimal variables used to predict foreclosure are investigated to have less complex model building, and also to achieve better interpretability for the overall model. The final models are compared using their average accuracies and sensitivities using the respective variances of these values in order to determine which one would perform the best on the dataset. However, no definitive answer was found because there were a lower amount of computational resources available than were needed for this (more iterations on the models would need to be done). Therefore, based on the t-test, four top models, rather than a full ranking of models, were decided on: decision trees, partial data logistic regression, partial data SVM and full data SVM models. The SVM model with all data is performing statistically better than the other, but is found undesirable due to high training times and lots of data needed. Based on this, the decision trees and partial data logistic regression models are recommended because of high interpretability and low amount of data needed. The 5 predictors used for the partial data models are: Product, Paid interest, EMI due amount, EMI received amount and Current Interest Rate Minimum. These where found to have the most predictive value and thus it is also recommended to use these predictors to simplify the models. 

[Final Report](https://github.com/hannahpav/foreclosure-study/blob/main/House%20Foreclosure%20Final%20Report.pdf)

## Introduction
The NBFC Loan Transaction dataset contains information regarding foreclosures in India. When a buyer cannot repay their mortgage, the mortgage goes into foreclosure, giving the bank license to sell the home and recoup their loss.

The foreclosure process is difficult for the buyer, who is losing their home, and the bank, who must use their resources to auction the house.

The purpose of this project is to use the 'Foreclosure Prediction of Financial Dataset' to minimize the foreclosure rate. Classification Models are built to accurately predict foreclosure based on the whole dataset and selected variables. The project is also meant to understand what the factors are, and how to explain to the buyer how high their risk of foreclosure is. A model which sacrifices accuracy for interpretability would meet this challenge.

The main research questions therefore are: 
1.  What does the bank need to be aware of to detect risk of the client going into foreclosure?
2.  How can we use as few variables as possible while maintaining an accurate model? The model should use as few variables as possible, because high dimensionality adds complexity for the bank employee needing to interpret the results. The model also becomes more fragile because this data will be needed at each moment for evaluation
3.  How can we build the most sensitive model to capture more loans in risk of foreclosure at the expense of selecting loans that may not be at risk?

To answer these questions the 'Foreclosure Prediction of Financial Dataset' was used \cite{Kaggle}. To increase interpretability variable selection is performed to determine which variables are the most impactful. A multitude of classification models where fitted to determine the right trade-off between complexity and interpretability, the models fitted are:

1. Decision-trees
2. Random-Forest
3. Boosted Trees
4. Logistic Regression
5. K-nearest neighbours
6. Neural networks
7. Support vector machines
   
Furthermore, principal component analysis is performed to see if this would increase the accuracy or sensitivity of the model. Generally, the model's quality is determined by its sensitivity because the impact of going to foreclosure outweighs the risk of a false positive. It is less trouble to do some additional research based on the model compared to not perceiving a loan as risky and then going to foreclosure.
