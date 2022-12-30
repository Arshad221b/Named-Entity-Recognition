# Named-Entity-Recognition
Huggigface RoBERTa model implementation for NER on conll2003 dataset. 

<h3>Flow of the program:</h3> 
<p> 1. Importing data using Huggingface Dataset </p>
<p> 2. Tokenisation of sentences </p>
<p> 3. Importing pre-trained model from huggingface hub </p>
<p> 4. Training the model using Trainer Fuction </p>
<p> 5. Inference using Huggingface Pipeline </p>

```
from transformers import pipeline
nlp = pipeline("ner", model=model_, tokenizer=tokenizer)
example = "My name is Wolfgang and I live in Berlin"

ner_results = nlp(example)
print(ner_results)
```
Ouput
```
[{'entity': 'B-PER', 'score': 0.84195936, 'index': 4, 'word': 'wolfgang', 'start': 11, 'end': 19}, {'entity': 'B-LOC', 'score': 0.9583987, 'index': 9, 'word': 'berlin', 'start': 34, 'end': 40}]
```
