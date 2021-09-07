# ConvKey

## Data
This repository contains the following files/folders:
- `ConvKey_processed_min2max4.csv` - the main file which was used to train Keyword Extractor. It combines both datasets: <i>News-Keywords based dataset</i> and <i>IR-Keyword-based dataset</i>. Dataset has been filtered under assumption that a sentence would have at minimum 2 at maximum 4 keywords
- folder `./news_raw` - contains raw data (sentences with keywords) collected from news sources such as: BBC, Salon, The Local (`./news_raw/news_bbc.csv`, `./news_raw/news_salon.csv`, `./news_raw/news_thelocal.csv`)
- folder `./IR_kwds_raw` - contains raw data (sentences with keywords) collected using the IR Keywords based method. Folder has 2 files: one includes sentences from which <i>minimum 1 - maximum 3</i> keywords were identified, the other one includes sentences from which <i>min 2 - max 4</i> keywords were identified. (`./IR_kwds_raw/qulac_min1_max3kwds.csv`, `./IR_kwds_raw/qulac_min2_max4kwds.csv`)

## Structure of the data
All data files follow the same structure and contain the following attributes:
- `text` - tokeized version of the original text
- `keywords_indices` - indicies of the keywords in a sentence
- `keywords_count` - count of keywords in a sentence

For example, for the original sentence: “Conservatives and liberals drink different beer”
| Attribute  | Data example | Comment |
| ------------- | ------------- | --- |
| text  | [’conservatives’, ’and’, ’liberals’, ’drink’, ’different’, ’beer’] | Tokenized sentence |
| keywords_indices  | [0, 2, 5]  | Meaning that the keywords are: [’conservatives’, ’liberals’, ’beer’] |
| keywords_count  | 3 | Count of the keywords |

Below you can find a sample of the data taken from `ConvKey_processed_min2max4.csv` dataset:

| text  | keywords_indices | keywords_count |
| ------------- | ------------- | --- |
|['find', 'background', 'information', 'about', 'man', 'made', 'satellites']|[2, 5]| 2 |
|['bring', 'back', 'the', 'dark', 'how', 'our', 'overuse', 'of', 'artificial', 'light', 'is', 'changing', 'nighttime', 'for', 'the', 'worse']|[6, 8, 9]|3|
