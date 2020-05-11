# Doc-substructure-NMT

This repository contains the datasets used in [Document Sub-structure in Neural Machine Translation](https://arxiv.org/abs/1912.06598) (Dobreva, Zhou and Bawden, 2020).

We release parallel datasets in three language pairs: French-English, Bulgarian-English and Chinese-English. The parallel data has been extracted from Wikipedia dumps and aligned, preserving the section structure of Wikipedia articles. We also release monolingual data for each of the four languages. For more details on the creation of the corpora, please refer to the above paper.

## Format

### Parallel data
The parallel data is divided into training, dev and test sets. For each language pair, two test sets are available based on what language the original Wiki article was written in, e.g. whether it was written in French and then translated into English, or written in English and translated into French. All parallel data is in tab-separated files containing the following fields:
  - Wiki page title
  - Section title in {Fr,Bg,Zh}
  - Section title in English
  - {Fr,Bg,Zh} sentence 
  - En sentence
  
Examples:
```
Jakob Ackeret   Biographie              Birth and education             Jakob Ackeret est né en Suisse en 1898.                                               Jakob Ackeret was born in 1898 in Switzerland.
Paolo Isnardi   Style                   Style                           Isnardi a écrit plusieurs lamentations, des madrigaux, des messes et des psaumes.     Isnardi wrote several lamentations, madrigals, masses, and psalms.
Ruth Arnon      Carrière scientifique   Career as a Scientist|Overview  Ruth Arnon rejoint le Weizmann Institute of Science en 1960.                          Ruth Arnon joined the Weizmann Institute of Science in 1960.
```

### Monolingual data
Monolingual data is in tab-separated files containing the following fields:
  - Wiki page title
  - Section title
  - Sentence
  
Examples:
```
Cythna Lindenberg Letty Biographie              En 1973, elle a reçu un doctorat honorifique en droit de l'Université de Witwatersrand.
Girard la Pucelle       Carrière                En 1167, Girard écrivit à Thomas Becket pour réaffirmer sa loyauté envers lui, et il l'informa des événements en Allemagne.
Amina Annabi            Biographie|Chanteuse    Cette dernière remporte donc le concours tandis qu'Amina se voit rétrogradée à la seconde place.
```

### Notes on formatting
The initial section in Wikipedia articles introducing the object of the entry does not have a title. We have used the dummy title "Introduction" for all sentences from this initial section regardless of the language.

## Publications

If you use these corpora, please cite the paper:

Radina Dobreva, Jie Zhou, Rachel Bawden (2020). Document Sub-structure in Neural Machine Translation. In Proceedings of the Twelfth International Conference on Language Resources and Evaluation (LREC 2020).

```
  @InProceedings{doc-substructure-nmt,
  author = {Radina Dobreva and Jie Zhou and Rachel Bawden},
  title = {Document Sub-structure in Neural Machine Translation},
  booktitle = {Proceedings of the Twelfth International Conference on Language Resources and Evaluation (LREC 2020)},
  year = {2020}
  }
```
