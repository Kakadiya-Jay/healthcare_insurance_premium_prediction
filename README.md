# Healthcare Insurance Premium Prediction

This project predicts healthcare insurance premiums using machine learning models trained on past customer data. The goal is to help users estimate their insurance premium based on their information, making the process transparent and accessible.

## Project Overview

- **Purpose:** Predict the insurance premium for a customer using their details (such as age, health, etc.).
- **Approach:** The project uses past years' customer data and their premiums to train machine learning models. The trained models are then used to predict premiums for new customers.

## Model Segmentation

To improve accuracy, the project uses two separate models based on the customer's age:

1. **Age ≤ 25 years:**
	- Model: Linear Regression
	- Accuracy: ~98.80% (with only 2.14% extreme error rate)
	- Reason: This model performs extremely well for younger customers.

2. **Age > 25 years:**
	- Model: XGBoost Regression
	- Accuracy: ~99.7% (with only 0.32% extreme error rate)
	- Reason: XGBoost gives better results for older customers compared to Linear Regression.

## Project Structure

- `main.py`: Main application file to run the prediction app.
- `prediction_helper.py`: Helper functions for prediction logic.
- `artifacts/`: Contains trained model and scaler files.
- `notebook/`: Contains datasets and Jupyter notebooks for data analysis and model training.
- `requirements.txt`: List of all required Python packages.

## How to Install Dependencies

Before running the application, install the required dependencies using the following command:

```bash
pip install -r requirements.txt
```

## How to Run the Application

To start the application, run the following command in your terminal:

```bash
python main.py
```

This will launch the Streamlit web interface where you can input customer details and get a premium prediction.

## Features

- Predicts insurance premium based on user input.
- Uses two different models for better accuracy based on age group.
- User-friendly web interface built with Streamlit.

## Notes

- All model files are stored in the `artifacts` folder.
- Datasets and notebooks for model training are in the `notebook` folder (located in the same directory as `artifacts`).
- Make sure you have Python installed on your system.

## Example Use Case

1. Open a terminal in the project directory.
2. Install dependencies: `pip install -r requirements.txt`
3. Run the app: `python main.py`
4. Enter customer details in the web interface to get a premium prediction.

## Contact

For any questions or support, please contact the project maintainer.
