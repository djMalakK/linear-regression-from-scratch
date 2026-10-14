# Linear Regression from Scratch

## Overview

This project implements a Linear Regression model from scratch using Python and NumPy to predict students' final mathematics grades.

The goal is to understand how Linear Regression works internally by implementing Gradient Descent, generating predictions, and calculating evaluation metrics without using scikit-learn for model training or evaluation.

## Dataset

This project uses the Student Performance dataset from the UCI Machine Learning Repository.

- **Dataset:** Student Performance — Mathematics
- **Target variable:** `G3` (final mathematics grade)
- **Input features:**
  - `studytime`: Weekly study time category
  - `failures`: Number of past class failures
  - `absences`: Number of school absences
  - `G1`: First-period grade
  - `G2`: Second-period grade

The original mathematics dataset contains 395 student records and 33 attributes.

**Dataset source:** [UCI Machine Learning Repository — Student Performance](https://archive.ics.uci.edu/dataset/320/student+performance)

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Jupyter Notebook

## Project Workflow

1. Load and explore the dataset.
2. Select the input features and target variable.
3. Split the data into training and test sets.
4. Standardize the input features using training-set statistics.
5. Add a bias term to the feature matrix.
6. Implement Linear Regression using Gradient Descent.
7. Generate predictions on the test set.
8. Calculate evaluation metrics manually.
9. Visualize training loss and compare actual versus predicted grades.

## Implementation

The model is implemented using NumPy without relying on scikit-learn for model training or evaluation.

The implementation includes:

- Manual weight initialization
- Gradient Descent optimization
- Feature standardization
- Predictions using matrix operations
- Manual calculation of Mean Absolute Error (MAE) and R² Score

## Evaluation Results

The model was evaluated on a held-out test set using two metrics:

- **Mean Absolute Error (MAE): 1.159**
- **R² Score: 0.776**

The MAE indicates that predictions differed from actual final grades by an average absolute error of approximately 1.16 grade points.

The R² score indicates that the model explained approximately 77.6% of the variance in final grades within this test set.

These results depend on the train-test split and training configuration and do not guarantee the same performance on other datasets.

## Visualizations

The notebook includes the following visualizations:

- **Training Loss:** Shows how the Mean Squared Error changes during Gradient Descent.
- **Actual vs. Predicted Grades:** Compares the model's predictions with the actual final grades.

These visualizations help assess the learning process and prediction performance.

## Limitations

- Performance depends on the train-test split and training parameters.
- The model uses a limited set of student features.
- `G1` and `G2` are earlier grades strongly associated with the final grade `G3`, which can make prediction easier.
- Results may not generalize to other schools or educational settings.
- This project is intended for educational purposes and is not designed for high-stakes educational decisions.

## Learning Objectives

Through this project, I practiced:

- Understanding the mathematics behind Linear Regression.
- Implementing Gradient Descent from scratch.
- Working with NumPy arrays and matrix operations.
- Applying feature standardization.
- Evaluating regression models using MAE and R².
- Visualizing machine learning results.

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/djMalakK/linear-regression-from-scratch.git
   ```

2. Navigate to the project directory:

   ```bash
   cd linear-regression-from-scratch
   ```

3. Install the required libraries:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Ensure that `student-mat.csv` is in the project directory.

5. Open `linear_regression.ipynb` in VS Code or Jupyter Notebook and run the cells in order.

## Future Improvements

- Experiment with different learning rates and numbers of training epochs.
- Evaluate performance across multiple train-test splits.
- Add cross-validation for more reliable evaluation.
- Compare the implementation with scikit-learn's Linear Regression model.

---

**Project:** Linear Regression from Scratch using Python and NumPy
