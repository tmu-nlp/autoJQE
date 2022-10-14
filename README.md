# autoJQE



This repository contains binary patch data for reconstructing dataset for quality estimation of GEC.


## Data
Please pull thse codes on your local space.

```
$ git clone https://github.com/tmu-nlp/ProQE.git
```


The header contains the following columns:
 - `原文`: source sentence.
 - `訂正`: GEC system output sentence.
 - `個別評価`: annotation scores by 3 annotators.
 - `評価`: average of `個別評価`.


## Citation

If you use our dataset, please cite our LREC paper:

 1. Yujin Takahashi, Masahiro Kaneko, Masato Mita and Mamoru Komachi. Proficiency Matters Quality Estimation in Grammatical Error Correction. 13th Edition of Language Resources and Evaluation Conference (LREC 2022). May, 2022.
