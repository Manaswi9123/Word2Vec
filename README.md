# Word2Vec
## The dataset we are using here is a subset of Amazon reviews from the Cell Phones & Accessories category. The data is stored as a JSON file and can be read using pandas.
##  Link to the Dataset: http://snap.stanford.edu/data/amazon/productGraph/categoryFiles/reviews_Cell_Phones_and_Accessories_5.json.gz

# 🗺️ Word2Vec: Learning Semantic Relationships

Traditional text processing treats words as isolated symbols. This repository implements **Word2Vec**, an unsupervised learning architecture that represents words in a continuous vector space where distance correlates with semantic similarity.

---

## 🛠️ The NLP Stack
* **Library:** Gensim (Industry standard for topic modeling and word embeddings).
* **Language:** Python.
* **Data Manipulation:** Pandas, NumPy.
* **Concepts:** Cosine Similarity, Distributed Representations, Skip-gram/CBOW.

---

## 🧠 Key Features & Experiments

### 1. Training the Model
* Utilized the **Gensim** library to train a Word2Vec model on a custom corpus.
* Configured key hyperparameters including `window` (context size), `min_count` (frequency threshold), and `workers` (parallelization).

### 2. Similarity and Analogies
I conducted several tests to verify the model's linguistic "common sense":
* **Most Similar:** Finding words that appear in similar contexts (e.g., finding synonyms for "bad").
* **Similarity Scoring:** Quantifying the relationship between two specific words (e.g., a similarity score of ~0.52 for "cheap" and "inexpensive").
* **Does Not Fit:** Identifying the "odd one out" in a list of words based on their vector positions.



### 3. Vector Mathematics
The model allows for "word algebra," where vectors can be added or subtracted to find relationships:
* **The Logic:** If the model is trained well, it can solve equations like *King - Man + Woman = Queen*.

---

## 📈 Why use Word2Vec?
* **Captures Context:** Unlike One-Hot Encoding, Word2Vec understands that "Great" is closer to "Good" than it is to "Table."
* **Dimensionality Reduction:** Represents thousands of unique words in a relatively small vector space (e.g., 100-300 dimensions).
* **Transferability:** These learned vectors (weights) can be used as the input for more complex models like LSTMs or Transformers.

---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git](https://github.com/Manaswi9123/Python-DataScience-Fundamentals.git)

2. **Install Dependencies:**
        pip install gensim pandas numpy

3. **Execute:** Open Word2Vec.ipynb in Jupyter or VS Code to explore the word similarities and vector clusters.
