# autoJQE



This repository contains binary patch data for reconstructing dataset for quality estimation of GEC.

## Requirements

 - [bsdiff/bspatch](http://www.daemonology.net/bsdiff/)

## Data
Running the script with the following command will automatically download the [W&I+LOCNESS dataset](https://www.cl.cam.ac.uk/research/nl/bea2019st/) and apply the patch.

```
$ git clone https://github.com/tmu-nlp/ProQE.git
$ cd ProQE
$ bash ./scripts/setup.sh
```

`scripts/setup.sh` generates data for each proficiency level in `data/tsv` directory.
```
$ ls ./data/tsv
a.tsv b.tsv c.tsv n.tsv
```

The first line of each generated data is a header.
```
$ head -n 1 ./data/tsv/a.tsv
source	output	scores	ave_score
```
The header contains the following columns:
 - `source`: source sentence.
 - `output`: GEC system output sentence.
 - `scores`: annotation scores by 3 annotators.
 - `ave_score`: average of `scores`.

Note: The `source` and `output` sentences are detokenized to prevent annotators from evaluating the tokenization as an error. (we used [nltk](https://github.com/nltk/nltk) for detokenization.)

## Citation

If you use our dataset, please cite our LREC paper:

 1. Yujin Takahashi, Masahiro Kaneko, Masato Mita and Mamoru Komachi. Proficiency Matters Quality Estimation in Grammatical Error Correction. 13th Edition of Language Resources and Evaluation Conference (LREC 2022). May, 2022.
