# # BodoBERT and BodoPoS


Part of Speech Tagger for Bodo Language using BiLSTM-CRF with Transformer-based Language Model BodoBERT

This repository contains pre-trained vanilla BERT model and POS tagging model for Bodo Language.

## Requirements

* It requires python 3.6+
* Install [Flair](https://github.com/flairNLP/flair) preferably  in in favorite virtual environment, 

## How to run

<!--  Download the pre-trained BERT model from the link [BodoBERT](https://iitgoffice-my.sharepoint.com/:f:/g/personal/drbj153_iitg_ac_in/Et9_2NXTa81Plm8qgIUqqs4BQSiUgfvFMALoJlXwMY23Aw?e=z35g8I) (This is not required for running the POS tagging model) -->

Download the pre-trained Bodo POS tagging model from the link- [BodoPOS](https://iitgoffice-my.sharepoint.com/:u:/g/personal/drbj153_iitg_ac_in/ET9XJhlMgrBKkqzVtAUXKiIBt2a9ur28f5Z7a1UaxWfdNQ?e=8OGT4F)


```
from flair.models import SequenceTagger
from flair.data import  Sentence, Token

# Load the tagger

model = SequenceTagger.load('BodoPOS.pt')

#  create example sentence
sen='स्नि साननि उनाव आरोबाव बे सि-जोमफोरखौ गानफिननानै मोसायै मुसुरै शनि फुजा खुंफिनो । '
sentence = Sentence(sen)

# predict tags and print
model.predict(sentence)
print(sentence.to_tagged_string())

```


