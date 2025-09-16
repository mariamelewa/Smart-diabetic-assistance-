# Smart Diabetic Assistant  

## Overview  
The **Smart Diabetic Assistant** is an accessible AI-driven system that supports diabetes management. It helps users make informed daily decisions through nutritional insights, insulin dose guidance, meal recommendations, FAQs, and glucose trend analysis.  

The system is designed to be lightweight, accessible via API, web, or mobile, and centered on user-friendly interaction.  

---

## Key Features  
- **Food & Nutrition Lookup**  
  - Recognizes foods from text input.  
  - Retrieves carbs, calories, protein, and fat values using nutrition datasets (USDA, Open Food Facts, Kaggle).  

- **Meal Suggestions**  
  - Provides diabetic-friendly meal options from curated recipes.  
  - Suggests alternatives when users request meals (e.g., “Suggest lunch”).  

- **Insulin Calculator**  
  - Computes insulin dose estimates using the user’s insulin-to-carb ratio (ICR).  
  - Includes safety guardrails and disclaimers.  

- **FAQ Chatbot**  
  - Rule-based chatbot that answers common diabetes-related questions.  
  - Built on curated datasets (MedQuAD or custom CSV).  

- **Tracking & Trends**  
  - Logs meals, insulin doses, and glucose levels.  
  - Visualizes data in tables and graphs.  
  - Detects recurring patterns, e.g., foods that spike blood sugar.  

---

## System Architecture (Proposed)  
**User Interface** (Flutter Mobile App)  
⬇️  
**Diabetes Management System**  
- Food Service (nutrition lookup & caching)  
- Meal Service (suggestions)  
- Insulin Service (calculator)  
- FAQ Service (chatbot)  
- Tracking & Trends Service (logs & insights)  
⬇️  
**Data Layer**  
- External APIs & datasets (USDA, Open Food Facts, Kaggle)  
- Internal database (SQLite/Postgres) for logs, cache, meals, FAQ  

---

## Tools & Libraries  
- **Core**: Python, SQLite3, SQLAlchemy  
- **Data Processing**: NumPy, Pandas, JSON  
- **APIs**: Requests (USDA, Open Food Facts)  
- **NLP**: NLTK, SpaCy (optional for entity recognition)  
- **Visualization**: Matplotlib, Seaborn  
- **ML (optional extensions)**: Scikit-learn, TensorFlow/PyTorch  

---

## Dataset Sources  
- **Nutrition Lookup**:  
  - [USDA FoodData Central](https://fdc.nal.usda.gov/download-datasets)  
  - [Open Food Facts](https://world.openfoodfacts.org/)  
  - [Kaggle – Diabetes Food Dataset](https://www.kaggle.com/datasets/jothammasila/diabetes-food-dataset)  

- **Meal Suggestions**:  
  - [Food.com Recipes](https://www.kaggle.com/datasets/irkaal/foodcom-recipes-and-reviews)  
  - [Healthy Diet Recipes](https://www.kaggle.com/datasets/thedevastator/healthy-diet-recipes-a-comprehensive-dataset/data)  

- **FAQ Chatbot**:  
  - [MedQuAD Dataset](https://github.com/abachaa/MedQuAD)  
  - [HuggingFace MedQuad](https://huggingface.co/datasets/keivalya/MedQuad-MedicalQnADataset)  

---

## Deliverables  
- **Flutter Application**
- **Database Schema** for storing logs, meals, and cache.  
- **ETL Scripts** for dataset cleaning and normalization.  
- **FAQ & Meal CSV files** for predefined content.  
- **Visualization Module** for glucose and insulin trends.  

---

## Disclaimer  
This system is a **support tool only**. It does **not replace medical advice**. Users must always consult healthcare professionals for clinical decisions.  
