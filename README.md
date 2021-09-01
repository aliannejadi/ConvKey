# ConvKey

## Data
This repository contains the following files/folders:
- <i>ConvKey_processed_min2max4.csv</i> - the main file which was used to train Keyword Extractor. It combines both datasets: <i>News-Keywords based dataset</i> and <i>IR-Keyword-based dataset</i>. Dataset has been filtered under assumption that a sentence would have at minimum 2 at maximum 4 keywords
- folder <i>/news_raw</i> - contains raw data (sentences with keywords) collected from news sources such as: BBC, Salon, The Local
- folder <i>/IR_kwds_raw</i> - contains raw data (sentences with keywords) collected using the IR Keywords based method. Folder has 2 files: one includes sentences from which <i>minimum 1 - maximum 3</i> keywords were identified, the other one includes sentences from which <i>min 2 - max 4</i> keywords were identified.

## Structure of the data
Data files contain the following attributes:
- <i>text</i> - tokeized version of the original text
- <i>target</i> - here is presented the original sentence with keywords being surrounded by the <KEYWORD> tag from both sides
- <i>keywords_sorted</i> - a list of keywords sorted by their respective order in the sentence
- <i>keywords_indices</i> - indicies of the keywords in a sentence
- <i>keywords_count</i> - count of keywords in a sentence
