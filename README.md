# Twitter-HateSpeech-Detector

Hi. thanks for stopping by!

This is a personal project I have been working on over the last 2 months which detects potentially hateful speech in Twitter comments. To do this, I trained a Machine Learning model using a dataset CSV file with ~10,000 tweets and tested it with a series of files each with ~1000 tweets. The datasets used for this project can be found as files within this repositary. 

## Overview

To start with, I wrote a script which 'cleans' the tweets ready for further processing (lemmatisation, stemming, removal of stop words, etc.). Then for the preprocessing step, I used a bag-of-words model to simplify the repesentation of text in tweets (model disregards grammar, word-order, etc. but keeps multiplicity of words https://en.wikipedia.org/wiki/Bag-of-words_model). I then based my model using a Long Short-Term Memory model, LSTM, a recurrent neural network (https://en.wikipedia.org/wiki/Long_short-term_memory) - something I had experiecing using in one of my other projects (https://github.com/os717/news_headlines_trader) and wanted to try again in a different context.

## Results

Testing has showed that my latest model successfully ignores 81% of benign tweets and identifies 73% of hateful tweets. It was intersting to notice that, when tuning the model, there was often an inverse retionship between successfully identifying hateful comments and sucessfully ignoring non-hateful comments (which potentially poses difficult societal questions for how we should deal with hate-speech - should we lean towards wrongly flagging benign comments in order to ensure hateful comments are always flagged, or should we prioritise never flagging benign comments but accept that some hateful comments may fall through the gaps). 

## Next Steps

At the moment, I am currently investigating ways of reducing the false-positive rate for flagging the hateful speech by incorporating sarcasm/humour detection into the model. 

### All in all, this has been a really interesting project. Just wanted to share my progress ;) - stay tuned for updates.

