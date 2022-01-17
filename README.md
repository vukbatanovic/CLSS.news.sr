# CLSS.news.sr - The Serbian Cross-Level Semantic Similarity News Corpus
The Serbian CLSS News Corpus consists of 1000 phrase-sentence and 1000 sentence-paragraph pairs in Serbian gathered from news sources on the web.
Each sentence pair was manually annotated with fine-grained semantic similarity scores on the 0-4 scale.
The final scores were obtained by averaging the individual scores of five annotators.

## Corpus creation
The source texts for the CLSS.news.sr corpus were gathered from www.naslovi.net, a news aggregator website in Serbian.
The pairs were constructed by exploiting the journalistic convention that the beginning sections of a news article usually give a summary of the article's content.
Hence, extracting the beginning sections from the articles that deal with the same subject matter, but are gathered from different news outlets, is a good way of obtaining semantically related text pairs.

*Naslovi.net* provides a headline and an introductory paragraph for each news report, sometimes with a subhead as well.
The headlines were treated as source material for phrases, subheads as source material for sentences, and introductory paragraphs as source material for paragraphs.
A paragraph was defined as text containing a minimum of two sentences, where only complete sentences are taken into account.
A sentence had to contain at least one finite verb form, whereas a phrase was not allowed to contain finite verbs.

Using the 18000 collected news reports (June - August 2021), the annotators manually compiled a set of pairs for both text lengths.
In doing so, they were instructed to aim for a balanced score distribution for the pairs they construct.

## Corpus annotation
Each text pair was annotated in parallel by five annotators working independently, using a 0-4 Likert score scale.
The [STSAnno](https://vukbatanovic.github.io/STSAnno/) tool was used in the annotation process.

In addition to score definitions, the annotators were provided with three examples for each similarity score and text pair length.
The annotation guidelines (with examples) are available in original [Serbian](http://github.com/vukbatanovic/CLSS.news.sr/blob/main/Annotation%20guidelines%20-%20Serbian.pdf) and in [English](http://github.com/vukbatanovic/CLSS.news.sr/blob/main/Annotation%20guidelines%20-%20English.pdf) translation.

The final semantic similarity scores for each sentence pair were obtained by averaging the scores of individual annotators.

## Corpus format
The Serbian CLSS News Corpus is available as a single tab-separated .txt file containing both the phrase-sentence and the sentence-paragraph pairs - *[CLSS.news.sr.txt](http://github.com/vukbatanovic/CLSS.news.sr/blob/main/CLSS.news.sr.txt)*.
Each set of text lengths is also available as a separate tab-separated .txt file:
* Phrase-Sentence CLSS pairs - [CLSS.news.sr.phrase-sentence.txt](http://github.com/vukbatanovic/CLSS.news.sr/blob/main/CLSS.news.sr.phrase-sentence.txt)
* Sentence-Paragraph CLSS pairs - [CLSS.news.sr.sentence-paragraph.txt](http://github.com/vukbatanovic/CLSS.news.sr/blob/main/CLSS.news.sr.sentence-paragraph.txt)

All files contain 8 tab-separated columns:
* Column 1 - the final semantic similarity score, obtained as the average of individual annotator scores
* Columns 2-6 - the individual scores of all five annotators
* Column 7 - the shorter text in a pair
* Column 8 - the longer text in a pair

Texts are written in the Serbian Latin script.
The file is encoded in UTF-8.

## Corpus statistics
The average annotator self-agreement score, expressed in terms of the Pearson correlation coefficient *r*, is 0.93 for the phrase-sentence pairs, and 0.923 for the sentence-paragraph pairs.
The average annotator self-agreement score, expressed in terms of the Krippendorff's alpha coefficient, is 0.926 for the phrase-sentence pairs, and 0.92 for the sentence-paragraph pairs.

The average (binary) inter-rater agreement score, expressed in terms of the Pearson correlation coefficient *r*, between an annotator and the averaged scores of all other annotators is 0.938 for the phrase-sentence pairs. and 0.937 for the sentence-paragraph pairs.
The average binary inter-rater agreement score, expressed in terms of the Krippendorff's alpha coefficient, between an annotator and the averaged scores of all other annotators is 0.934 for the phrase-sentence pairs. and 0.932 for the sentence-paragraph pairs.
The global inter-rater agreement score between all annotators, expressed in terms of the Krippendorff's alpha coefficient, is 0.899 for the phrase-sentence pairs. and 0.895 for the sentence-paragraph pairs.

The phrase-sentence subset of *CLSS.news.sr* contains around 30 thousand tokens, with an average phrase length of around 6 tokens and an average sentence length of around 23 tokens.
The sentence-paragraph subset of *CLSS.news.sr* contains around 86 thousand tokens, with an average sentence length of around 22 tokens and an average paragraph length of around 64 tokens.

The average semantic similarity score value is 1.96 for the phrase-sentence pairs and 1.91 for the sentence-paragraph pairs.
The distribution of text pairs across the range of similarity scores, including intermediate values, is fairly balanced.

## References
TBA

## Acknowledgement
CLSS.news.sr was created as part of the project *[Advancing Novel Textual Similarity-based Solutions in Software Development – AVANTES](http://avantes.etf.bg.ac.rs/index-eng.html)*, supported by the [Science Fund of the Republic of Serbia](http://fondzanauku.gov.rs/?lang=en), grant no. 6526093, AI-AVANTES, within the “Program for Development of Projects in the field of Artificial Intelligence”.

## License
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

If you wish to use this dataset in a commercial product, please contact me at: vuk.batanovic / at / ic.etf.bg.ac.rs
