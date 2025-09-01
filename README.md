#  House Price Prediction using Linear Regression  

This project predicts *house prices* based on the *area (in sq.ft.)* using *Linear Regression implemented from scratch*.  
The aim is to understand the working of regression without relying on machine learning libraries like scikit-learn.  

---

##  Problem Statement  

House prices usually depend on multiple factors such as area, location, number of rooms, etc.  
In this simplified case, we predict *house price using only the area of the house*.  

---

##  Dataset  

- Dataset file: Housing.csv  
- Columns used:  
  - *Area (sq.ft.)* → Independent variable (X)  
  - *Price* → Dependent variable (Y)  
- Missing values are removed during preprocessing.  

---

##  Mathematical Background  

The linear regression model is:  

\[
Price = w \times Area + b
\]

Where:  
- \( w \) = Weight (slope, price per sq.ft.)  
- \( b \) = Bias (intercept, base price)  

*Loss Function (Mean Squared Error):*  

\[
MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - (\hat{y}_i))^2
\]

*Gradient Descent Updates:*  

\[
w := w - \alpha \cdot \frac{\partial MSE}{\partial w}, \quad
b := b - \alpha \cdot \frac{\partial MSE}{\partial b}
\]

Where:  
- \( \alpha \) = Learning rate  
- Updates continue until convergence (loss decreases).  

---

##  Algorithm Steps  

1. Load dataset (Housing.csv)  
2. Extract area and price columns  
3. Normalize area values for stable training  
4. Initialize w and b randomly  
5. For each epoch:  
   - Predict prices using current w and b  
   - Compute loss (MSE)  
   - Calculate gradients  
   - Update parameters (w, b) using gradient descent  
   - Track R² score and loss  
6. Convert learned parameters back to original scale  
7. Output final regression equation  

---

##  Model Evaluation  

- *Loss (MSE)* decreases over epochs, indicating improved predictions.  
- *R² Score (Accuracy)* increases with training, showing better fit.  
- Final regression line approximates the housing dataset effectively.  

---

##  Results & Conclusion  

- The model successfully learns the relationship between *Area and Price*.  
- Gradient Descent ensures convergence towards optimal parameters.  
- Although this example uses only one feature (Area), the same principle can be extended to multiple features.  
- The implementation strengthens understanding of *core machine learning math* behind regression.  

---
