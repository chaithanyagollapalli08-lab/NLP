# NLP Preprocessing and Feature Extraction

## Project Overview

This repository demonstrates the complete Natural Language Processing (NLP) pipeline, starting from text preprocessing to advanced feature extraction and linguistic analysis techniques. The goal is to transform raw text into meaningful numerical representations that can be used for Machine Learning and Deep Learning models.

---

# NLP Preprocessing Pipeline

Raw text cannot be directly understood by machine learning algorithms. Therefore, it must go through several preprocessing steps.

## 1. Lowercasing

Converts all characters into lowercase to maintain consistency and reduce vocabulary size.

### Example

Input:
```
I Love NLP
```

Output:
```
i love nlp
```

---

## 2. Text Cleaning

Removes unwanted information such as URLs, punctuation marks, special characters, and extra spaces.

### Example

Input:
```
Visit https://google.com! NLP is awesome!!!
```

Output:
```
Visit NLP is awesome
```

---

## 3. Tokenization

Splits text into individual words or tokens.

### Example

Input:
```
I love NLP
```

Output:
```python
['I', 'love', 'NLP']
```

---

## 4. Stopword Removal

Removes commonly occurring words that contribute little meaning.

### Example

Input:
```python
['I', 'am', 'learning', 'NLP']
```

Output:
```python
['learning', 'NLP']
```

Common stopwords:
```
is, am, are, the, a, an, in, on, at, of
```

---

## 5. Stemming

Reduces words to their root form by removing suffixes.

### Examples

| Original Word | Stemmed Word |
|--------------|-------------|
| Playing | Play |
| Running | Run |
| Studies | Studi |
| Connected | Connect |

---

## 6. Lemmatization

Converts words into their meaningful dictionary form.

### Examples

| Original Word | Lemmatized Word |
|--------------|----------------|
| Running | Run |
| Better | Good |
| Studies | Study |
| Mice | Mouse |

Lemmatization is generally more accurate than stemming because it considers context and vocabulary.

---

# Feature Extraction Techniques

After preprocessing, text must be converted into numerical vectors so machine learning algorithms can process it.

---

## 1. Bag of Words (BoW)

Represents text using word frequency counts.

### Example

Documents:
```
I love NLP
I love Python
```

Vocabulary:
```
[I, love, NLP, Python]
```

Vectors:

| Document | I | love | NLP | Python |
|-----------|---|------|-----|--------|
| Doc1 | 1 | 1 | 1 | 0 |
| Doc2 | 1 | 1 | 0 | 1 |

### Advantages

- Simple
- Easy to implement

### Limitations

- Ignores context
- Produces sparse vectors

---

## 2. N-Grams

Captures sequences of words instead of individual words.

### Types

#### Unigram (1-word)

```
I love NLP
```

Output:
```
[I, love, NLP]
```

#### Bigram (2-word)

Output:
```
[I love, love NLP]
```

#### Trigram (3-word)

Output:
```
[I love NLP]
```

### Advantages

- Captures local context
- Useful for text classification

---

## 3. TF-IDF (Term Frequency-Inverse Document Frequency)

Measures the importance of a word in a document relative to the entire corpus.

### Formula

TF-IDF = TF × IDF

Where:

```
TF = Term Frequency

IDF = log(Total Documents / Documents containing the term)
```

### Advantages

- Reduces impact of common words
- Highlights informative words

---

# Word Embeddings

Unlike BoW and TF-IDF, embeddings capture semantic meaning and context.

---

## 4. Word2Vec

Converts words into dense vectors while preserving semantic relationships.

Developed by Google.

### Architectures

### CBOW (Continuous Bag of Words)

Predicts target word from surrounding words.

### Skip-Gram

Predicts surrounding words from target word.

### Example

```
King - Man + Woman ≈ Queen
```

### Advantages

- Captures semantic relationships
- Dense vector representation

---

## 5. GloVe (Global Vectors)

Developed by Stanford University.

Combines:
- Global statistical information
- Local context information

### Advantages

- Better semantic understanding
- Pre-trained embeddings available

Examples:
```
King ↔ Queen
Paris ↔ France
Tokyo ↔ Japan
```

---

## 6. FastText

Developed by Facebook.

Represents words using character-level subwords.

### Example

Word:
```
Playing
```

Subwords:
```
Pla
Lay
ayi
ying
```

### Advantages

- Handles out-of-vocabulary words
- Better for misspellings and rare words

---

# Linguistic Analysis

Beyond numerical representations, NLP also analyzes grammatical and semantic structures.

---

## 7. Part-of-Speech (POS) Tagging

Assigns grammatical categories to words.

### Example

Sentence:
```
Sachin plays cricket.
```

Output:

| Word | POS Tag |
|--------|---------|
| Sachin | Noun |
| plays | Verb |
| cricket | Noun |

### Applications

- Grammar checking
- Information extraction
- Chatbots

---

## 8. Dependency Parsing

Identifies grammatical relationships between words.

### Example

Sentence:
```
Sachin plays cricket.
```

Relationship:

```
plays → Root
Sachin → Subject of plays
cricket → Object of plays
```

### Applications

- Question answering
- Machine translation
- Text summarization

---

## 9. Named Entity Recognition (NER)

Identifies important real-world entities in text.

### Example

Sentence:
```
Sachin works at Google in Hyderabad.
```

Output:

| Entity | Type |
|----------|------|
| Sachin | Person |
| Google | Organization |
| Hyderabad | Location |

### Common Entity Types

- Person
- Organization
- Location
- Date
- Time
- Money
- Product

### Applications

- Resume Parsing
- Information Extraction
- Search Engines
- Virtual Assistants

---

# Libraries Used

- Python
- NumPy
- Pandas
- NLTK
- SpaCy
- Gensim
- Scikit-learn
- Regular Expressions (re)

Install dependencies:

```bash
pip install numpy pandas nltk spacy gensim scikit-learn
```

---

# Project Workflow

```
Raw Text
    ↓
Lowercasing
    ↓
Text Cleaning
(Remove URLs, Punctuation)
    ↓
Tokenization
    ↓
Stopword Removal
    ↓
Stemming / Lemmatization
    ↓
Feature Extraction
(BoW, N-Grams, TF-IDF)
    ↓
Word Embeddings
(Word2Vec, GloVe, FastText)
    ↓
Linguistic Analysis
(POS Tagging, Dependency Parsing, NER)
    ↓
Machine Learning / Deep Learning Models
```

---

# Applications

- Sentiment Analysis
- Spam Detection
- Fake News Detection
- Text Classification
- Chatbots
- Recommendation Systems
- Search Engines
- Resume Screening
- Machine Translation
- Question Answering Systems

---


## Author

**Chaithanya Gollapalli**

Aspiring Data Scientist 

Gmail: gollapallichaithanya08@gmail.com
