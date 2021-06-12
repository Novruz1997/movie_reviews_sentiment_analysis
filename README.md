# Sentiment Analysis on Movie Review dataset from NLTK

NLTK is a Python package for NLP. You can get more information from [NLTK](https://www.nltk.org/) website.

NLTK is used for text preprocessing and feature engineering. Sklearn is used as a helper library to perform Sentiment Analysis. 

For Feature Generation, NLTK already has a built-in, pretrained sentiment analyzer called [VADER](http://www.nltk.org/howto/sentiment.html) (Valence Aware Dictionary and sEntiment Reasoner).

## USAGE

```python
from nltk.sentiment import SentimentIntensityAnalyzer

sia  = SentimentAnalyzer()

sia.polarity_scores('NTLK is one of the most popular NLP library with too many features')  # returns positive %, negative %, compound %
```


**Plotting top 100 positive and negative words in corpus**

```python
  def plot_top_100(self, category):
    '''plotting top 100 words either positive or negative'''
    try:
      if category in ['positive', 'negative']:
        if category == 'positive':
          x = WordCloud().generate(' '.join(list(self.top_100_positive)))
          plt.imshow(x, interpolation='bilinear')
          plt.axis('off')
          plt.show()
        else:
          x = WordCloud().generate(' '.join(list(self.top_100_negative)))
          plt.imshow(x, interpolation='bilinear')
          plt.axis('off')
          plt.show()
    except ValueError:
      print('category mush be either positive of negative')
```


![most common 100 negative words is shown](https://github.com/Novruz1997/movie_reviews_sentiment_analysis/blob/main/pics/Screen%20Shot%202021-06-12%20at%205.12.30%20PM.png)


## License

[MIT](https://choosealicense.com/licenses/mit/)

