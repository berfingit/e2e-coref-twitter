## The Corpora
The OntoNotes[1] and the TwiConv[2] corpora are used in the experiments done for the paper *Adapting Coreference Resolution to Twitter
Conversations*.
The files which are used from the OntoNotes corpus are given in ontonotes_files_used.txt.

The TwiConv corpus is shared in the repository https://github.com/berfingit/TwiConv. Please refer to the corpus' repository for the instructions on how to reproduce the corpus. The conll format we applied in this paper is slightly different than the corpus' distributed version. Therefore,
before the construction of the corpus, the conll_skeleton/ folder and the make_conll.py script in the TwiConv distribution should 
replaced by the versions we share in this repository.

The annotations in Twiconv corpus conform with the Ontonotes annotation style except for the annotation of verb mention,
which are annotated in OntoNotes but not in TwiConv corpus.

The list of the files used in train and test sets is provided in files_for_paper.docx. 


## USAGE

Here you will get instruction on how to get the train and test sets used for the experiments.


### Split into train and test set

To split into training and test sets used in re-training e2e (Lee et al, 2018), run ``python split_test_train.py <PATH TO CONLL FILES>``, the file format will appear in ``train`` and ``test``


### The CoNLL format

The CoNLL format for the corpus is inspired by the original CoNLL-2012 format with some differences.
Empty lines indicate sentence breaks.

```
COLUMN	CONTENT
0 		Thread ID
1 		Thread number
2 		Token number in sentence
3 		Token
4 		POS tag
5 		Parse info
6 		[always -]
7 		[always -]
8 		[always -]
9 		Speaker/User handle
10		Named entity type
12		Coreference ID
```

## References
[1] Sameer Pradhan, Lance Ramshaw, Ralph Weischedel, Jessica Macbride, and Linnea Micciulla. 2007. Un-restricted Coreference: Identifying Entities and Events in OntoNotes. International Conference on Semantic Computing, 0:446–453.
[2] Berfin Aktaş and Annalena Kohnert. TwiConv: A Coreference-annotated Corpus of Twitter Conversations. In Proceedings of the Third Workshop on Computational Models of Reference, Anaphora and Coreference (CRAC@COLING), 47–54. Barcelona, Spain, December 2020. Association for Computational Linguistics.
