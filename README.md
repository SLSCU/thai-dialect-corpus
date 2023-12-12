# thai-dialect-corpus
Corpus of Central Thai dialect and three other Thai dialects (Khummuang, Korat, and Pattani).

This corpus contains a officially split of 700 hours for Central Thai, and 40 hours for the three dialect each. The corpus is designed such that there are some parallel sentences between the dialects, making it suitable for Speech and Machine translation research.

Our demo ASR model can be found at https://www.cmkl.ac.th/research/porjai. The data collection of the Thai Central was collected using [Wang Data Market](https://www.wang.in.th/).

Since parts of this corpus are in the [ML-SUPERB challenge](https://multilingual.superbbenchmark.org), the test sets are not released in this github and would be released subsequently in ML-SUPERB.

We provide the audio and metadata in [this link](https://drive.google.com/drive/folders/14_niFB5fH29z4hZybEVF-jK5Q-wi9s5U?usp=share_link).

In the Google drive, you will see 2 directories, `thai-central` and `thai-dialect`

## Thai-central data

A `thai-central` directory contains the following file structure:

```
thai_central
├── audio
│   ├── train_audioxx.zip
│   ├── ...
│   ├── dev_audioxx.zip
│   └── ..
├── dev.csv
└── train.csv
```

We provide `.csv` files containing the metadata of each dataset as follows:

- `utterance` is an utterance ID which is also the name of audio file.
- `sentence` is a transcription.
- `audio` is a name of audio file and the directory where it belongs.


## Thai-dialect data

`thai-dialect_train_dev.zip` contains the following directory structure:

```
thai_dialect
├── khummuang
├── korat
└── pattani
```

In each dialect is separated into

```
<thai-dialect>
├── audio
│   ├── train_audioxx.zip
│   ├── ...
│   ├── dev_audioxx.zip
│   └── ..
├── dev.csv
└── train.csv
```
The metadata contains the 3 columns as thai-central dataset and
- `thai_sentence` is the Thai-translated transcription.
- `dialect_type` specifies whether the data is from the `ECOM` or `SURV` subset.

The baseline models of our corpus are at
- Thai-central: https://huggingface.co/SLSCU/thai-dialect_thai-central_model
- Khummuang: https://huggingface.co/SLSCU/thai-dialect_khummuang_model
- Korat: https://huggingface.co/SLSCU/thai-dialect_korat_model
- Pattani: https://huggingface.co/SLSCU/thai-dialect_pattani_model


The Thai-dialect Corpus is licensed under CC-BY-SA 4.0. (https://creativecommons.org/licenses/by-sa/4.0/)

## Acknowledgement

We would like to thank the PMU-C grant (Thai Language Automatic Speech Recognition Interface for Community E-Commerce, C10F630122)
for the support of this research. 
We also would like to acknowledge the Apex compute cluster team which provides compute support for this project.

Some evaluation data was donated from Wang.

The data

## Paper

[Thai Dialect Corpus and Transfer-based Curriculum Learning Investigation for Dialect Automatic Speech Recognition](https://www.isca-speech.org/archive/pdfs/interspeech_2023/suwanbandit23_interspeech.pdf)
```
@inproceedings{suwanbandit23_interspeech,
  author={Artit Suwanbandit and Burin Naowarat and Orathai Sangpetch and Ekapol Chuangsuwanich},
  title={{Thai Dialect Corpus and Transfer-based Curriculum Learning Investigation for Dialect Automatic Speech Recognition}},
  year=2023,
  booktitle={Proc. INTERSPEECH 2023},
  pages={4069--4073},
  doi={10.21437/Interspeech.2023-1828}
}
```
