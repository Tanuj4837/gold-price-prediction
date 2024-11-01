Here’s a README file for your Flask app that predicts the GLD price.

---

# Gold Price Prediction Web App

This project is a **Gold Price Prediction Web Application** built with **Flask** and **Random Forest Regression**. It predicts the daily price of Gold (GLD) based on market features such as `SPX`, `USO`, `SLV`, and `EUR/USD`, along with date-related features (`day`, `month`, `year`). The model's performance metrics (Mean Absolute Error and R² score) are displayed on the home page.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Future Improvements](#future-improvements)

## Features

- **Gold Price Prediction**: Predicts the daily price of Gold based on user-provided market inputs and date.
- **Cross-Validation Performance Metrics**: Displays the average Mean Absolute Error (MAE) and R² score from 5-fold cross-validation.
- **Interactive Web Interface**: Simple HTML form for inputting prediction values.

## Requirements

- Python 3.7 or higher
- Flask
- Pandas
- Scikit-learn

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/gold-price-prediction-app.git
   ```
2. **Navigate to the project directory**:
   ```bash
   cd gold-price-prediction-app
   ```
3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
4. **Dataset**:
   - Place your dataset file (`gld_price_data.csv`) in the root directory.
   - Ensure the dataset contains the following columns:
     - Date, SPX, USO, SLV, EUR/USD, GLD

## Usage

1. **Run the Flask app**:
   ```bash
   python app.py
   ```
2. **Access the app**:

   - Open a web browser and go to `http://127.0.0.1:5000/`.

3. **Predict**:
   - On the home page, enter the required feature values:
     - `SPX`: S&P 500 index
     - `USO`: United States Oil Fund
     - `SLV`: Silver ETF
     - `EUR/USD`: Euro/US Dollar exchange rate
     - Date: Select day, month, and year.
   - Submit to receive a prediction for the price of Gold (GLD).

## File Structure

- **app.py**: The main Flask application containing routes for rendering the home page and making predictions.
- **gld_price_data.csv**: Dataset containing historical data for model training.
- **templates/index.html**: HTML file for the front end.

## How It Works

- **Model Training**:

  - The Random Forest model is trained on `SPX`, `USO`, `SLV`, `EUR/USD`, and date-related features using 5-fold cross-validation.
  - Performance metrics (MAE and R²) are calculated and displayed on the home page.

- **Prediction**:
  - User inputs are standardized using `StandardScaler` before passing them to the trained model for prediction.

## Future Improvements

- **Additional Metrics**: Display more metrics like Mean Squared Error.
- **Enhanced Front End**: Improve the design and add input validation.
- **Model Optimization**: Experiment with additional models and hyperparameter tuning.

---
