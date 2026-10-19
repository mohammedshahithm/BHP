# Bengaluru House Price Prediction

A machine learning web application that estimates residential property prices in Bengaluru using property features such as location, total square footage, BHK, and number of bathrooms.

## Live Demo

**Try the application:** https://bhp-price-prediction-frontend.onrender.com

## Features

- Estimate property prices using a trained machine learning model.
- Select from available Bengaluru locations.
- Enter square footage, BHK, and bathroom count.
- Receive predictions through a Flask REST API.
- Access the application through a publicly hosted web interface.

## Tech Stack

- **Language:** Python, JavaScript
- **Machine Learning:** Pandas, NumPy, Scikit-learn
- **Backend:** Flask, Flask-CORS, Gunicorn
- **Frontend:** HTML, CSS, JavaScript, jQuery
- **Deployment:** Render
- **Version Control:** Git and GitHub

## Project Structure

```text
BHP/
├── client/
│   ├── index.html
│   ├── app.css
│   └── app.js
└── server/
    ├── server.py
    ├── util.py
    ├── requirements.txt
    └── artifacts/
        ├── banglore_home_prices_model.pickle
        └── columns.json
```

## How It Works

1. The user enters property details through the web interface.
2. JavaScript sends the input to the Flask prediction API.
3. The backend converts the inputs into the feature representation expected by the trained model.
4. The model predicts an estimated property price.
5. The frontend displays the result in lakhs.

## Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/mohammedshahithm/BHP.git
cd BHP
```

### 2. Install backend dependencies

```bash
cd server
python -m venv .venv
```

Activate the environment on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

### 3. Start the Flask API

```bash
python server.py
```

The API runs locally at `http://127.0.0.1:5000` when using Flask's default development settings.

## API Endpoints

| Method | Endpoint | Purpose |
|---|---|---|
| GET | `/get_location_names` | Returns available locations |
| POST | `/predict_home_price` | Predicts the estimated property price |

The prediction endpoint accepts `total_sqft`, `location`, `bhk`, and `bath`.

## Notes

- Predictions are estimates produced by a trained model, not guaranteed market valuations.
- Results depend on the quality, coverage, and distribution of the training data.
- The hosted application uses Render's free service tier, which may introduce delays after inactivity.

## Author

Mohammed Shahith M

GitHub: https://github.com/mohammedshahithm
