# Mushroom Data set
![Mushroom](https://github.com/Nadda1004/Intro_Machine_learning/blob/main/WeekendProject_Week_2/mushroom_img.jpg?raw=true)

* Source: https://archive.ics.uci.edu/ml/datasets/Mushroom
* Dictonary :
    * This data set includes descriptions of hypothetical samples
    corresponding to 23 species of gilled mushrooms in the Agaricus and
    Lepiota Family (pp. 500-525).  Each species is identified as
    definitely edible, definitely poisonous, or of unknown edibility and
    not recommended.  This latter class was combined with the poisonous
    one.  The Guide clearly states that there is no simple rule for
    determining the edibility of a mushroom; no rule like ``leaflets
    three, let it be'' for Poisonous Oak and Ivy.
    
     * Number of Instances: 8124 , Number of Attributes: 22 (all nominally valued): 
         * cap-shape:                bell=b,conical=c,convex=x,flat=f,
                                      knobbed=k,sunken=s
         *  cap-surface:              fibrous=f,grooves=g,scaly=y,smooth=s
         *  cap-color:                brown=n,buff=b,cinnamon=c,gray=g,green=r,
                                      pink=p,purple=u,red=e,white=w,yellow=y
         * bruises?:                 bruises=t,no=f
         * odor:                     almond=a,anise=l,creosote=c,fishy=y,foul=f,
                                      musty=m,none=n,pungent=p,spicy=s
         * gill-attachment:          attached=a,descending=d,free=f,notched=n
         * gill-spacing:             close=c,crowded=w,distant=d
         * gill-size:                broad=b,narrow=n
         * gill-color:               black=k,brown=n,buff=b,chocolate=h,gray=g,
                                      green=r,orange=o,pink=p,purple=u,red=e,
                                      white=w,yellow=y
        * stalk-shape:              enlarging=e,tapering=t
        * stalk-root:               bulbous=b,club=c,cup=u,equal=e,
                                      rhizomorphs=z,rooted=r,missing=?
        * stalk-surface-above-ring: fibrous=f,scaly=y,silky=k,smooth=s
        * stalk-surface-below-ring: fibrous=f,scaly=y,silky=k,smooth=s
        * stalk-color-above-ring:   brown=n,buff=b,cinnamon=c,gray=g,orange=o,
                                      pink=p,red=e,white=w,yellow=y
        * stalk-color-below-ring:   brown=n,buff=b,cinnamon=c,gray=g,orange=o,
                                      pink=p,red=e,white=w,yellow=y
        * veil-type:                partial=p,universal=u
        * veil-color:               brown=n,orange=o,white=w,yellow=y
        * ring-number:              none=n,one=o,two=t
        * ring-type:                cobwebby=c,evanescent=e,flaring=f,large=l,
                                      none=n,pendant=p,sheathing=s,zone=z
        * spore-print-color:        black=k,brown=n,buff=b,chocolate=h,green=r,
                                      orange=o,purple=u,white=w,yellow=y
        * population:               abundant=a,clustered=c,numerous=n,
                                      scattered=s,several=v,solitary=y
        * habitat:                  grasses=g,leaves=l,meadows=m,paths=p,
                                      urban=u,waste=w,woods=d

  * Class Distribution: 
    --    edible: 4208 (51.8%)
    -- poisonous: 3916 (48.2%)
    --     total: 8124 instances
    
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
      * The values predicted for each observation was the most common value in the train set (which was edible)
      * The model scored 51.08%
    2. Logistic Regression
      * The model scored 95.25% before tuning
      * The model scored 95.97% after tuning with GridSearchCV (with the parameter: fit_intercept ,max_iter, penalty, solver)
      * The model scored 95.73% after tuning with RandomizedSearchCV (with the parameter: C, penalty)
    3. k-Nearest Neighbors
    * for more details about the confusion matrix and other metrics check the notebook 
###### To Conclude:
* The KNN model scored the highest and its FP and FN were the lowest rather than the other models

_____________________________________________________________________________________________________________

#### The Second file : W2_D5_ML_Week2_Project_Dummies_01.ipynb (dummies column split to 0 and 1)

##### Modeling 
     1. Baseline Model 
       *  The values predicted for each observation was the most common value in the train set (which was edible)
       *  The model scored 51.08%
     2. Logistic Regression
       * The model scored 99.98% before tuning 
       * The model scored 99.93% after tuning with GridSearchCV (with the parameter: fit_intercept ,max_iter, penalty, solver)
       * The model scored 100% after tuning with RandomizedSearchCV (with the parameter: C, penalty)
     3. **k-Nearest Neighbors**
       * The model scored 100%.
     * for more details about the confusion matrix and other metrics check the notebook  
###### To Conclude:
*  The KNN and Logistic Regression with RandomizedSearchCV models scored the highest and its FP and FN were the lowest rather than the other models 
