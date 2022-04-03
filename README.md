# umich-694-695
SIADS Milestone 2 Project
In many real-world applications, there is a need to make sure textual information is comprehensible/readable by audiences who may not have high reading proficiency. This might include students, children, adults with learning/reading difficulties, and those who have English as a second language. The simple Wikipedia (https://en.wikipedia.org/wiki/Simple_English_Wikipedia), for example, was created exactly for this purpose. Before the editors spend a lot of effort to simplify the text and increase its readability, it would be very useful to suggest to them which parts of an article's text might need to be simplified.

We set up a text classification task to accomplish this goal. Every document (a line in the data file) is a sentence from an Wikipedia article.

Your goal is to classify each document (sentence) into ONE of two categories, based on whether it needs to be simplified.

0: the sentence does NOT need to be simplified.

1: the sentence DOES need to be simplified.

The training data contains 416,768 sentences, already labeled with one of the above categories. The test data contains 119,092 comments that are unlabeled. The submission should be a .csv (comma separated free text) file with a header line "ID,Category" followed by exactly 119,092 lines. In each line, there should be exactly two integers, separated by a comma. The first integer is the line ID of a test sentence **(0-119,091)**, and the second integer is the category your classifier predicts one of (0,1).

You can make 10 submissions per day. Once you submit your results, you will get an accuracy score computed based on 50% of the test data. This score will position you somewhere on the leaderboard. Once the competition ends, you will see the final accuracy computed based on 100% of the test data. The evaluation metric is the accuracy of your classifier - so the higher the better.

Please be sure to review the Rules page before you start. You can use any classifiers, any combination of features, and either supervised or semi-supervised methods. You can choose to use feature selection, or not. You can also be creative and make use of external data sources that do not contain the exact text comments in the data. We've provided a few helper resources below.

Helper Resources
You aren't required to use the following resources, but you may find them useful as a source of features. They are included with the other data files.

additional_resource_file_readme.txt :: Describes the columns of the files below. 
dale_chall.txt   :: This is the Dale-Chall list of ~3000 elementary English words that are typically familiar to 80% of American 4th grade students (in the 90s)
Concreteness_ratings_Brysbaert_et_al_BRM.txt ::  Concreteness ratings for about 40k English words.
AoA_51715_words.csv :: List of approximate age (In years) when a word was learned, for 50k English words.
**NEW**HLT 2004 Readability: Unigram Language Models This folder contains files with frequency counts computed on the entire dataset for the twelve categories of labeled documents used in the HLT 2004 paper, corresponding to material at each of the U.S. elementary school grades 1 through 12 (indexed as 0 to 11). There is also a background English model file. With these raw unigram counts, plus some smoothing as described in the paper, the grade-level language models used for the classifier can be derived. More info can be found here:
K. Collins-Thompson and J. Callan. A language modeling approach to predicting reading difficulty. Proceedings of HLT / NAACL 2004, Boston, USA, May 2004. 193-200. (pdf here)
Acknowledgements
We thank Cristina Garbacea for providing this Wikipedia dataset.
