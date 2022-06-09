# Paraphrase detection
## About
Paraphrase detection is the task to define whether *two formally different texts have the same (or similar) meaning*.
This notebook deals with **sentence-level paraphrases** from [Paraphraser corpus](http://paraphraser.ru/download/). 

The Paraphraser corpus contains sentence pairs obtained from the Russian news headlines (РИА Новости, Лента.ру, Российская газета, РБК) with crowdsourced annotation [Pivovarova et al., 2017](https://helda.helsinki.fi/bitstream/handle/10138/232301/AINL2017_paper_24.pdf?sequence=1). 

Paraphrase classes include:
* 1 - non-paraphrases
* 0 - loose paraphrases (similar meaning)
* 1 - strict paraphrases (same meaning)

No specific criteria on the distinction between loose and strict paraphrases are provided by the creators of the corpus, so we take it as is.

## Structure
In the notebook with [paraphrase detection algorithm](https://github.com/annatrn0/paraphrase_detection/blob/main/Paraphrase_detection.ipynb) we try to detect 7 syntactic and 7 lexic transformations which lead to a paraphrase. Some functions which detect a transformation require txt files that are stored in [data](https://github.com/annatrn0/paraphrase_detection/tree/main/data) (they are also incorporated into the ipynb file so you don't have to dowload them to run the code). Each sentence pair is viewed as a number of transformations. These transformations serve as features for the future classification model.

We perform two-class and three-class classification with a number of models.
