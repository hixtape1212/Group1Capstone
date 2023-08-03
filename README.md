# Group-1 Consulting 
## See Through the Ambiguity - Predicting Home Prices
![Skyline](AustinSkyline.jpg)
Group-1 Consulting has been approached by a real estate investement agency who is requesting an algorithm that predicts home prices. The real estate investment firm FlatTech RealEstate, buys homes in the Austin area. They have tasked our team with finding a datafile, clean it, and run various algorithms to create an home price predictor. Our algorith will predict home prices based on common features of home listings like number of beds, baths, lot size, square footage, etc. to help both buyers and sellers see through the ambiguity in home pricing.

* [***Business Understanding:***](#business-understanding) The business case our team is attempting to solve.
* [***Data Understanding:***](#data-understanding) Basic overview of our approach and dataset.
* [***Model Evaluation Strategy:***](#model-evaluation-strategy) Overview of model selection.
* [***Conclusion:***](#conclusion) TBD
* [***Navigation:***](#navigation) Link and description of files in the repo.

# Business Understanding
Home prices in the U.S. particullary in fast growing cities are important to know for both buyers and sellers, and sometimes the fair market value of a home can be influenced by outside factors, emotional views, and other points that could inflate or deflate the price of a home. Add to that the usually it can cost anywhere from $200 - $600 to appraise a home, machine learning is a great alternative to take some of the ambiguity and time-consuimption out of home pricing. An algorithm such as the one our group has developed can aleviate the risk of buying homes in voliatile markets, letting our clients know a relative value of the home they are buying, helping them to know whether or not they are getting a good deal. 

# Data Understanding
When looking for data, our team was looking for complete datasets on individual home prices, perhaps with an address as a primary key, with the relevant features that most home owners look for when buying a home. These were mentioned above but include number of beds, baths, lot size, and square footage. Other features would be an added bonus, but at the core we wanted data that you would find on a typical home listing.

Searching through Kaggle, our team was able to find the Austin, TX House Listing Dataset by Eric Pierce. He created the dataset for his capstone project in college in 2021. The data was scrapped from Zillow at the time, and he originally wanted to use both images and house features to predict home prices. It was very clean, having over 15,000 listings with 40+ features of each entry. Also a huge plus was that there were no NaN, which made the initial data cleaning part very simple.

# Model Evaluation Strategy
Our strategy to evaluating the problem and create a model was a three pronged approach. Our team wanted to see dhow using different models would improve accuracy of prediction as well as decrease our overall evaluation metric. The models we decided to use were Linear Regression, Decision Trees, and finally a Sequential Deep Nueral Network. 

### Linear Regression
Linear regression techniques are relatively simple and quick lo implement, and is appropiate when there is a linear relationship between the dependent variable (house price) and the independent variables (size, number of rooms and bathrooms, etc). In this case is reasonable to assume that, in general increase of house size, number of rooms and bathrooms results in a proportional increace in house price. 

We wanted start with a simple model to predict house price and evaluate results before apply other complex models.
### XGBoost regression
The results in linear regression model weren't the best, so we tried with different techniques as desicion tree, random forest and XGBoost, this last had the best performance and we worked in it.
XGBoost algorithm is one of the most popular techniques, is a versatil algorithm that can be used for both classification and regression problems, it is fast to execute and highly efective and in this case gave us the best model for predictions.
### Sequential Deep Nueral Network
Our sequential deep nueral network was an attempt at the end to see if there could be any additional improvement in accuracy. The nature of the nueral network is more complex, requires more computational resources, and isn't very intuitive in it's predictions. However, in many situations this approach can yeild better results. 
Multiple nueral networks we're trained and ran, some being very simple with roughly 3000 trainable parameters, and others being more complex with over 100000 trainable parameters. The range in complexity was in an attempt to lower evaluation metric which wasn't successful. In the end many of the models leveled out with an evaluation metric of XXXXXXX and didn't show much improvement afterwards. Many attempts to train a better model were stopped as it became more difficult to stop overfitting, even using techniques like early stopping and dropout layers.

# Conclusion
In order to accurately predict home prices in the Austin area, the algorithm models that would be the most effective are the XGBoost Regressor model and the Neural Network model we created. Of the two models, the XGBoost Regressor model is the most accurate model. XGBoost typically excels when trying to create a model with a high-dimensional dataset like the one that we have. ​Determination coefficient is 0.79 in other words, this model is explaining the 79% of data​. The MAE shows that our model is off by about 55,616 dollars in each prediction, in other words we could sell a house 55 thousand dollars more expensive or cheaper.​ This technique gave us the smallest MAE, and after applying cross validation we get the same determination coefficient. With an MAE of 50,000 results are promising, but additional work is needed to optimize our model.​ The main limitations are that we are only working with data from 2018-2021 and that there is a large variance in our prediction. For our next steps, we need to tune the model using various hyperparameters, and finally we need to validate and present the optimized model. 

# Navigation
In this repository, you will find the following: this readme.md file, our consolidated Jupyter notebook that contains all of our code for the data analysis, the data file that we used for our source data, and the pdf version of our powerpoint presentation. 
