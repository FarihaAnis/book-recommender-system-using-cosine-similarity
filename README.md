# Book Recommendation System Using Cosine Similarity

## **Objective**
To develop a recommendation system that suggests books to users based on shared rating patterns, leveraging collaborative filtering and cosine similarity.

---

## **Tools and Libraries**
- **Data Manipulation**: pandas, numpy
- **Similarity Computation**: sklearn.metrics.pairwise.cosine_similarity
- **Utility**: IPython.display for visualizing recommendations

---

## **Dataset**
The system utilizes publicly available datasets from [Kaggle](https://www.kaggle.com/datasets/ra4u12/bookrecommendation) : 
- **Books**: Contains details such as titles, authors, publishers, and cover images.
- **Ratings**: Tracks user ratings for books.
- **Users**: Includes demographic information (optional for this workflow).

### **Preprocessed Data**:
- Filtered books with at least 50 user ratings.
- Focused on users with more than 50 ratings to ensure active user data.

---

## **Methodology**
1. **Data Preprocessing**:
   - Combined book metadata with user ratings for a unified dataset.
   - Removed duplicates and normalized titles for consistency.
   - Filtered out less popular books and inactive users to focus on meaningful interactions.

2. **Rating Matrix**:
   - Created a matrix where:
     - Rows represent books.
     - Columns represent users.
     - Cells contain user ratings (or `0` if unrated).

3. **Cosine Similarity**:
   - Calculated pairwise similarity scores between books based on user rating patterns.
   - Stored results in a similarity matrix for efficient retrieval.

4. **Recommendation Engine**:
   - For a given book, retrieved the most similar books using the similarity matrix.
   - Displayed recommendations with titles, cover images, and similarity scores.

---

## **Testing**
- Example input books included:
  - _"Harry Potter and the Chamber of Secrets (Book 2)"_
  - _"A Is for Alibi (Kinsey Millhone Mysteries)"_
  - _"A Walk to Remember"_
- The system recommended related books from the same series or by the same author, demonstrating the effectiveness of cosine similarity.

---

## **Results**
- Successfully identified highly related books based on user rating patterns.
- Accurate recommendations for series like _Harry Potter_ and _Kinsey Millhone Mysteries_.
- Limitations observed in diversity when dealing with books outside established patterns.

---

## **Conclusion**
The recommendation system effectively connects users to books they are likely to enjoy by analyzing user rating patterns. Cosine similarity provides a robust method for collaborative filtering, making the system well-suited for recommending books within series or by the same author. Future improvements could focus on increasing diversity in recommendations and addressing broader user preferences.

---

## **Copyright Remark**
This project was developed for self-learning purposes using publicly available datasets and adhering to fair use principles. No commercial use is intended, and intellectual property rights for datasets and external resources belong to their respective owners.
