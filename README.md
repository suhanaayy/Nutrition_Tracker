# 🍎 Nutrition_Tracker

**Nutrition_Tracker** is an AI-powered application that processes images of food labels to determine whether the food is healthy or unhealthy. It utilizes Google Cloud Vision for OCR and a generative AI model to analyze nutritional information, storing the processed results in MongoDB.

---

## 📌 Overview

This application allows users to:
- Upload or link food label images
- Extract and clean nutritional data using OCR
- Adjust values based on serving size
- Analyze healthiness using a generative AI model
- Save structured data in MongoDB

---

## 🚀 Features

- **Image Upload & URL Input**: Analyze food labels via direct upload or image links.
- **OCR Processing**: Detect and clean text using Google Cloud Vision.
- **Nutrient Extraction**: Extract and format key nutrients from text.
- **Serving Size Adjustment**: Normalize values per serving.
- **Health Analysis**: Classify food as *Healthy* or *Unhealthy* using AI.
- **Database Storage**: Persist structured data into MongoDB.

---

## 🛠️ Prerequisites

- Python 3.10 or higher
- Google Cloud Vision API credentials
- Google Generative AI API key
- MongoDB database instance

---

## 📦 Installation

1. Clone the repository:

```bash
git clone https://github.com/suhanaayy/Food-Cateloging-.git
cd Food-Cateloging-
```

2. Install the required packages:

```bash
pip install -r requirements.txt
```

3. Set up the environment variables:
   - Create a `.env` file in the root directory of the project.
   - Add the following variables:

```env
GOOGLE_API_KEY=<your-google-api-key>
GOOGLE_APPLICATION_CREDENTIALS=<path-to-your-google-cloud-credentials-json>
MODEL_PATH=<path-to-your-model-file>
MONGO_URI=<your-mongo-uri>
```

---

## 📁 File Structure

- `main.py`: Contains the main functions for OCR, text cleaning, nutrient extraction, and formatting data.
- `webapp.py`: Streamlit application interface for user interactions.
- `mongo.py`: Contains functions to interact with the MongoDB database.
- `constants.py`: Contains constant values and patterns used in the application.
- `requirements.txt`: Lists all the dependencies required for the project.
- `.env`: Environment variables (not included in the repository; must be created manually).

---

## ▶️ Usage

1. Run the Streamlit application:

```bash
streamlit run webapp.py
```

2. Upload an image or enter an image URL for processing.

3. Enter the image URL to store in the database.

4. Click the "Enter" button to start processing.

5. The application will display the detected text, extracted nutrients, and whether the food is healthy or unhealthy.

6. If the data is valid, it will be inserted into the MongoDB database.

---

## 🧠 Functions

### main.py
- `format_data(input_dict)`: Formats the extracted nutrient data.
- `convert_to_float(value)`: Converts a string to a float.
- `healthy_unhealthy(ocr_text)`: Determines if the food is healthy or unhealthy using the AI model.
- `adjust_nutrient_values(output, serving_size)`: Adjusts nutrient values based on the serving size.
- `clean_ocr_text(text)`: Cleans the OCR-detected text.
- `extract_nutrients(text)`: Extracts nutrient information from the cleaned text.
- `detect_text(img_path)`: Performs OCR on the given image.

### webapp.py
- Streamlit application interface for user interactions.

### mongo.py
- `insert_to_db(data, db_name, collection_name)`: Inserts data into the specified MongoDB collection.

### constants.py
- Contains constant values and regular expressions used for nutrient extraction.

---

## 🛠️ Troubleshooting

- Ensure all required environment variables are set correctly in the `.env` file.
- Make sure your Google Cloud Vision API credentials are valid and correctly referenced in the environment variables.
- Verify that the MongoDB URI is correct and the database is accessible.
