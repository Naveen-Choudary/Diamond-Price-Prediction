# Diamond Price Prediction

This project is a web-based application that predicts the price of a diamond based on its features. It utilizes machine learning models trained on the `gemstone.csv` dataset and is deployed using Flask.

## Features
- Train multiple regression models and select the best-performing one.
- Preprocess categorical and numerical features using `OneHotEncoder` and `StandardScaler`.
- Deploy the trained model using Flask.
- Simple UI for user input and prediction visualization.

---

## Installation & Setup

### 1. Clone the Repository
```sh
git clone https://github.com/Naveen-Choudary/Diamond-Price-Prediction.git
cd Diamond-Price-Prediction
```

### 2. Create a Virtual Environment (Optional but Recommended)
```sh
python -m venv venv
```
#### On Windows:
```sh
venv\Scripts\activate
```
#### On macOS/Linux:
```sh
source venv/bin/activate
```

### 3. Install Dependencies
```sh
pip install -r requirements.txt
```

### 4. Train the Model (if needed)
Run the model training script to generate `model1.pkl` and `preprocessor.pkl`:
```sh
python train_model.py
```

### 5. Run the Flask Application
```sh
python app.py
```
Access the web application at [http://127.0.0.1:5000/](http://127.0.0.1:5000/).

---

## Project Structure
```
Diamond-Price-Prediction/
│── gemstone.csv           # Dataset
│── train_model.py         # Model training script
│── model1.pkl             # Trained model
│── preprocessor.pkl       # Preprocessing pipeline
│── templates/             # Frontend UI
│   ├── index.html         # Main page
│── static/                # CSS, JS, images (if needed)
│── app.py                 # Flask application
│── requirements.txt       # Project dependencies
│── .gitignore             # Files to ignore in Git
│── README.md              # Project documentation
```

---

## API Endpoint

### `/predict` (POST)

**Request:**
```json
{
  "carat": 0.8,
  "cut": "Premium",
  "color": "E",
  "clarity": "SI1",
  "depth": 62.3,
  "table": 57,
  "x": 5.85,
  "y": 5.83,
  "z": 3.61
}
```

**Response:**
```json
{
  "price": 5321.45
}
```

---

## Contributing
Feel free to contribute by submitting issues or pull requests.

---

## License
This project is open-source. Feel free to use, modify, and distribute it as needed.
