### Name: Ehab Mohammed Al-Ademi
### ID: 202170330
### Group 2

## Note
The Depth First Search Method Homework can be found attached in the Repository above. The program asks creates a node then asks how many nodes are attached to it. The program then recurses back into itself asking how many nodes are attached to each of the created nodes in the previous iteration. It continues with this until all nodes and subnodes have been titled. Then, the user is asked to choose the starting node and target node before finding computing thee search method required to find the target node.

This program implements a Depth-First Search (DFS) algorithm with a simple user interface, allowing the user to define a graph interactively. The `dfs` function performs a recursive search starting from a given node, visiting each node deeply along one path before backtracking to explore other branches. The function marks each node as visited to prevent revisiting and prints the order in which nodes are visited during the traversal. 

The user interaction is handled by the `get_graph_input` function, which prompts the user to input the number of nodes in the graph and the connections (edges) for each node. After constructing the graph, the `main` function confirms the graph's structure and asks the user for the starting node. The program then runs the DFS algorithm from the specified starting node, printing the traversal order. This allows the user to visualize the depth-first traversal of the graph based on their input.

# Overview
This project uses the Orange Data Mining platform to predict stock prices for three leading tech companies: Intel, Apple, and Nvidia. Stock data from 2009 to August 2024 serves as the training dataset, allowing the development of predictive models using Support Vector Machines (SVM), Random Forest, and Logistic Regression. The target for prediction is a "Label" column, which returns 1 if the company's closing stock price increases by more than 2% over two business days and 0 otherwise. This binary classification helps gauge whether a significant rise in stock prices is expected within a short time frame.

A separate dataset from September 1st to 14th, 2024, serves as the testing dataset. This recent data allows the models to be evaluated on unseen information to assess their performance and predictive accuracy. By leveraging three different models, the project offers a comparative approach to stock price forecasting, aiming to identify which machine learning algorithm provides the most reliable predictions in the tech sector.

# Data Collection & Preparation
Historical stock data from 2009 to August 2024 was collected for training and testing purposes for Intel, Apple, and Nvidia. From:
#### Apple's Stock Data: https://www.investing.com/equities/apple-computer-inc-historical-data
#### Nvidia's Stock Data: https://www.investing.com/equities/nvidia-corp-historical-data
#### Intel's Stock Data: https://www.investing.com/equities/intel-corp-historical-data
A large dataset was preprocessed and used as the training dataset. A new column in each titled "Label" was created as the target variable, which returns a boolean value: 1 if the stock’s closing price increases by more than 2% over two business days, or 0 if it doesn't. The Excel formula used was:
#### Excel Formula: IF((B4-B2)/B2>0.02,1,0)
#### in which 
#### B4= the closing stock price of two days in advance
####        B2= the closing stock price of today
A second dataset, covering stock data from September 1st to 14th, 2024, was created to serve as the testing dataset. This recent data allows for the evaluation of the models on new, unseen information.


# Model Selection Rationale
**1. Support Vector Machine (SVM)**  
SVM was selected for its effectiveness in binary classification problems, such as predicting whether a stock price will rise or not (the "Label" being 1 or 0). SVM works by finding the optimal hyperplane that separates data points of different classes, making it ideal for distinguishing between stock movements that show a 2% increase versus those that don’t. SVM's ability to handle complex, high-dimensional data patterns ensures that it can effectively process the historical stock data, which may contain nonlinear relationships between features.

**2. Random Forest**  
Random Forest was chosen due to its robustness and high accuracy in classification tasks, particularly when dealing with large datasets like stock market data. It is an ensemble learning method that builds multiple decision trees during training and outputs the class that is the mode of the classes of the individual trees. This model is well-suited for handling noisy data, which is often the case with stock prices that fluctuate unpredictably. Additionally, Random Forest’s ability to handle overfitting better than single decision trees ensures that it provides more reliable predictions.

**3. Logistic Regression**  
Logistic Regression was selected for its simplicity and interpretability in binary classification tasks. It estimates the probability that a given input belongs to a specific class (in this case, whether the stock price will rise by 2% or not). Logistic Regression assumes a linear relationship between the input features and the log-odds of the target variable, making it a good baseline model. It is computationally efficient and provides quick, interpretable results, which is useful for analyzing stock market trends where the goal is often to gain insights into the factors driving price changes.

Each model was chosen for its strengths in classification tasks: SVM for its precision in separating classes with complex patterns, Random Forest for its robustness and accuracy with noisy data, and Logistic Regression for its simplicity and ease of interpretation. Together, these models provide a well-rounded approach to predicting stock price movements.

# Testing and Evaluation
The testing dataset, which includes data from the first two weeks of September 2024, was used to evaluate the models. By analyzing the performance of each model on this fresh dataset, the project assesses how well the predictions hold up in real-time market conditions. The comparative evaluation of the SVM, Random Forest, and Logistic Regression models will help in determining the most reliable predictor for stock price movements among the three companies.


