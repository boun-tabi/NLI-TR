###### For English click [here](https://github.com/boun-tabi/NLI-TR).
___
# 📜 NLI-TR
NLI-TR veri kümesi [SNLI](https://nlp.stanford.edu/projects/snli/ ) ve [MultiNLI](https://www.nyu.edu/projects/bowman/multinli/) isimli iki büyük ölçekli İngilizce veri kümesinin [Amazon Translate](https://aws.amazon.com/tr/translate/) servisi aracılığıyla Türkçeye tercüme edilerek elde edilen bir veri kümesidir.  Türkçe veri kümesindeki cümlelerin orjinal İngilizce cümlelerine iki veri kümesinde de yer alan ortak anahtar alan (pairID) kullanılarak erişilebilir.

Veri kümesinin özelliklerine [buradan](https://arxiv.org/abs/2004.14963) ulaşılabilir, NLI çalışma alanı ile ilgili genel bilgilere [CS224U ders videolarından](https://www.youtube.com/watch?v=M_VPUF9ResU&list=PLoROMvodv4rObpMCir6rNNUlFAn56Js20&index=8 "Lectures – NLI | Stanford CS224U: Natural Language Understanding | Spring 2019") ulaşılabilir.

## 📜 SNLI-TR
[SNLI-TR 1.0](#-nli-tr-indir) ve [SNLI-TR 1.1](#-nli-tr-indir) (~44MB, zip)  orjinal [SNLI 1.0](https://nlp.stanford.edu/projects/snli/snli_1.0.zip "The Stanford Natural Language Inference (SNLI) Corpus") (~100MB, zip) veri kümesinin Türkçe tercümesidir (YSA). Sürüm 1.0'dan farklı olarak Sürüm 1.1'de (`translation_annotations`) anahtar alanı içerisinde tercüme kalitesine dair değerlendirme bilgileri yer almaktadır.

SNLI veri kümesinden bir örnek:
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
        "sentence2_parse": "(ROOT (S (NP (DT A) (NN woman)) (VP (VBZ is) (PP (IN in) (NP (DT the) (JJ hosptial) (NN working)))) (. .)))"
}
</pre>

SNLI-TR veri kümesindeki karşılığı:
<pre>
{
        "annotator_labels": [
            "neutral"
        ],
        "captionID": "4688994030.jpg#3",
        "gold_label": "neutral",
        "pairID": "4688994030.jpg#3r1n",
        "sentence1": "Hastanede maske takan bir sağlık görevlisi.",
        "sentence2": "Hastanede çalışan bir kadın var."
}
</pre>
 
 #### 🏷 SNLI-TR License
 
SNLI-TR veri kümesi, orjinal SNLI veri kümesi ile aynı şekilde [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/ "Creative Commons Attribution-ShareAlike 4.0 International License") lisansına sahiptir.

***

## 📜 MultiNLI-TR
[MultiNLI-TR 1.0](#-nli-tr-indir) ve [MultiNLI-TR 1.0](#-nli-tr-indir) (~72MB, zip) veri kümeleri orjinal [MultiNLI 1.0](https://cims.nyu.edu/~sbowman/multinli/multinli_1.0.zip "The Multi-Genre NLI Corpus") (~216MB, zip) veri kümesinin Türkçe tercümesidir (YSA). Sürüm 1.0'dan farklı olarak Sürüm 1.1'de (`translation_annotations`) anahtar alanı içerisinde tercüme kalitesine dair değerlendirme bilgileri yer almaktadır.

MultiNLI veri kümesinden bir örnek:

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

MultiNLI-TR veri kümesindeki karşılığı:
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
 
MultiNLI-TR veri kümesi, orjinal MultiNLI veri kümesi ile aynı lisansa sahip olup detaylarına [MultiNLI makalesi](https://www.nyu.edu/projects/bowman/multinli/paper.pdf) üzerinden ulaşılabilir. 


## :heavy_check_mark: Annotations

Tercüme kalitesinin değerlendirildiği örnekler için değerlendirme bilgileri aşağıda SNLI-TR veri kümesinden bir örnekle gösterildiği gibi `translation_annotations` isimli anahtar alan içerisinde yer almaktadır.  
<pre>
{
        "annotator_labels": [
            "entailment"
        ],
        "captionID": "6925887658.jpg#3",
        "gold_label": "entailment",
        "pairID": "6925887658.jpg#3r1e",
        "sentence1": "İki futbolcu topu almak için yarışıyor.",
        "sentence2": "İki futbolcu bir futbol maçında oynuyor",
        "translation_annotations": {
            "annotator_ids": [
                1,2,5,8,10
            ],
            "annotator_labels": [
                "entailment","entailment","entailment","entailment","entailment"
            ],
            "translation_scores": [
                5,5,4,5,5
            ],
            "gold_label": "entailment"
        }
}
</pre>

`translation_annotations` alanı içerisinde yer alan anahtar alanların açıklamalarına aşağıda ulaşılabilir.
 
* `annotator_ids`: Tercüme kalitesini değerlendiren kişilerin tekil numaraları.
* `annotator_labels`: Tercüme sonrasında cümle çiftleri arasında gözlemlenen NLI etiketleri. Tercüme kalitesinin kritik düzeyde düşük olduğu örneklerde `"broken"` etiketi verilmiştir.
* `translation_scores`: Tercüme kalitesine dair Lickert ölçeği [1-5] ile verilen değerlendirme skorları.
* `gold_label`: Mutlak çoğunluğu sağlayan etiket (`majority-level`).  Mutlak çoğunluğun sağlanamadığı durumda veya kritik tercüme problemlerinin yer aldığı cümle çiftlerinde bu alanda `"broken"` etiketi yer almaktadır.

Karşılaştırma açısından SNLI veri kümesindeki karşılığı:

<pre>
{
   "annotator_labels":[
      "entailment"
   ],
   "captionID":"6925887658.jpg#3",
   "gold_label":"entailment",
   "pairID":"6925887658.jpg#3r1e",
   "sentence1":"Two soccer players are vying for the ball.",
   "sentence1_binary_parse":"( ( Two ( soccer players ) ) ( ( are ( vying ( for ( the ball ) ) ) ) . ) )",
   "sentence1_parse":"(ROOT (S (NP (CD Two) (NN soccer) (NNS players)) (VP (VBP are) (VP (VBG vying) (PP (IN for) (NP (DT the) (NN ball))))) (. .)))",
   "sentence2":"Two soccer players are playing in a soccer match",
   "sentence2_binary_parse":"( ( Two ( soccer players ) ) ( are ( playing ( in ( a ( soccer match ) ) ) ) ) )",
   "sentence2_parse":"(ROOT (S (NP (CD Two) (NN soccer) (NNS players)) (VP (VBP are) (VP (VBG playing) (PP (IN in) (NP (DT a) (NN soccer) (NN match)))))))"
} 
</pre>


## 📚 Kaynaklar 

### 📖 NLI-TR indir

#### 🔗 Linkler
* [SNLI-TR 1.0](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/snli_tr_1.0.zip) and [SNLI-TR 1.1](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/snli_tr_1.1.zip) (~44MB, zip).
* [MultiNLI-TR 1.0](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/multinli_tr_1.0.zip) and [MultiNLI-TR 1.1](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/multinli_tr_1.1.zip) (~72MB, zip)

#### 🤗 HuggingFace datasets
```py
from datasets import load_dataset

snli_tr_dataset = load_dataset('nli_tr', 'snli_tr')
multinli_tr_dataset = load_dataset('nli_tr', 'multinli_tr')
```
* Örnek uygulama 👉 [![Colab demo](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1vuKlI8Q5ZlDnf2fhFs_-WnjUhuuyUuCp?usp=sharing) . 

### 🔬 Tekrarlanabilirlik 

Tüm kodlara, modellere ve örnek girdi verilerine [buradan](https://drive.google.com/drive/folders/1Wo4XzYzVOWDFwFvnfDBzYoNGXYsV_xcz?usp=sharing) ulaşabilirsiniz.  Merak ettiğiniz tüm sorularınız için her zaman bize ulaşabilirsiniz. 


## ✒ Künye 

>[Emrah Budur](https://scholar.google.com/citations?user=zSNd03UAAAAJ), [Rıza Özçelik](https://www.cmpe.boun.edu.tr/~riza.ozcelik), [Tunga Güngör](https://www.cmpe.boun.edu.tr/~gungort/)  and [Christopher Potts](https://web.stanford.edu/~cgpotts). 2020. 
Data and Representation for Turkish Natural Language Inference. To appear in Proceedings of EMNLP. [[pdf]](https://arxiv.org/abs/2004.14963) [[bib]](https://tabilab.cmpe.boun.edu.tr/datasets/nli_datasets/nli-tr.bib)

```
@inproceedings{budur-etal-2020-data,
    title = "Data and Representation for Turkish Natural Language Inference",
    author = "Budur, Emrah and
      \"{O}z\c{c}elik, R{\i}za and
      G\"{u}ng\"{o}r, Tunga",
    booktitle = "Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing",
    month = nov,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics"
}
```

## ❤ Teşekkürler 

Bu araştırma _AWS Cloud Credits for Research Program (önceki adıyla AWS Research Grants)_ tarafından desteklenmiştir. Bu çalışma süresince değerli katkıları ve kalite değerlendirme destekleri için _Alara Dirik, Almira Bağlar, Berfu Buyüköz, Berna Erden, Fatih Mehmet Güler, Gökçe Uludoğan, Gözde Aslantaş, Havva Yüksel, Melih Barsbey, Melike Esma İlter, Murat Karademir, Ramazan Pala, Selen Parlar, Tuğçe Ulutuğ, Utku Yavuz_'a çok teşekkür ederiz. Ek olarak _Stefan Schweter_ and _Kemal Oflazer_ Hocaya BERTurk modelinin eğitildiği veri kümesini bizimle paylaştıkları için müteşekkiriz. Ayrıca Stanford NLP Lab çatısı altındaki _Omar Khattab_, _Dallas Card_, _Yiwei Luo_ ve diğer pek çok seçkin araştırmacılara değerli tavsiyeleri, görüş alışverişleri için çok teşekkür ederiz.  Ayrıca anonim hakemlerimize faydalı yorumları ve geliştirici geribildirimleri için çok teşekkür ederiz.

## 📧 Bize ulaşın 

Tüm soru, öneri ve geribildirimleriniz için bize ulaşabilirsiniz ([Emrah Budur](mailto:emrah.budur@boun.edu.tr), 
[Rıza Özçelik](mailto:riza.ozcelik@boun.edu.tr)).

## 📢 Duyurular

🎮 (2020-11-18) Kelime oyunu! Bu sayfaya "hayat kurtaran" bazı ifadeler sakladık🙂  Bu ifadeleri bulup [bu tweet](https://twitter.com/ebudur/status/1329417872108621825) üzerinden alıntı veya cevap vererek paylaşan bir kişiye bir sürprizimiz 🎁 var🙂 Son katılım zamanı: 20 Kasım 20 2020 saat 23:59 (UTC)!

💬 (2020-11-18) MAkalemizin [EMNLP 2020](https://2020.emnlp.org) konferansındaki [Gather.town](https://www.virtualchair.net/events/emnlp2020) oturumu 18 Kasım 2020 tarihinde saat 18:00-20:00 (UTC)'de B Odasında gerçekleştirilecektir.  Sorularınızı merakla bekliyoruz 🙂 

🎯 (2020-06-01) Çalışmamızın _"Data and Representation for Turkish Natural Language Inference"_ başlıklı yeni sürümü [EMNLP 2020](https://2020.emnlp.org) konferansına gönderildi. 

🐣 (2020-09-14) Makalemiz [EMNLP 2020](https://2020.emnlp.org) ana konferansına kabul edildi 🙂 Çalışma boyunca destek veren herkese minnettarız 🤗 
