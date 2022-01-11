# Model_Competition_MIT-GOSSIS

#DATA Resources
patient health data from MIT’s GOSSIS (Global Open Source Severity
of Illness Score). This dataset was used in the 2020 Global Women in Data Science hackathon hosted by
Kaggle (https://www.kaggle.com/c/widsdatathon2020/overview).The dataset includes information about
more than 130,000 Intensive Care Unit (ICU) visits
(For details of the dataset, please read dictionary.)

# Project Goal
The goal is to build a model to predict patient survival given these ICU visit information.


# Modeling in Subgroups: One Model or Many?
Large data sets can include a variety of subgroups. The qualities of these subgroups may be quite different
from each other. Each subgroup may have a different relationship between the outcome and the predictors
in a supervised learning model. 

This raises a question of how to generate the best predictions. Some options
(among others) would include:
• One Model: All of the subgroups are aggregated into a single data set that is used to inform the
construction of a single model.
• Many Models: A separate model is constructed for each subgroup based upon the corresponding subset
of the overall data.

These differing approaches have their respective advantages and disadvantages:
• One Model: It is easier to build, use, revise, and maintain one model. A larger overall sample size can
be utilized. However, a single model will assume that each prediction’s association with the outcome
is similar across all of the subgroups.
• Many Models: Modeling within a subgroup can provide a customized estimate of the relationships
between the predictors and the outcome in that subgroup. This allows for differing effects across the
models. However, each subgroup’s model will necessarily be based on a smaller sample size. Developing,
using, and revising multiple models can also require substantially greater labor.

# Data Splitting
We randomly split our data into training & testing sets (80/20). For the One 
Model approach, you train & tune your model using the training set and predict on the testing set. For the
Many Models approach, you’ll split both your training set and testing set by subgroups, train & tune your
model using the subgroup training set only and predict on your subgroup testing set.


# Classification Approach
Each model will be used to classify whether a patient survived (hospital_death). The values returned will
either be:
• 1 (or TRUE): The patient survived.
• 0 (or FALSE): The patient did not survived.


# A Scoreboard
We display the results of experiments in a scoreboard of the following form:
The Modeling Type should include values that correspond to the algorithms you select in the 5 categories.
This table should be sorted in decreasing order of one of the proportion columns to display the best overall
prediction in the first row. Please round the results to a reasonable number of digits (e.g. 2, 3, or 4).
Depicting the table using the datatable function in the DT package will create a sortable HTML table.
Details


Resource: Columbia University_Applied Analytics_Machine Learning Course


