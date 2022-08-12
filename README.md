# Enron-Email-classification

## DATA
The dataset entitled “A subset of about 1700 labelled email messages" is downloaded from https://bailando.berkeley.edu/enron_email.html . The dataset contains six categories of emails as given below:

![tables](https://user-images.githubusercontent.com/81705929/184306873-81f71fa6-fecb-4eda-95f1-733bc5ec1c82.png)

## DATA PROCESSING
1) First, Parse the emails into a list email objects. One can read more about email parser
from https://docs.python.org/3/library/email.parser.html
2) Then, create a data frame containing 'Message-ID', 'Date', 'From', 'To', 'Subject',
'Mime-Version', 'Content-Type', 'Content-Transfer-Encoding', 'X-From', 'X-To', 'X-cc',
'X-bcc', 'X-Folder', 'X-Origin', 'X-FileName', ‘Content’ as the columns.
3) Create a new data frame that contains the ‘Subject’ and ‘Content’ of the emails, Merge
these columns into one ‘data’ column. Now, we assign the labels to each email. (Since
the emails are stored in an arrangement (category1, category2, ..., category6), and we
know the number of emails belonging to each category, therefore storing the labels
accordingly).
4) Convert all words to lowercase.
5) Remove all the punctuations.
6) Remove all the stop words contained in English language.
7) Next, apply lemmatization to the data.
8) Split the data into training and testing data using train_test_split method of sklearn.

## DATA VISUALIZATION

![image](https://user-images.githubusercontent.com/81705929/184307067-013d6cfa-a6e5-4038-9e63-08c3167615b3.png)

The above plot doesn’t give any clear idea about the length of emails. So, I plotted the
following histogram.

![image](https://user-images.githubusercontent.com/81705929/184307134-5c3bc88a-ff57-437e-ac9a-787db6d210e8.png)

I have performed experiments by setting up three different values for the maximum length of
the emails, 250, 500, and 750.

## MODELLING
I have performed the experiments by using two different model architectures, CNN and
CLSTM. The C-LSTM architecture is based on the work of Zhou, Chunting, et al. "A C-LSTM
neural network for text classification." arXiv preprint arXiv:1511.08630 (2015).
I have used two different types of word embeddings, GloVe and fastText.

## EXPERIMENTAL RESULTS

![tables_l](https://user-images.githubusercontent.com/81705929/184307390-d8bb44a7-9453-4677-90f4-0e837e774560.png)

The plots for each of these experiments are given below.

![image](https://user-images.githubusercontent.com/81705929/184307452-fde7ec46-d40a-47f0-b3be-9a60aa1a0fec.png)
Fig. model 1

![image](https://user-images.githubusercontent.com/81705929/184307536-2edc6092-50a2-4b53-b3b5-3d6bc92fac69.png)
Fig. model 2

![image](https://user-images.githubusercontent.com/81705929/184307584-ee013437-4430-4a31-9a18-b4932651a5b9.png)
Fig. model 3

![image](https://user-images.githubusercontent.com/81705929/184307662-2d27e8dc-9711-4a3a-8b3b-2c9850512fc2.png)
Fig. model 4

![image](https://user-images.githubusercontent.com/81705929/184307730-3f93b806-5b53-421a-a8f5-0f9a14e666b3.png)
Fig. model 5

![image](https://user-images.githubusercontent.com/81705929/184307770-a7341685-775c-4da6-85d0-c7139cfdf030.png)
Fig. model 6

![image](https://user-images.githubusercontent.com/81705929/184307823-d896fae4-1037-49d2-be13-895fdec9b6f0.png)
Fig. model 7

![image](https://user-images.githubusercontent.com/81705929/184307873-b874d644-9ecc-4fbc-87de-b5ba63049aa9.png)
Fig. model 8
