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
  
### Monolingual data
Monolingual data is in tab-separated files containing the following fields:
  - Wiki page title
  - Section title
  - Sentence
  
### Notes on formatting
The initial section in Wikipedia articles introducing the object of the entry does not have a title. We have used the dummy title "Introduction" for all sentences from this initial section regardless of the language.
