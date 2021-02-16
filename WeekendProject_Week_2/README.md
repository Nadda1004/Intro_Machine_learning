# Mushroom Data set
### Group Members:
      - Nada Alzahrani
      - Abeer Alghamdi
      - Afrah Alharbi
![Mushroom](https://github.com/Nadda1004/Intro_Machine_learning/blob/main/WeekendProject_Week_2/mushroom_img.jpg?raw=true)

* Source: https://archive.ics.uci.edu/ml/datasets/Mushroom
    
## Steps we followed:
### Note:
   * There is 2 files:
      * Differences:
         * The first file (W2_D5_ML_Week2_Project_Dummies_Range.ipynb) map the columns values to a range (0 , length of values inside the columns)
         * The second file (W2_D5_ML-Week2-Project_Dummies_01.ipynb) map each value into columns and then (0,1)
      * Similarities: 
         * Changed every columns value from one letter to whole words so it can be more understanble
         * Split train set to 70% and test set to 30%
         * the second file (W2_D5_ML-Week2-Project_Dummies_01.ipynb) map each value into columns and then (0,1)
         * Models
      
#### the first file : W2_D5_ML_Week2_Project_Dummies_Range.ipynb (dummies column split in range)
  
##### Modeling
    1. Baseline Model
      - The values predicted for each observation was the most common value in the train set (which was edible)
      - The model scored 51.08%
    2. Logistic Regression
      - The model scored 95.25% before tuning
      - The model scored 95.97% after tuning with GridSearchCV (with the parameter: fit_intercept ,max_iter, penalty, solver)
      - The model scored 95.73% after tuning with RandomizedSearchCV (with the parameter: C, penalty)
    3. k-Nearest Neighbors
    - for more details about the confusion matrix and other metrics check the notebook 
###### To Conclude:
* The KNN model scored the highest and its FP and FN were the lowest rather than the other models

_____________________________________________________________________________________________________________

#### The Second file : W2_D5_ML_Week2_Project_Dummies_01.ipynb (dummies column split to 0 and 1)

##### Modeling 
     1. Baseline Model 
       -  The values predicted for each observation was the most common value in the train set (which was edible)
       -  The model scored 51.08%
     2. Logistic Regression
       - The model scored 99.98% before tuning 
       - The model scored 99.93% after tuning with GridSearchCV (with the parameter: fit_intercept ,max_iter, penalty, solver)
       - The model scored 100% after tuning with RandomizedSearchCV (with the parameter: C, penalty)
     3. k-Nearest Neighbors
       - The model scored 100%.
     - for more details about the confusion matrix and other metrics check the notebook  
###### To Conclude:
*  The KNN and Logistic Regression with RandomizedSearchCV models scored the highest and its FP and FN were the lowest rather than the other models 
