# Machine Downtime Prediction API

## Project Overview
This project provides a machine learning API for predicting machine downtime based on temperature and run time data.

## Prerequisites
- Python 3.8+
- pip

## Installation
1. Clone the repository:
```bash
git clone https://github.com/yourusername/machine-downtime-prediction.git
cd machine-downtime-prediction
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Running the API
```bash
uvicorn src.predictive_analysis:app --reload
```

## API Endpoints
- `/`: Root endpoint, returns welcome message
- `/upload/`: Upload CSV dataset
- `/train`: Train machine learning model
- `/predict`: Make downtime predictions

## Example Prediction Request
```json
{
  "Temperature": 75.5,
  "Run_Time": 500
}
```

## Testing
1. Upload dataset via `/upload/`
2. Train model via `/train`
3. Make predictions via `/predict`
