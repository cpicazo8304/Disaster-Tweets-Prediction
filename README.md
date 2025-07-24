# Kaggle Competition - [Natural Language Processing with Disaster Tweets]

This repository contains my work for the [Competition Name](https://www.kaggle.com/competitions/nlp-getting-started/overview) on Kaggle.

---

## Competition Description
A short summary of the competition:
- Goal: Predict which tweets are talking about real disasters and which aren't.
- Evaluation metric: F1 scores.
- Data: Contains train.csv and test.csv with train.csv containing 5 columns and test.csv containing 4 columns (no target column). For more information on the data, check out the [data page](https://www.kaggle.com/competitions/nlp-getting-started/data) on Kaggle.

---

## Approach
- **Data Preprocessing:** Analyzed the location feature since it had phrases that did not represent locations, so utilize Name-Entity Recognition to keep only the phrases that represented locations or organizations. Additionally, cleaned up the text and location data by lowercasing and removing punctuation and stop words to then combine the location and text feature to be utilized in the BERT model for training and testing. 
- **Models:** Utilized the roBERTa model provided by Hugging Face transformers library. 
- **Validation:** Validation was done in while training with the Trainer() method (training data was split into validation and training data). 

---

## Results
-**F1 Score**: approximately 80%

---

## Files
- `notebooks/` - Jupyter notebook that includes the data preprocessing and classification code.
- `data/` - Training and testing data for the classification.

---

## Usage
To reproduce results:
```bash
# Clone the repository
git clone https://github.com/cpicazo8304/Disaster-Tweets-Prediction.git
cd Disaster-Tweets-Prediction


# Install dependencies
pip install -r requirements.txt

# Run the notebook or script
jupyter notebook notebooks/nlp-with-disaster-tweets.ipynb
