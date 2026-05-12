# Exploring-Mental-Health-Narratives-on-Reddit-Using-BERT-and-NER
Mental health discourse analysis on Reddit using BERTopic, Sentence-BERT embeddings, Named Entity Recognition (NER), and topic modeling for narrative-rich social media data.


This project analyzes mental health discussions on Reddit using Natural Language Processing (NLP) and topic modeling techniques. The framework combines document preprocessing, Named Entity Recognition (NER), Sentence-BERT embeddings, and BERTopic to identify meaningful themes and semantic patterns from narrative-rich Reddit posts.

Overview

Online mental health communities contain large amounts of unstructured textual data where users discuss anxiety, depression, ADHD, stress, relationships, academic pressure, and emotional experiences. Traditional topic modeling approaches often struggle with long and multi-theme narratives.

This project introduces a pipeline that:

Collects Reddit data using PRAW
Preprocesses and cleans textual data
Extracts named entities using NER
Enhances text with semantic information
Segments long posts into smaller chunks
Generates contextual embeddings using Sentence-BERT
Performs topic modeling using BERTopic
Reduces redundant topics
Evaluates and visualizes discovered themes
Pipeline

Reddit API (PRAW) → Preprocessing → NER Extraction → Text Enhancement → Chunking → Sentence-BERT Embeddings → BERTopic → Topic Reduction → Evaluation & Visualization

Features
Reddit data collection using PRAW
Advanced text preprocessing
Named Entity Recognition (NER)
Narrative-aware document chunking
Sentence-BERT semantic embeddings
BERTopic clustering and topic extraction
Topic reduction and refinement
Interactive visualizations
Topic coherence and diversity evaluation
Technologies Used
Python
PRAW
BERTopic
Sentence Transformers
spaCy
Scikit-learn
UMAP
HDBSCAN
Pandas
Matplotlib
Plotly
Dataset

Data was collected from multiple Reddit communities related to mental health discussions, including:

r/mentalhealth
r/adhd
r/adhdwomen
r/malementalhealth

The dataset contains user-generated narrative posts discussing emotional experiences, diagnoses, stress, relationships, and coping mechanisms.

Methodology
1. Data Collection

Posts and comments were collected using the Reddit API through PRAW.

2. Preprocessing

Text cleaning included:

Lowercasing
URL removal
Stopword removal
Punctuation removal
Lemmatization
3. Named Entity Recognition

NER was applied to extract meaningful entities such as:

Persons
Organizations
Locations
Dates
4. Text Enhancement

Extracted entities were integrated into the cleaned text to improve semantic representation.

5. Document Chunking

Long Reddit posts were divided into smaller segments (~80 words) to improve thematic granularity.

6. Sentence Embeddings

Sentence-BERT was used to generate dense semantic embeddings for each chunk.

7. Topic Modeling

BERTopic combined:

Sentence embeddings
UMAP dimensionality reduction
HDBSCAN clustering
c-TF-IDF topic representation
8. Topic Reduction

Semantically similar topics were merged to improve interpretability and reduce redundancy.

9. Evaluation and Visualization

Topics were evaluated using:

Topic coherence
Topic diversity
Human interpretability

Visualizations included:

Topic hierarchy
Intertopic distance maps
Word clouds
Topic frequency charts

Project Structure
├── data/
├── notebooks/
├── src/
├── visualizations/
├── models/
├── requirements.txt
├── README.md
└── main.py


Install dependencies:

pip install -r requirements.txt
Run the Project
python main.py

Or run the Jupyter notebooks inside the notebooks/ directory.

Results

The framework successfully identified meaningful latent themes from Reddit discussions, including:

Anxiety and depression
Academic stress
ADHD experiences
Relationships and family conflicts
Emotional coping mechanisms
Medication and therapy discussions

Chunk-level topic modeling improved thematic precision for long narrative posts.

Future Improvements
Emotion-aware topic modeling
Temporal trend analysis
Sentiment-integrated topic discovery
Transformer fine-tuning on mental health corpora
Multi-label topic assignment
License

This project is intended for academic and research purposes.

Author

Neeharika Sompalli
