# CV Compatibility Checker

## Overview
The CV Compatibility Checker is a Python tool designed to assess the compatibility between a candidate's CV and a job description. It utilizes state-of-the-art natural language processing (NLP) models to analyze the textual content of the CV and the job description, providing a compatibility score to aid in the recruitment process.

## Why Use NLP Models?
Traditional methods of CV screening involve manual review by recruiters, which can be time-consuming and prone to bias. By leveraging NLP models, we can automate this process and provide a more objective assessment of a candidate's suitability for a job role. NLP models, such as BERT (Bidirectional Encoder Representations from Transformers), are capable of understanding the semantic meaning and context of text, making them ideal for tasks like CV analysis.

## Models Used
### BERT (Bidirectional Encoder Representations from Transformers)
BERT is a transformer-based NLP model developed by Google. It has been pre-trained on large text corpora using a self-supervised learning approach. BERT can capture rich contextual information from text data, enabling it to understand the nuances and semantics of language. In our project, we use the `TFBertModel` implementation of BERT from the Hugging Face Transformers library.

### Cosine Similarity
Cosine similarity is a metric used to measure the similarity between two vectors by calculating the cosine of the angle between them. In our project, we use cosine similarity to quantify the similarity between the encoded representations of a candidate's CV and a job description. A higher cosine similarity score indicates a greater degree of compatibility between the CV and the job description.

## How It Works
1. **Text Encoding**: 
   - The job description and the candidate's CV are tokenized and encoded using the BERT tokenizer.
   - The encoded representations of the text are fed into the BERT model, which processes them through multiple transformer layers.

2. **Semantic Representation**:
   - The BERT model produces dense numerical representations (embeddings) of the input text, capturing their semantic meaning and context.

3. **Cosine Similarity Calculation**:
   - The cosine similarity between the encoded representations of the job description and the CV is calculated using the cosine similarity metric.
   - This similarity score indicates the degree of compatibility between the candidate's CV and the job description.

4. **Compatibility Score**:
   - The compatibility score is expressed as a percentage, indicating the extent to which the candidate's skills and experience align with the requirements of the job.

## Usage
To use the CV Compatibility Checker:
1. Input the job description and the candidate's CV text.
2. The tool will analyze the compatibility between the CV and the job description and provide a compatibility score.
3. Based on the compatibility score, recruiters can make informed decisions about the suitability of the candidate for the job role.

## Dependencies
- `transformers`: Provides access to pre-trained BERT models and tokenizers.
- `tensorflow`: TensorFlow backend for deep learning operations.
- `scikit-learn`: Provides cosine similarity calculation for compatibility assessment.

## Installation
To install the required dependencies, run:
```
pip install -r requirements.txt
```

## Acknowledgements
- This project utilizes the Hugging Face Transformers library.
- Special thanks to the developers and contributors of BERT and the Transformers library for their pioneering work in natural language processing.

## Contact
For any inquiries or feedback, please contact [taha_zafar@hotmail.com].
