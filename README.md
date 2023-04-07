# Text Normalization for TTS

## Abstract
The task of normalization can be divided into several subtasks, which may differ depending on the specific language and dialect used. Some of the common text normalization subtasks for TTS include:
Word expansion: In TTS, it is important to expand abbreviations and abbreviations to ensure they are pronounced correctly. For example, the abbreviation "in-t" should be expanded to "institute", and the abbreviation "JSC" should be expanded to "joint stock company". There is also a more complicated case when “40 km2” should be verbalized not as “forty kilometers two” and not even as “forty kilometers squared” but as “forty square kilometers”.


Number normalization: TTS systems must take into account correct form agreement for cardinal, ordinal, and Roman numerals, and process numbers in such a way that they sound natural when spoken aloud. For example, the number "123" can be expanded to "one hundred twenty-three" or "one-two-three" depending on the context or the style of speech desired. Thus, "We start at the expense of 123" should be transformed into "We start at the expense of one two three" and the text "I live on 123 Engels Avenue" into "I live on Engels Avenue one hundred and twenty-three."

## Dataset 
For work, a dataset was chosen from the kaggle competition Text Normalization Challenge - Russian language. It contains 761424 offers and 10574516 tokens.

## Model
For testing, a sequence-to-sequence transformation model was chosen to normalize text in Russian. The transformer was originally proposed in article Attention Is All You Need. The TensorFlow 2 library was chosen for work - it is an open platform for machine learning and deep learning created by Google.

## Metrics and results
In order to more clearly understand how well our model coped with the task, the BLEU metric was also calculated for the untransformed dataset in order to use this estimate as a baseline. As a result, for the untransformed dataset we got BLEU = 0.25, for the dataset transformed by our model we got BLEU = 0.54.