# Technical Requirements

Python 3.8+

Dependencies listed in requirements.txt:

``` bash
pandas
numpy
scikit-learn
faiss-cpu
requests
langchain_google_genai
tqdm
```

You also need a Google API Key for embeddings.
Set it in your environment:

``` bash
export GOOGLE_API_KEY="your_api_key_here"
```

# Dataset:

We use the provided dataset:
```bash
https://raw.githubusercontent.com/Bluedata-Consulting/GAAPB01-training-code-base/main/Assignments/assignment2dataset.csv
```

# Recommendation Function

``` python
def recommend_courses(profile: str, completed_ids: List[str]) -> List[Tuple[str, float]]:
    """
    Returns the top-5 recommended courses for a learner profile.
    Excludes courses the learner has already completed.
    Each result is (course_id, similarity_score).
    """
```

# Notebook

assignment2.ipynb contains all the necessary code and it can be run directly after above setup steps.


# Sample Input Queries

The system is evaluated on these 5 test cases:

“I’ve completed the ‘Python Programming for Data Science’ course and enjoy data visualization. What should I take next?”

“I know Azure basics and want to manage containers and build CI/CD pipelines. Recommend courses.”

“My background is in ML fundamentals; I’d like to specialize in neural networks and production workflows.”

“I want to learn to build and deploy microservices with Kubernetes—what courses fit best?”

“I’m interested in blockchain and smart contracts but have no prior experience. Which courses do you suggest?”


# Example Output (sample)

```bash
=== Profile 1: I've completed the 'Python Programming for Data Science' course and enjoy data visualization...
 -> C002 | Data Visualization with Matplotlib & Seaborn | Score: 0.8234
 -> C006 | Advanced Analytics with Python | Score: 0.7551
 ...
```
