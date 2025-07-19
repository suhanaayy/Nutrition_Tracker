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

1. **Clone the repository:**

```bash
git clone https://github.com/Adi123XD/Food-Cateloging-.git
cd Food-Cateloging-
