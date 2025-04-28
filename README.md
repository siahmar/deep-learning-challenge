# Deep-learning-challenge 

### Background

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

* **EIN** and  **NAME** —Identification columns
* **APPLICATION_TYPE** —Alphabet Soup application type
* **AFFILIATION** —Affiliated sector of industry
* **CLASSIFICATION** —Government organization classification
* **USE_CASE** —Use case for funding
* **ORGANIZATION** —Organization type
* **STATUS** —Active status
* **INCOME_AMT** —Income classification
* **SPECIAL_CONSIDERATIONS** —Special considerations for application
* **ASK_AMT** —Funding amount requested
* **IS_SUCCESSFUL** —Was the money used effectively

### Before You Begin

1. Create a new repository for this project called `deep-learning-challenge`.  **Do not add this Challenge to an existing repository** .
2. Clone the new repository to your computer.
3. Inside your local git repository, create a directory for the Deep Learning Challenge.
4. Push the above changes to GitHub.

## Report on the Neural Network Model

1. **Overview** of the analysis: Explain the purpose of this analysis.

   *The purpose of this project is to develop a binary classification tool for the nonprofit foundation Alphabet Soup to identify funding applicants with the highest likelihood of success in their ventures. Leveraging machine learning and neural networks, the tool will analyze features from the provided dataset to predict the potential success of applicants, enabling data-driven decisions to optimize funding outcomes.*
2. **Results** : Using bulleted lists and images to support your answers, address the following questions:

* Data Preprocessing
  * What variable(s) are the target(s) for your model?
    * *The target variable (y) was set as `IS_SUCCESSFUL` column*
  * What variable(s) are the features for your model?
    * *The following columns were the features of the model: `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `INCOME_AMT`, `ASK_AMT`*
  * What variable(s) should be removed from the input data because they are neither targets nor features?
    * `EIN` and `NAME` columns were removed in both the oringinal model and optimized model
    * `EIN`, `NAME`, `STATUS` and `SPECIAL_CONSIDERATIONS` were removed from the optimized model to see if accuracy could be improved
* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
    * For the optimization model, in the first attempt 3 hidden layers were used with 150 neurons in the first layer, 50 in the second and 10 in the third. In the third attempt both the number of neurons and layers were increased, where 500 neurons was used in the first and second hidden layers, 250 in the third and 100 in the fourth hidden layer.
      * A modest number of neurons was used to avoid underfitting or overfitting the data, but increasing the number of neurons and layers did not improve the accuracy of the model.
    * A combination of different non-linear activation functions were employed
  * Were you able to achieve the target model performance?
    * No a target model accuracy of >75% was not achieved
  * What steps did you take in your attempts to increase model performance?
    1. The number of variables was reduced
    2. Extra hidden layers were used
    3. More neurons were used at each layer
    4. Different activation functions were used

3. **Summary** : Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.

* In summary, the current model achieves a moderate accuracy of 72.7% and shows room for improvement, particularly as indicated by a relatively high loss of 56%. To address these limitations, a Random Forest model could be used as an alternative, as it performs well on classification problems with imbalanced data due to its ensemble approach. Additionally, TensorFlow 2.0's tools for hyperparameter tuning could help optimize neural network models by finding the best architecture and parameters. This combination would enhance the classification results and enable more confident data-driven decisions.
