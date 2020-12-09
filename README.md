# hfarm-clustering-longevityinsurance
The following projects test the theory that people with healthy eating habits, unlike those without them, tend to believe that they will live a long life. Therefore they are more likely to be concerned about their financial well-being during retirement, which increases the probability of them buying longevity insurance.

The dataset used is the Carrefour dataset obtainable at this URL https://github.com/ging/carrefour_basket_data_challenge which provides supermarket consumption data.

For a detailed explanation please read the report of the project.

Here are summarized to steps undertaken to test this theory:

* Categorization of Carrefour products into 38 categories, to reduce the dimensionality of the dataset.

* Grouping the dataset by customers using 2 different metrics:
  * Average consumption by category for each customer
  * Macronutrient composition of the average consumption by category for each customer
 
* Clustering customers via different techniques:
  * DBSCAN on Linear combinations of the average consumption by category for each customer
  * K-Means on the category by initializing cluster centroids
  * K-Means on the macronutrient composition
  * Gradient Descent to minimize difference in 'health score' between the healthy and the unhealthy cluster
 
* Testing of the theory by means of a survey which measures individuals' consumption behaviour and propensity to purchase longevity insurance
  * PDSLasso as a trade-off between consistency in parameters and prediction performance in a high k - low n scenario
  * Reducing omitted variable bias via Instrumental Variables
 
* Experiment proposition by applying a Logit Model.
