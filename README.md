# spacy-star-trek
spaCy 3.0 project experiments with Star Trek NER data

```python -m spacy project clone -b main -r https://github.com/chssch/spacy-star-trek ner_tng```
```cd ner_tng```
```python -m spacy project assets```


```python -m spacy project run all```


### Model usage:
```
import spacy

nlp = spacy.load("ner_star_trek_tng/training/model-best/")

doc = nlp("We are the Borg. Existence, as you know it, is over.")

print([(ent.label_, ent) for ent in doc.ents])
# [('ALIEN_SPECIES', Borg)]
```
