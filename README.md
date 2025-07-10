# Applying NLP for Topic Modelling to Analyse Gym Reviews

This project uses Natural Language Processing (NLP) techniques to analyse customer reviews from PureGym, with the goal of uncovering what motivates members to join, stay, or leave. By applying topic modelling and emotion analysis, the project supports customer-centric decision-making in areas like experience design, retention strategy, and operational improvement.

---

## Business Context

PureGym aims to provide a low-cost, inclusive fitness experience at scale. Understanding what members value, complain about, or emotionally respond to is key to:
- Enhancing member engagement and satisfaction
- Informing improvements to gym operations, app usability, and customer service
- Tailoring marketing and retention messaging to emotional drivers

---

## Objectives

- Identify common themes and concerns in customer reviews using topic modelling
- Detect underlying emotional sentiment to uncover customer motivations
- Generate insights that can inform product and operations strategy

---

## Notebooks

- [`topic_modelling_bertopic.ipynb`](./topic_modelling_bertopic.ipynb)  
  Main workflow using BERTopic, Hugging Face emotion analysis, and LLM summarisation.

- [`topic_modelling_lda_gensim.ipynb`](./topic_modelling_lda_gensim.ipynb)  
  Early-stage experimentation with traditional LDA via Gensim.  

---

## Data Loading Note

To avoid code duplication across notebooks, core data cleaning and EDA were completed in the BERTopic notebook. The processed review data is loaded into the Gensim LDA notebook using `.pkl` files saved from that initial step.

This is due to constraints with Gensim compatibility.

---

## Methods & Tools

- **Topic Modelling**: BERTopic and LDA (Gensim)
- **Emotion Detection**: Hugging Face Transformers (DistilRoBERTa emotion model)
- **Language Models**:  Large Language Models (LLMs) for summarisation and generating insights
- **Data Prep & Analysis**: Python, Pandas, NLTK, spaCy
- **Visualisation**: Matplotlib

---

## Context: Why Use LDA with Gensim?

Latent Dirichlet Allocation (LDA) is a well-established topic modelling method and was included here as part of the original academic brief. In this project, I tested LDA (using Gensim) early in the process as a baseline for comparison. However, due to:
- Lower topic coherence
- More limited visualisation capabilities
- Practical issues running Gensim consistently in Colab environments

I chose to use **BERTopic**, which provided more meaningful outputs and better suited the business context of this analysis.

This notebook is included to demonstrate comparative exploration but is not used in the final insight generation.

---

## Key Results

- Extracted 10+ interpretable topics from thousands of reviews — including app complaints, cleanliness, staff behaviour, contract terms, and facility quality
- Detected emotion clusters such as:
  - Frustration with staff responsiveness, equipment maintenance and facility cleanliness
- Used LLMs to generate actionable insights that address common customer complaints

---

## Business Value

This approach enables fitness brands like PureGym to:
- Prioritise issues that drive negative sentiment and attrition
- Tailor improvements to customer emotional drivers
- Automate large-scale review analysis for strategic planning

---

## Next Steps

- Integrate topic & sentiment trends into a real-time dashboard
- Correlate insights with retention and churn metrics
- Segment insights by location or demographic

---

## File Structure

puregym-nlp-topic-modelling/
│
├── README.md                            # Project overview 
├── topic_modelling_bertopic.ipynb       # Main Jupyter notebook with main workflow + final outputs
├── topic_modelling_lda_gensim.ipynb     # Alternate method for comparison
├── requirements.txt                     # Libraries used
└── .gitignore                 

---

## Contact

Created by [Matt Cocker]  
Feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/matt-cocker-b77b49216/) or view other projects at [github.com/matt-cocker](https://github.com/matt-cocker)
