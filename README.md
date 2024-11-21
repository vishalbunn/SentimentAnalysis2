# Sentiment Analysis Web Application
This project is a Flask-based web application for **sentiment analysis**. It allows users to predict sentiments (Positive or Negative) for individual text inputs or bulk data (CSV files). The app also provides a graphical distribution of sentiments for bulk predictions.

## 🚀 Features
- **Single Prediction**: Analyze the sentiment of a single text input.
- **Bulk Prediction**: Upload a CSV file containing sentences and get predictions along with a sentiment distribution graph.
- **Visualization**: Pie chart representation of sentiment distribution.
- **RESTful API**: Supports both file upload and JSON-based requests.

## 📂 Project Structure
- **`app.py`**: The main Flask application.
- **`Models/`**: Pre-trained models for prediction.
  - `model_xgb.pkl`: XGBoost model.
  - `scaler.pkl`: Scaler for feature normalization.
  - `countVectorizer.pkl`: Count Vectorizer for text feature extraction.
- **`templates/`**: Contains the `landing.html` file for the web interface.

## 🛠️ Requirements
- Python 3.8 or above
- Required Python packages (install via `requirements.txt`):
  ```bash
  flask
  nltk
  pandas
  matplotlib
  scikit-learn
  xgboost
  ```

## 🔧 Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_GITHUB_USERNAME/sentiment-analysis-app.git
   cd sentiment-analysis-app
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure NLTK stopwords are downloaded:
   ```python
   import nltk
   nltk.download('stopwords')
   ```
4. Run the application:
   ```bash
   flask run
   ```

## 🌐 API Endpoints
### 1. **Test Endpoint**
   - **URL**: `/test`
   - **Method**: GET
   - **Response**: `"Test request received successfully. Service is running."`

### 2. **Home Endpoint**
   - **URL**: `/`
   - **Method**: GET or POST
   - **Response**: Renders `landing.html`.

### 3. **Prediction Endpoint**
   - **URL**: `/predict`
   - **Method**: POST
   - **Request**:
     - **File Upload**: Upload a CSV file with a column named `Sentence`.
     - **JSON**: Provide a text string as `{"text": "Your sentence here"}`.
   - **Response**:
     - **Single Prediction**: JSON object with the sentiment prediction.
     - **Bulk Prediction**: CSV file with predictions and sentiment distribution graph.



## 🤝 Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m "Added feature"`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.




