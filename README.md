# thai-dialect-corpus
Corpus of Central Thai and three dialects (Khummuang, Korat, Pattani).

This corpus contains a total of 850 hours for Central Thai, and 50 hours for the three dialect each. The corpus is designed such that there are some parallel sentences between the dialects, making it suitable for Speech and Machine translation research. We also provide the official splits.

Our demo ASR model can be found at https://www.cmkl.ac.th/research/porjai

Since parts of this corpus is in the [ML-SUPERB challenge](https://multilingual.superbbenchmark.org), the test sets are not released in this github and would be released subsequently in ML-SUPERB.

We provide the audio and metadata in [this link](https://drive.google.com/drive/folders/14_niFB5fH29z4hZybEVF-jK5Q-wi9s5U?usp=share_link).

## Thai-central data

`Thai-central_train_dev.zip` contains the following file structure:

```
thai_central
├── dev.csv
└── train.csv
```

We provide `.csv` files containing the metadata of each dataset as follows:

- `utterance` is an utterance ID.
- `sentence` is a transcription.
- `audio` is a name of audio file.


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
├── dev.csv
└── train.csv
```
The metadata contains the 3 column as thai-central dataset and
- `official_sentence` is the Thai-translated transcription.
- `dialect_type` specifies whether the data is from the `ECOM` or `SURV` subset.
