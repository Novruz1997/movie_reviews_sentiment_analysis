# Sentiment Analysis on Movie Review dataset from NLTK

NLTK is a Python package for NLP. You can get more information from [NLTK](https://www.nltk.org/) website.

NLTK is used for text preprocessing and feature engineering. Sklearn is used as a helper library to perform Sentiment Analysis. 

For Feature Generation, NLTK already has a built-in, pretrained sentiment analyzer called [VADER](http://www.nltk.org/howto/sentiment.html) (Valence Aware Dictionary and sEntiment Reasoner).

## USAGE

```python
from nltk.sentiment import SentimentIntensityAnalyzer

sia  = SentimentAnalyzer()

sia.polarity_scores('NTLK is one of the most popular NLP library with too many features')  # returns positive %, negative %, compound %

## License

[MIT](https://choosealicense.com/licenses/mit/)

