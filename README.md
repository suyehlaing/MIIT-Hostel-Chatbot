# MIIT-Hostel-Chatbot
MIIT Hostel Chatbot: NLP-Based Question-Answering System

This project is an NLP-based Q&A system designed to assist students with hostel-related inquiries at MIIT. It leverages Semantic Search to understand the intent behind a user's question, even if it is phrased differently than the training data.

## Overview
MIIT Hostel Chatbot uses a retrieval-based approach. Instead of simply looking for matching words, it converts sentences into high-dimensional vectors (embeddings) to calculate how "similar" a user's query is to the pre-defined hostel FAQ database.

---

## Technologies Used
- Python
- Sentence Transformers (all-MiniLM-L6-v2) Model
- Google Colab
- Scikit-learn
- NumPy

---

## Dataset
The dataset consists of **question–answer pairs** related to hostel facilities, rules, timings, and services.  
Each question includes multiple **paraphrased variations** to improve matching accuracy.

---

## Approach
1. Encode all dataset questions using **SentenceTransformer**
2. Encode the user input query
3. Compute **cosine similarity** between the input query and stored questions
4. Select the question with the **highest similarity score**
5. Return the corresponding answer

---

## Motivation and Background

Moving into a university hostel is a major transition for students, often accompanied by a flood of questions regarding eligibility, fees, and daily rules. At MIIT, the Student Affairs office manually handles these repetitive inquiries, which can lead to:

    Response Delays: Students waiting for hours or days for simple answers during peak registration periods.

    Information Overload: Important details getting lost in long PDFs or physical notice boards.

    Staff Burnout: Faculty and staff spending significant time answering the same questions about curfews, laundry, and meal plans.

This project was born out of the need for a 24/7 accessible assistant that provides instant, accurate information. By automating these common queries, we allow Student Affairs to focus on more complex student cases while ensuring students get the help they need immediately, right from their devices.

For questions not covered by the chatbot, students are encouraged to contact Student Affairs at studentaffair@miit.edu.mm.
