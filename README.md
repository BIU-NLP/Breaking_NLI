# Breaking NLI
## NLI test set with lexical inferences

### Overview

This dataset consists of 8193 premise-hypothesis sentence-pairs annotated to entailment, contradiction, and neutral. The premise and the hypothesis are identical except for one word/phrase that was replaced. This dataset is meant for testing methods trained to solve the natural language inference task, and it requires some lexical and world knowledge to achieve reasonable performance on it.

## Fields

* *sentence1:* The premise sentence.
* *sentence2:* The hypothesis sentence, which is the same as the premise except for one word/phrase that was replaced.
* *annotator_labels:* These are all of the individual labels from the three annotators. 
* *gold_label:* This is the label chosen by the majority of annotators.
* *pairID:* A unique identifier for each sentence1--sentence2 pair.
* *category:* This category sematically groups the replaced words.

### Data Source

The premise sentences are taken from the Stanford Natural Language Inference corpus:

	Samuel R. Bowman, Gabor Angeli, Christopher Potts, and Christopher D. Manning. 2015.
	A large annotated corpus for learning natural language inference. 
	Proceedings of the 2015 Conference on Empirical Methods in Natural Language Processing (EMNLP).

```
@inproceedings{snli:emnlp2015,
		Author = {Bowman, Samuel R. and Angeli, Gabor and Potts, Christopher, and Manning, Christopher D.},
		Booktitle = {Proceedings of the 2015 Conference on Empirical Methods in Natural Language Processing (EMNLP)},
		Publisher = {Association for Computational Linguistics},
		Title = {A large annotated corpus for learning natural language inference},
		Year = {2015}}
```
		
### Statistics

```
Sentence pairs: 8193
Labels: {'entailment': 982 'neutral': 47, 'contradiction': 7164}

Categories: {
'antonyms': 1147, 
'synonyms': 894, 
'cardinals': 759, 
'nationalities': 755, 
'drinks': 731, 
'antonyms_wordnet': 706, 
'colors': 699, 
'ordinals': 663, 
'countries': 613, 
'rooms': 595, 
'materials': 397, 
'vegetables': 109, 
'instruments': 65, 
'planets': 60}
```

### Citation

If you use this dataset in any published research, please cite:

```
@InProceedings{glockner_acl18,
  author    = {Glockner, Max and Shwartz, Vered and Goldberg, Yoav},
  title     = {Breaking NLI Systems with Sentences that Require Simple Lexical Inferences},
  booktitle = {The 56th Annual Meeting of the Association for Computational Linguistics (ACL)},
  month     = {July},
  year      = {2018},
  address   = {Melbourne, Australia}
}
```

### License

This dataset is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-sa/4.0/).

### Comments

* The method we used for estimating human performance is based on Gong et al. (2018), and its description is only available in a [previous version](https://arxiv.org/pdf/1709.04348v1.pdf) of that paper.
