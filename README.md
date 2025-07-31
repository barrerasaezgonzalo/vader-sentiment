# Sentiment Analysis API

A simple REST API built with Flask and TextBlob to analyze the sentiment of a given text.

## Features

- Accepts text input via POST request.
- Returns sentiment polarity and category (`positive`, `negative`, or `neutral`).
- Lightweight and easy to extend.

## Requirements

- Python 3.7+
- Flask
- TextBlob
- (Optional) Flask-CORS for frontend access

## Installation

1. Clone the repo:

   ```bash
   git clone https://github.com/yourusername/sentiment-analysis-api.git
   cd sentiment-analysis-api
    ```

2. Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate   # Linux/macOS
venv\Scripts\activate      # Windows
.\venv\Scripts\Activate.ps1  # PowerShell
```

3. Install dependencies:

```bash
pip install flask textblob
python -m textblob.download_corpora
```

4. (Optional) If you want CORS enabled:

```bash
pip install flask-cors
```
## Usage

```bash
python app.py
```

By default, it will run on http://127.0.0.1:5000.

## API Endpoint

POST /sentiment
Request body (JSON):
```json
{
  "text": "I love programming!"
}
```
Response

```json
{
  "text": "I love programming!",
  "sentiment": "positive",
  "polarity": 0.625
}
```

