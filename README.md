# HateSpeech
1.Dataset

The data are stored as a CSV. Each data file contains 5 columns:

count = number of CrowdFlower users who coded each tweet (min is 3, sometimes more users coded a tweet when judgments were determined to be unreliable by CF).

hate_speech = number of CF users who judged the tweet to be hate speech.

offensive_language = number of CF users who judged the tweet to be offensive.

neither = number of CF users who judged the tweet to be neither offensive nor non-offensive.

class = class label for majority of CF users. 0 - hate speech 1 - offensive language 2 - neither

In this project, I merged the "hate speech" label and "offensive language" label into one lable, then conducted a binary classification work.

2.Text data preprocessing.

Remove Noise(punctuation, HTML,……)

Lowercasing

      Make the same words in different cases can be treated as the same.
      
Remove stop words

      Drop some extremely common words which would appear to be of little value in data analyzing.(Remove the words that are very commonly used in a given language, we can focus on the important words instead.) 
      
Tokenization

     Split an input sequence into tokens. A token can be a word, sentence, paragraph , etc. In this project, I just split sentences into words
     
Token normalization(Lemmatization    Stemming)

      Reduce inflectional forms and sometimes derivationally related forms of a word to a common base form. Eg: (am,are,is->>be)(car,cars,car’s,cars’->>car)
      In this project I use Lemmatization to normalize the token.

3.Text Vectorization.

Bag of words (BOW), TF-IDF. In this project, I compared these two techniques with different classifiers.

4.Build different classification models.

Three traditional models I used in this project.

Logistic Regression 

SVM 

