# 🌐 Python API Integration & JSON Handling Methods

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![REST API](https://img.shields.io/badge/API-Requests%20%26%20HTTP-brightgreen.svg)
![JSON](https://img.shields.io/badge/Data-JSON%20Parsing-red.svg)

## 📌 Overview
APIs and JSON format form the backbone of modern web services and data pipelines. This repository contains practical guides and Jupyter notebooks demonstrating how to make HTTP requests, interact with REST APIs, parse nested JSON payloads, and transform API responses into analysis-ready Pandas DataFrames.

---

## 📂 Repository Contents
- **`API Methods_Vandana.ipynb`**:
  - Making HTTP requests using Python's `requests` and `urllib` libraries.
  - Handling HTTP status codes (`200`, `400`, `404`, `500`), request headers, authentication tokens, query parameters, and pagination.
- **`Json_handling and methods_Vandana.ipynb`**:
  - Serialization and deserialization (`json.loads()`, `json.dumps()`, `json.load()`, `json.dump()`).
  - Flattening deeply nested JSON structures using `pandas.json_normalize()`.
  - Error handling for malformed or corrupted JSON documents.

---

## 💻 Code Example: Fetching & Flattening API Data
```python
import requests
import pandas as pd

# Fetch data from REST API
response = requests.get("https://api.example.com/data", headers={"Accept": "application/json"})
if response.status_code == 200:
    data = response.json()
    # Normalize nested JSON into tabular DataFrame
    df = pd.json_normalize(data)
    print(df.head())
```

---

## 🛠️ Requirements
```bash
pip install requests pandas jupyter
```

---

## 👤 Author
- **Vandana Illipilla** - [GitHub Profile](https://github.com/Vandana251)
