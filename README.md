# selpref-emb
Selectional Preference Embeddings (EMNLP 2017)

This repository contains joint embeddings of selectional preferences, words, and fine-grained entity types.

Download the embeddings here:

* [lemmatized, basicDependencies](https://drive.google.com/open?id=0B5Gn0zIax9GPZGRMZUVFYUZkR2s)
* [lemmatized, enhancedDependencies](https://drive.google.com/open?id=0B5Gn0zIax9GPTkF0dmswNEttQXM)
* [lemmatized, enhancedPlusPlusDependencies](https://drive.google.com/open?id=0B5Gn0zIax9GPc2xoNWxSaUZpVkU)

* [unlemmatized, basicDependencies](https://drive.google.com/open?id=0B5Gn0zIax9GPVEFEbXRTaHR1b28)
* [unlemmatized, enhancedDependencies](https://drive.google.com/open?id=0B5Gn0zIax9GPZkc0U21oRmpsTEE)
* [unlemmatized, enhancedPlusPlusDependencies](https://drive.google.com/open?id=0B5Gn0zIax9GPcmt3Zm52UWJMQWM)

These are in the gensim model format, which can be loaded in Python like this:

```python
from gensim.models import KeyedVectors

model_file = "/path/to/model_file"
KeyedVectors.load_word2vec_format(model_file, binary=True)
```

The vocabulary consists of:

- verbs and their dependency governor separated by "@", e.g. "sink@nsubj" or "elect@dobj"
- words and short noun phrases, e.g. "Titanic"
- fine-grained entity types using the FIGER inventory, e.g.: /product/ship or /person/politician
