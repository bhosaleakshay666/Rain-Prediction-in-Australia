# RAIN IN AUSTRALIA

```
Data Science Engineering Methods

Ashay Kanade 
Akshay Bhosale

```

# Problem Statement

### The Australian Continent is known for it’s beautiful beaches, diverse flora and

### fauna, and natural wonders like the Great Barrier Reef, among others. But a lot of

### people do not know about the tumultuous topography and jagged landforms,

### which make it extremely hard to define seasons and predict the weather, especially

### rainfall.


# Introduction

```
Australia’s exceptional aridity is the result of a unique combination of factors. Cold
ocean currents off the west coast means there is little evaporation to form rain clouds,
while the Great Dividing Range that runs down Australia’s east coast prevents rain from
penetrating far inland. There are few mountains to force air upwards where it can cool
into rain, and the region is dominated by the subtropical high-pressure belt that both
warms and dries the air. What’s more, the continent is extremely susceptible to the El
Niño–Southern Oscillation, a heating or cooling of the Pacific Ocean that can bring
prolonged periods of high temperatures and drought.
We will try to answer the question of whether or not it will rain tomorrow in Australia. We
implemented kNN, Decision tree, Random Forest with Python and Scikit-Learn.
We have used the Rain in Australia dataset for this project.
```

# The Dataset – Rain in Australia

```
This dataset contains about 10 years of
daily weather observations from many
locations across Australia. RainTomorrow
is the target variable to predict. It means --
did it rain the next day, Yes or No?
This column is Yes if the rain for that day
was 1mm or more.
```

# Preprocessing the Dataset – Our

# Approach

```
We have taken the following steps for preprocessing on
our selected dataset :-
```
**1. Finding Missing Values:**
We have used mode values to impute categorical
variables, and for numeric variables, we have used simple
imputers, iterative imputation as well as knn imputation
to fill in the missing values.
**2. Finding Outliers:**
Firstly we used the Describe() function to find variables
where we were able to see the differences in the Quartile
Ranges. For finding the appropriate upper value we used
Statistical Formula which was : Upper fence = Q3 + (1.5 *
IQR). Using this formula we procured the upper fence
values for above mentioned variables. We redefined the
maximum values as the upper fence.


# Preprocessing(Contd.)

**3. Sampling the Dataset:**

We sampled the data set as we found out that the target
variable was imbalanced.

**4. Dummy Variables:**

There were five categorical variables excluding target
variables so we decided to make these dummy variable
columns. We calculated the frequencies of these categorical
variables and introduced them as unique columns in the
dataset.

**5. Scaling the Dataset:**
Differences in the scales across input variables may increase
the difficulty of the problem being modeled. So we scaled the
dataset to make it more stable and machine friendly to use.


# Training Models Used

## We have used 4 types of training models namely :

- **KNN Model**

### -DNN Model

### -Decision Tree

### -Random Forest


# KNN Model and it’s Inference
```
- Even though KNN being the simplest model of them all, it consumed a huge
    amount of time as well as power. So we would **not** recommend you to use KNN
    for such a big dataset.
- Accuracy on test set : **79.79%**
```

# DNN Model and it’s Inference
```
DNN being one of the most sophisticated of them all, it
consumed a lot of computing power even though we
executed it on Google Colab.

When the epoch was set for **110** and batch size was **5** , we
observed that after the 36th epoch the validation accuracy
was going below **1%** therefore we discontinued the
execution.

Then, we tuned the hyperparameter of the epoch and set
it to **22** and increased the batch size to **7** which gave us
the accuracy **77.55%** on the test set.
```

# Decision Tree Model and it’s Inference

```
We observed that the decision tree was second optimal
after random forest with the parameters max_depth =
16 and max_features = sqrt. We achieved an
accuracy of 78.67% & 80.63% on two differently
imputed test sets.
```

# Random Forest Model and it’s Inference

```
Random forest was the most robust and quickest of them all
with the highest accuracy rate of 85.36% and 86.3% on two
differently imputed test sets. Using this we were also able to
derive important features looking at which we dropped the
least important of them and achieved an accuracy of 89.12%
with the model which was trained just on most important
features.
```

# Conclusion and Future Scope

### From the aforementioned results achieved , we conclude that the best results are

### given by the Random Forest Model with an accuracy going as much as 89.12%

### when trained on the most important features.

```
After using above mentioned models we constructed that the humidity, sunshine & cloud
covered at 3pm plays an important role for predicting the rainfall in Australia over different
regions depending on wind gust speed, evaporation and min/max temperature highly
correlating with wind direction.
```

# THANK YOU!


