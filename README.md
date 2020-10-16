# 📜 NLI-TR
The Natural Language Inference in Turkish (NLI-TR) is a set of two large scale datasets that were obtained by translating the foundational NLI corpora ([SNLI](https://nlp.stanford.edu/projects/snli/ "The Stanford Natural Language Inference (SNLI) Corpus") and [MultiNLI](https://www.nyu.edu/projects/bowman/multinli/ "The Multi-Genre NLI Corpus")) using [Amazon Translate](https://aws.amazon.com/tr/translate/ "Amazon Translate NMT service").  The English sentences of the datasets can be accessed from the original corpus by using their common identifier key (pairID).

The characteristics of the datasets can be reviewed in [the arXiv paper](https://arxiv.org/abs/2004.14963) and the details of the NLI task can be reviewed in [the lectures videos of CS224U](https://www.youtube.com/watch?v=M_VPUF9ResU&list=PLoROMvodv4rObpMCir6rNNUlFAn56Js20&index=8 "Lectures – NLI | Stanford CS224U: Natural Language Understanding | Spring 2019").  

## 📜 SNLI-TR
The [SNLI-TR 1.0](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/snli_tr_1.0.zip "The Turkish Translation of The Stanford Natural Language Inference (SNLI) Corpus") and [SNLI-TR 1.1](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/snli_tr_1.1.zip "The Turkish Translation of The Stanford Natural Language Inference (SNLI) Corpus") (~44MB, zip) are the Turkish translation (NMT) of the original [SNLI 1.0](https://nlp.stanford.edu/projects/snli/snli_1.0.zip "The Stanford Natural Language Inference (SNLI) Corpus") (~100MB, zip).  The only difference between the version 1.0 and 1.1 is that the latter includes and additional key field (`translation_annotations`) containing the evaluations of translations for some of the examples.

An example from SNLI:
<pre>
{
        "annotator_labels": [
            "neutral"
        ],
        "captionID": "4688994030.jpg#3",
        "gold_label": "neutral",
        "pairID": "4688994030.jpg#3r1n",
        "sentence1": "A medical worker wearing a mask in the hospital.",
        "sentence1_binary_parse": "( ( ( A ( medical worker ) ) ( wearing ( ( a mask ) ( in ( the hospital ) ) ) ) ) . )",
        "sentence1_parse": "(ROOT (NP (NP (DT A) (JJ medical) (NN worker)) (VP (VBG wearing) (NP (NP (DT a) (NN mask)) (PP (IN in) (NP (DT the) (NN hospital))))) (. .)))",
        "sentence2": "A woman is in the hosptial working.",
        "sentence2_binary_parse": "( ( A woman ) ( ( is ( in ( the ( hosptial working ) ) ) ) . ) )",
        "sentence2_parse": "(ROOT (S (NP (DT A) (NN woman)) (VP (VBZ is) (PP (IN in) (NP (DT the) (JJ hosptial) (NN working)))) (. .)))",
        "promptID": 90816
}
</pre>

The corresponding Turkish translation in SNLI-TR:
<pre>
{
        "annotator_labels": [
            "neutral"
        ],
        "captionID": "4688994030.jpg#3",
        "gold_label": "neutral",
        "pairID": "4688994030.jpg#3r1n",
        "sentence1": "Hastanede maske takan bir sağlık görevlisi.",
        "sentence2": "Hastanede çalışan bir kadın var.",
        "promptID": 90816
}
</pre>
 
 #### 🏷 SNLI-TR License
 
SNLI-TR licensed under the same terms as SNLI which is [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/ "Creative Commons Attribution-ShareAlike 4.0 International License").

***

## 📜 MultiNLI-TR
The [MultiNLI-TR 1.0](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/multinli_tr_1.0.zip "The Turkish Translation of The Multi-Genre NLI Corpus") and [MultiNLI-TR 1.1](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/multinli_tr_1.1.zip "The Turkish Translation of The Multi-Genre NLI Corpus") (~41MB, zip) are the Turkish translation (NMT) of the original [MultiNLI 1.0](https://cims.nyu.edu/~sbowman/multinli/multinli_1.0.zip "The Multi-Genre NLI Corpus") corpus (~216MB, zip). The only difference between the version 1.0 and 1.1 is that the latter includes an additional key field (`translation_annotations`) containing the evaluations of translations for some of the examples.   

An example from MultiNLI:

<pre>
{
        "annotator_labels": [
            "neutral"
        ],
        "genre": "telephone",
        "gold_label": "neutral",
        "pairID": "48889n",
        "promptID": "48889",
        "sentence1": "and uh then you'd be willing to give up your job to <ins><b>stay home</b></ins> and with or stay with the children",
        "sentence1_binary_parse": "( and ( uh ( then ( you ( 'd ( be ( willing ( to ( ( give up ) ( your ( job ( to ( ( ( stay ( ( home and ) with ) ) or ) ( stay ( with ( the children ) ) ) ) ) ) ) ) ) ) ) ) ) ) ) )",
        "sentence1_parse": "(ROOT (FRAG (CC and) (NP (NP (NNP uh)) (SBAR (S (ADVP (RB then)) (NP (PRP you)) (VP (MD 'd) (VP (VB be) (ADJP (JJ willing) (S (VP (TO to) (VP (VB give) (PRT (RP up)) (NP (PRP$ your) (NN job) (S (VP (TO to) (VP (VP (VB stay) (UCP (ADVP (RB home)) (CC and) (PP (IN with)))) (CC or) (VP (VB stay) (PP (IN with) (NP (DT the) (NNS children)))))))))))))))))))",
        "sentence2": "Is your dream to <ins><b>stay at home</b></ins>?",
        "sentence2_binary_parse": "( ( ( Is your ) ( dream ( to ( stay ( at home ) ) ) ) ) ? )",
        "sentence2_parse": "(ROOT (SQ (VBZ Is) (NP (PRP$ your)) (NP (NP (NN dream)) (S (VP (TO to) (VP (VB stay) (PP (IN at) (NP (NN home))))))) (. ?)))"
}
</pre>

The corresponding Turkish translation in MultiNLI-TR:
<pre>

{
        "annotator_labels": [
            "neutral"
        ],
        "genre": "telephone",
        "gold_label": "neutral",
        "pairID": "48889n",
        "promptID": "48889",
        "sentence1": "Ve o zaman <ins><b>evde kal</b></ins>mak ya da çocuklarla kalmak için işinden vazgeçersin.",
        "sentence2": "Hayaliniz <ins><b>evde kal</b></ins>mak mı?"
}
</pre>

 #### 🏷 MultiNLI-TR License
 
MultiNLI-TR is licensed under the same terms as MultiNLI which is described in the [MultiNLI paper](https://www.nyu.edu/projects/bowman/multinli/paper.pdf). 
 
## ✒ Citation 

>[Emrah Budur](https://scholar.google.com/citations?user=zSNd03UAAAAJ), [Rıza Özçelik](https://www.cmpe.boun.edu.tr/~riza.ozcelik), [Tunga Güngör](https://www.cmpe.boun.edu.tr/~gungort/)  and [Christopher Potts](https://web.stanford.edu/~cgpotts). 2020. 
Use of Machine Translation to Obtain Labeled Datasets for Resource-Constrained Languages.. arXiv preprint arXiv:2004.14963. [[pdf]](https://arxiv.org/abs/2004.14963) [[bib]](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/nli-tr.bib)

```
@article{NLI-TR-2020-arXiv-2004.14963,
    Author = {Emrah Budur and R{\i}za \"{O}z\c{c}elik and Tunga G\"{u}ng\"{o}r and Christopher Potts},
    Title = {Use of Machine Translation to Obtain Labeled Datasets for Resource-Constrained Languages},
    Year = {2020},
    Eprint = {arXiv:2004.14963},
}
```

## ❤ Acknowledgment 

This research was supported by the _AWS Cloud Credits for Research Program (formerly AWS Research Grants)_. We thank _Alara Dirik, Almira Bağlar, Berfu Buyüköz, Berna Erden, Fatih Mehmet Güler, Gökçe Uludoğan, Gözde Aslantaş, Havva Yüksel, Melih Barsbey, Melike Esma İlter, Murat Karademir, Selen Parlar, Utku Yavuz_ for 
their annotation support and vital contributions. We are grateful also to _Stefan Schweter_ and _Kemal Oflazer_ for sharing the dataset that BERTurk was trained on, and _Omar Khattab_ from Stanford NLP Lab for valuable advice and discussion.

## 📧 Contact 

Please feel free to contact [Emrah Budur](mailto:emrah.budur@boun.edu.tr) and 
[Rıza Özçelik](mailto:riza.ozcelik@boun.edu.tr) for any questions, comments and feedbacks.

## 📢 Announcements

🎯 (2020-06-01) A new version of our work entitled as _"Data and Representation for Turkish Natural Language Inference"_ was submitted to [EMNLP 2020](https://2020.emnlp.org). 

🐣 (2020-09-14) Our paper has been accepted as a long paper at [EMNLP 2020](https://2020.emnlp.org) 🙂 Grateful to everyone who supported our work along the way 🤗 
