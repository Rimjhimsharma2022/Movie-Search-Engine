# AI Systems Development Assignment 1  

**Author**: Rimjhim Sharma  

**Roll No.**: 221000046

**Branch**: CSE

---

## 📌 Project Overview  

This project implements a **semantic search engine for movie plots**.  
Using pre-trained sentence embeddings (`all-MiniLM-L6-v2`) and cosine similarity, the system finds the most relevant movies for a given natural language query.  

The solution is implemented in Python, tested with unit tests, and structured to meet all requirements of the **AI Systems Development course assignment**.  

---

## ✨ Features  

- **Sentence Embeddings** with [SentenceTransformers](https://www.sbert.net/).  
- **Semantic Search** using cosine similarity between query and dataset embeddings.  
- **Reusable Function**: `search_movies(query, top_n)` returns the top matching movies.  
- **Unit Tests** included to ensure correctness.  
- **Easy to Extend** with other datasets or models.  

---

## 📂 Project Structure  
```bash
Ai-System-Devlopment-Assignemnt-1/
├── movie_search.py # Main semantic search logic
├── movies.csv # Dataset (titles + plots)
├── movie_search_notebook.ipynb # Notebook (experiments / demo)
├── tests/
│ └── test_movie_search.py # Unit tests
├── requirements.txt # Python dependencies
├── .gitignore # Ignore venv, pycache, etc.
├── README.md # Project documentation (this file)
└── unit_tests.png # Screenshot of passing tests (optional)
```

---

## ⚙️ Setup & Installation  

1. **Clone the repository**  
```bash
git clone https://github.com/Rimjhimsharma2022/movie-search-engine.git
cd Ai-System-Devlopment-Assignemnt-1
 ```
   


2. Create virtual environment
```bash
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows
```


3. Install dependencies
 ```bash
pip install -r requirements.txt
```


## 🚀 Usage

In Python:
 ```bash
from movie_search import search_movies

query = "spy thriller in Paris"
results = search_movies(query, top_n=5)

print("Search results:")
print(results)
```


Example output:
 ```bash
Search results:
                 title                                               plot
1347           XYZ Movie   A thrilling spy adventure set in the heart of Paris...
2204           ABC Movie   A detective uncovers a conspiracy in Europe...
...
 ```

## ✅ Testing
 ```bash
Run unit tests to verify functionality:

python -m unittest tests/test_movie_search.py -v
```


All tests must pass ✔️ to score full marks.


## 🧠 Technical Workflow

Load dataset (movies.csv) into Pandas DataFrame.

Encode movie plots into embeddings with all-MiniLM-L6-v2.

Encode user query → get embedding.

Compute cosine similarity between query and all movie embeddings.

Return top N results as a DataFrame with title and plot.



## 📜 License

This project is for educational purposes under the AI Systems Development course.


---


