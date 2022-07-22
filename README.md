# multilingual-relation-extraction-transformers

## Task
Relation extraction is an important and well explored problem in NLP. Given a sentence and a pair of entities from the sentence, it requires to predict the relation between the two.

Despite recent interest in deep generative models, for Indian languages, relation classification is still under explored due to the unavailability of tagged data.

Here the challenge is to predict the relation between two entities in a sentence for three Indian languages (Bengali, Telugu and Hindi) from a limited tagged training data. We provide training instances for each language across 25 relations.

## Approach
1. Finetune pretrained multilingual transformer models that have had Indian languages in their training phase. For this, we chose mBERT and XLM-Roberta. 
2. Final solution is the ensemble of these models. First, do a polyak averaging for each of the models to get a more regularized model and then ensemble them
