# 🛍️ Amazon Product Recommendation System

This project demonstrates the creation of a **product recommendation engine** for Amazon using **user-product ratings**. By leveraging multiple recommendation algorithms, we aim to enhance personalization and improve customer experience during online shopping.

---

## 📚 Context

With the explosion of digital content and product choices online, **recommendation systems** have become essential to guide users toward relevant items. Amazon’s recommendation engine is a cornerstone of its success, increasing both user engagement and sales.

This project mimics that by using **Amazon’s electronic product rating dataset** to build several types of recommender systems and compare their performance.

---

## 🎯 Objective

To build and evaluate different recommendation models using product ratings data. The focus is on recommending relevant products to users based on their past behavior.

---

## 🗃️ Dataset

The dataset contains **Amazon product ratings** for electronic items and includes:

- `userId`: Unique identifier for each user  
- `productId`: Unique identifier for each product  
- `rating`: Rating given by the user (0–5 scale)  
- `timestamp`: When the rating was given (not used for modeling)  

---

## 🧠 Techniques Used

The following four recommendation systems were implemented:

1. ✅ **Rank-Based Recommendation System**  
   - Based on average product ratings  
   - Simple, non-personalized baseline

2. 🔁 **User-User Similarity Collaborative Filtering**  
   - Recommends products liked by similar users  
   - Evaluated using `precision@k`, `recall@k`, and `F1-score`

3. 🔁 **Item-Item Similarity Collaborative Filtering**  
   - Recommends items similar to those previously rated highly  
   - Based on cosine similarity between items

4. 🧮 **Matrix Factorization (Model-Based Collaborative Filtering)**  
   - Implemented using **SVD** with the `Surprise` library  
   - Hyperparameters optimized via **GridSearchCV**

---

## 📊 Evaluation Metrics

Each model was evaluated using:

- **Precision@k**  
- **Recall@k**  
- **F1-Score**

📌 **Best performing model:**  
> User-user collaborative filtering achieved the **highest F1-score**, providing the most balanced and accurate personalized recommendations.

---

## 📌 Key Insights

- Rank-based methods are simple and scalable but lack personalization.
- User-user and item-item collaborative filtering capture user behavior well, but require sufficient overlap in user history.
- Matrix factorization reduces dimensionality and handles sparse data efficiently.
- Hyperparameter tuning significantly improves model performance.

---

## 💡 Recommendations

- Use **user-user similarity models** for personalized recommendations on platforms with rich user interaction history.
- For large-scale datasets, explore **hybrid models** combining content-based and collaborative techniques.
- Incorporate **timestamp data** in future models for time-aware recommendations.

---

## 🔍 Data Ethics

- All user data used was anonymized.
- Ratings were treated as behavioral signals, with no assumptions on demographics or preferences beyond interaction.

---

## 🛠 Tools & Libraries

- Python  
- Pandas, NumPy  
- `surprise` library  
- Scikit-learn  
- Matplotlib, Seaborn  
- Jupyter Notebook  

---
## 📎 Notebook

See the complete implementation and evaluation in the notebook:  
[`book_recommendation_analysis.ipynb`](notebooks/book_recommendation_analysis.ipynb)

---

