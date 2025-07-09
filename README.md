# Netflix Popular Predictor 

This project is a machine learning-based binary classification model that predicts whether a Netflix title is **popular or not** based on its metadata.

## Features Used
- `country`
- `duration_time`
- `duration_type`
- `rating`
- `genre` (extracted from `listed_in`)
- `famous_director` (based on top 10 directors)
- `release_year`
- `cast_count` (based on cast)

## Target Variable
`is_popular`:  
- `1` → Popular  
- `0` → Not Popular  

Defined using a heuristic based on:
- High rating (like `TV-MA`, `R`, `PG-13`)
- Well-known directors
- Recency of release

## Model Used
- **Random Forest Classifier**
- With class balancing using `resample()` from `sklearn.utils`

## Performance
- Final Accuracy: **93%**
- ROC-AUC and Precision-Recall curves indicate strong classifier behavior

## File Included
- `Netflix_predictor_classification.ipynb`: Main notebook
- `README.md`: This file

---

## Tools Used
- Python 3.13
- pandas, scikit-learn, matplotlib

---

## Future Improvements
- Use NLP to extract sentiment from cast/description
- Include more refined genre-based popularity scoring
- Deploy the model using Streamlit

---

## Author
Made with frustration and persistence by **Naira**  
