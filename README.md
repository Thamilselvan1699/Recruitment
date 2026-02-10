AI-Powered Resume–Job Description Matching System

## Overview

This project matches **multiple resumes** against a **single job description** using NLP and machine learning techniques.
It combines **skill-based matching** with **semantic similarity scoring** to evaluate how well a resume fits a role.

The system is designed to be:

* Interpretable
* Fast
* Easy to extend toward embeddings, LLMs, and production systems

---

## Features

* Extracts relevant skills from job descriptions and resumes
* Computes skill match percentage
* Calculates semantic similarity using **TF-IDF + cosine similarity**
* Evaluates **multiple resumes in batch**
* Provides clear match decisions (Strong / Partial / Weak)

---

## Tech Stack

* **Python**
* **spaCy**
* **scikit-learn**
* **pandas**

---

##  Project Structure

```
├── main.py
├── job_description.txt
├── resumes/
│   ├── resume1.txt
│   ├── resume2.txt
│   └── resume3.txt
├── requirements.txt
└── README.md
```

---



* **Job Description**: `job_description.txt`
* **Resumes**: Multiple `.txt` files inside the `resumes/` folder

---

 How It Works

1. Load job description and resumes
2. Extract skills using predefined skill keywords
3. Calculate:

   * Skill match percentage
   * Semantic similarity score
4. Combine scores to determine match strength
5. Output results for each resume

---

Sample Output

```
Resume: resume2.txt
Matched Skills: {'python', 'sql', 'power bi'}
Skill Match Percentage: 75%
JD–Resume Similarity Score: 0.68
Decision: Strong Match
```

---

##How to Run

```bash
pip install -r requirements.txt
python main.py


Design Notes

* Skill extraction is **rule-based** for transparency
* TF-IDF provides lightweight semantic similarity
* Thresholds are configurable based on hiring needs
* Optimized for early-stage AI recruitment systems

---

Future Enhancements

* Lemmatization & NER-based skill extraction (spaCy)
* Skill importance weighting
* Resume ranking instead of thresholding
* Sentence embeddings (SBERT / OpenAI / HF)
* Supervised learning using recruiter feedback
* API deployment with FastAPI
* Monitoring data drift in production


Use Case

* Resume screening automation
* Candidate ranking systems
* AI-assisted recruitment platforms
* ML fundamentals + applied NLP learning project

