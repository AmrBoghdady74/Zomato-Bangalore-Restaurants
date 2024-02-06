# Zomato-Bangalore-Restaurants Analysis and Model Deployment

## Introduction
The Zomato-Bangalore-Restaurants dataset provides insights into various factors affecting the establishment and popularity of different types of restaurants in Bangalore. In this project, we conduct exploratory data analysis (EDA) to understand trends in restaurant offerings, cuisines, pricing, and location concentrations. Additionally, we develop machine learning models to predict restaurant performance based on the dataset attributes. Finally, we deploy our best-performing model using Streamlit, allowing users to interactively explore predictions and insights.

## Data Description
The dataset consists of several features that describe different aspects of restaurants in Bangalore:

* **url:** URL of the restaurant on the Zomato website
* **address:** Address of the restaurant in Bengaluru
* **name:** Name of the restaurant
* **online_order:** Availability of online ordering
* **book_table:** Availability of table booking
* **rate:** Overall rating of the restaurant out of 5
* **votes:** Total number of ratings for the restaurant
* **phone:** Phone number of the restaurant
* **location:** Neighborhood where the restaurant is situated
* **rest_type:** Type of restaurant
* **dish_liked:** Dishes liked by customers
* **cuisines:** Food styles offered, separated by commas
* **approx_cost(for two people):** Approximate cost for a meal for two people
* **reviews_list:** List of tuples containing ratings and reviews by customers
* **menu_item:** List of menus available in the restaurant
* **listed_in(type):** Type of meal offered
* **listed_in(city):** Neighborhood where the restaurant is listed

## Exploratory Data Analysis (EDA)
1. **Popular Voted Restaurants:** Identifying the most popular restaurants based on votes.
2. **Top 10 Cuisines:** Determining the top 10 popular cuisines offered by Bangalore restaurants.
3. **Expensive Restaurant Types:** Identifying the top 10 expensive restaurant types on average.
4. **Restaurant Concentration by Location:** Determining the locations in Bangalore with the highest concentration of restaurants and listing the top 10.
5. **Distribution of Restaurant Ratings:** Analyzing the distribution of restaurant ratings in Bangalore.
6. **Correlation between Votes and Ratings:** Investigating correlations between the number of votes received by a restaurant and its rating.
7. **Top 10 Rated Restaurants:** Identifying the top 10 rated restaurants in Bangalore.
8. **Online Ordering and Table Booking Services:** Determining the number of restaurants offering online ordering and table booking services.
9. **Likelihood of Online Ordering and Table Booking:** Identifying which restaurant types are most likely to offer online ordering and table booking.
10. **Rating Differences with Online Ordering:** Analyzing the average ratings of restaurants with and without online ordering services.
11. **Rating Distribution by Cost for Two People:** Investigating the distribution of restaurant ratings based on the approximate cost for two people.
12. **Rating Differences by Listing Type:** Determining if there are differences in restaurant ratings based on the type of listing.

## Data Modeling
We experimented with various machine learning models to predict restaurant performance. The following table summarizes the training and testing scores for each model:

<table>
  <tr>
    <th>Model</th> 
    <th>Training Score</th>
    <th>Testing Score</th>
  </tr>
  <tr>
    <td><strong>Logistic Regression</strong></td>
    <td>0.6825</td>
    <td>0.6753</td>
  </tr>
  <tr>
    <td><strong>Decision Tree</strong></td>
    <td>0.8989</td>
    <td>0.7537</td>
  </tr>
  <tr>
    <td><strong>Random Forest</strong></td>
    <td>0.8989</td>
    <td>0.7544</td>
  </tr>
  <tr>
    <td><strong>K-Nearest Neighbors</strong></td>
    <td>0.7935</td>
    <td>0.7156</td>
  </tr>
  <tr>
    <td><strong>XGBoost</strong></td>
    <td>0.8017</td>
    <td>0.7273</td>
  </tr>
</table>

Random Forest emerged as the best-performing model initially. However, we noticed overfitting issues. After parameter tuning, the Random Forest model achieved better generalization:
<table>
  <tr>
    <th>Model</th> 
    <th>Training Score</th>
    <th>Testing Score</th>
  </tr>
  <tr>
    <td><strong>Random Forest</strong></td>
    <td>0.8248</td>
    <td>0.7561</td>
  </tr>
</table>

## Model Deployment with Streamlit
We deploy our Random Forest machine learning model using Streamlit, a Python library for building interactive web applications. Users can access the deployed model to predict restaurant performance based on input data. The Streamlit web application offers features such as input data, prediction results, model evaluation metrics, and insights regarding the predictive capabilities of the model.

### How to Access the Model Deployment:
1. **Access the Streamlit Web Application:** Visit the provided link to access the deployed machine learning model.
2. **Interact with the Model:** Input relevant restaurant data to receive predictions regarding the restaurant's performance.
3. **Run Locally:** Clone the repository, install dependencies, and run the Streamlit application locally on your machine to explore the model's capabilities.

## Conclusion
The analysis of the Zomato-Bangalore-Restaurants dataset provides valuable insights into restaurant dynamics in Bangalore. Factors such as cuisine popularity, location concentrations, service offerings, and pricing greatly influence restaurant success. The Random Forest model proves effective in predicting restaurant performance, especially after addressing overfitting concerns through parameter tuning. This analysis can help stakeholders make informed decisions regarding restaurant establishment and operation strategies in Bangalore.
