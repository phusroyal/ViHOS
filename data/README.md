Here is our data folder structure!
```
.
└── data/
    ├── Sequence labeling-based version/
    │   ├── Syllable/
    │   │   ├── dev_BIO_syllable.csv
    │   │   ├── test_BIO_syllable.csv
    │   │   └── train_BIO_syllable.csv
    │   └── Word/
    │       ├── dev_BIO_Word.csv
    │       ├── test_BIO_Word.csv
    │       └── train_BIO_Word.csv
    ├── Span Extraction-based version/
    │   ├── dev.csv
    │   └── train.csv
    └── Test_data/
        └── test.csv
```
# Sequence labeling-based version
## Syllable
Description: 
- This folder contains the data for the sequence labeling-based version of the task. The data is divided into two files: train, and dev. Each file contains the following columns:
  - **index**: The id of the word.
  - **word**: Words in the sentence after the processing of tokenization using [VnCoreNLP](https://github.com/vncorenlp/VnCoreNLP) tokenizer followed by underscore tokenization.
  The reason for this is that some words are in bad format:
  e.g. "điện.thoại của tôi" is split into ["điện.thoại", "của", "tôi"] instead of ["điện", "thoại", "của", "tôi"] if we use space tokenization, which is not in the right format of Syllable.
  As that, we used VnCoreNLP to tokenize first and then split words into tokens.
  e.g. "điện.thoại của tôi" ---(VnCoreNLP)---> ["điện_thoại", "của", "tôi"] ---(split by "_")---> ["điện", "thoại", "của", "tôi"].
  - **tag**: The tag of the word. The tag is either B-T (beginning of a word), I-T (inside of a word), or O (outside of a word).
- The train_BIO_syllable and dev_BIO_syllable file are used for training and validation for XLMR model, respectively.
- The test_BIO_syllable file is used for reference only. It is not used for testing the model. **Please use the test.csv file in the Testdata folder for testing the model.**
## Word
Description: 
- This folder contains the data for the sequence labeling-based version of the task. The data is divided into two files: train, and dev. Each file contains the following columns:
  - **index**: The id of the word.
  - **word**: Words in the sentence after the processing of tokenization using [VnCoreNLP](https://github.com/vncorenlp/VnCoreNLP) tokenizer
  - **tag**: The tag of the word. The tag is either B-T (beginning of a word), I-T (inside of a word), or O (outside of a word).
- The train_BIO_Word and dev_BIO_Word file are used for training and validation for PhoBERT model, respectively.
- The test_BIO_Word file is used for reference only. It is not used for testing the model. **Please use the test.csv file in the Testdata folder for testing the model.**

# Span Extraction-based version
Description:
- This folder contains the data for the span extraction-based version of the task. The data is divided into two files: train and dev. Each file contains the following columns:
  - **content**: The content of the sentence.
  - **index_spans**: The index of the hate and offensive spans in the sentence. The index is in the format of [start, end] where start is the index of the first character of the hate and offensive span and end is the index of the last character of the hate and offensive span.
- The train and dev file are used for training and validation for BiLSTM-CRF model, respectively.
  