# Predictive Analysis

This repository contains code for predictive analysis using a sample dataset. It includes an API that can be tested locally. Follow the instructions below to set up, run the code in Google Colab, or run the API locally and test the endpoints.

## Repository Contents
1. `Predictive_Analysis.ipynb`: Jupyter Notebook containing the main codebase.
2. `machine_downtime.csv`: A sample dataset used for the predictive analysis.
3. `predictive_analysis.py`: Python script to run the API locally.
4. This README file: Instructions on setup, usage, and API testing.

## Prerequisites
Ensure you have the following installed:
- Python 3.7 or higher
- Google Colab (browser access)
- Postman (for testing API endpoints)
- Required Python packages (specified in the notebook and `predictive_analysis.py`)

## Steps to Run the Code

### 1. Open the Notebook in Google Colab
1. Download the `Predictive_Analysis.ipynb` file from the repository.
2. Upload the file to Google Colab:
   - Go to [Google Colab](https://colab.research.google.com/).
   - Click on **File** > **Upload Notebook**.
   - Choose the `Predictive_Analysis.ipynb` file from your local system.

### 2. Upload the Dataset in Colab
1. After opening the notebook, ensure you also have the `machine_downtime.csv` file.
2. Upload the dataset in Colab:
   - In the left panel, click on the folder icon.
   - Click **Upload**, and select `machine_downtime.csv`.
   - The dataset will be accessible in the Colab environment.

### 3. Install Required Libraries
The first few cells of the notebook install the required libraries. Ensure you run these cells sequentially. Typical libraries include:
- `pandas`
- `scikit-learn`
- `flask` (for API implementation)

Run the cells in order to set up the environment.

### 4. Execute the Code
1. Run the data preprocessing, model training, and evaluation cells.
2. Follow the notebook's instructions for model analysis.

### 5. Start the API Locally in Colab
At the end of the notebook, there is a section to start the Flask API. Execute the cell to initiate the API on a local server. It will display a URL (e.g., `http://127.0.0.1:5000/`) where the API is running.

## Running the API Locally Using `predictive_analysis.py`

1. **Set Up the Environment**
   - Install Python 3.7 or higher.
   - Create and activate a virtual environment:
     ```bash
     python -m venv venv
     source venv/bin/activate   # On Windows: venv\Scripts\activate
     ```
   - Install the required libraries:
     ```bash
     pip install -r requirements.txt
     ```

2. **Run the API**
   - Ensure the `machine_downtime.csv` file is in the same directory as `predictive_analysis.py`.
   - Start the API server by running:
     ```bash
     python predictive_analysis.py
     ```
   - The server will start on `http://127.0.0.1:5000/`.

3. **Testing the API with Postman**

### 1. Install Postman
If you haven't already, download or open here [Postman](https://www.postman.com/).

### 2. Set Up Postman Requests
1. Open Postman and create a new request.
2. Select the **POST** method.
3. Enter the API endpoint URL (e.g., `http://127.0.0.1:5000/predict`).
4. Go to the **Body** tab and select **raw**.
5. Choose **JSON** as the data format and input the sample data in JSON format. For example:
   ```json
   {
       "feature1": 5.1,
       "feature2": 3.5,
       "feature3": 1.4,
       "feature4": 0.2
   }
   ```

### 3. Send the Request
Click **Send** to test the endpoint. If everything is set up correctly, the API will return a response with the prediction.

## Troubleshooting
- Ensure the Flask server is running.
- Use the provided dataset format when testing endpoints.
- Verify that all required libraries are installed.

## Conclusion
This project demonstrates predictive analysis using a sample dataset and provides an API for real-time predictions. Follow the steps above to set up, run, and test the code and API. For additional questions, feel free to open an issue in this repository.

