
# sentiment-analysis
this repo has sentiment analysis of review given for online fashion items(mainly clothing) using BERT

An online fashion retailer wants to develop a machine learning model that can classify customer reviews into different sentiment categories. The model will take as input a customer review and output a prediction of the review's sentiment, such as positive, negative, or neutral.

# dataset description 

This dataset includes 23486 rows and 10 feature variables. Each row corresponds to a customer review, and includes the variables:

Clothing ID: Integer Categorical variable that refers to the specific piece being reviewed.
Age: Positive Integer variable of the reviewers age.
Title: String variable for the title of the review.
Review Text: String variable for the review body.
Rating: Positive Ordinal Integer variable for the product score granted by the customer from 1 Worst, to 5 Best.
Recommended IND: Binary variable stating where the customer recommends the product where 1 is recommended, 0 is not recommended.
Positive Feedback Count: Positive Integer documenting the number of other customers who found this review positive.
Division Name: Categorical name of the product high level division.
Department Name: Categorical name of the product department name.
Class Name: Categorical name of the product class name.


# data preprocessing 

I have taken only 2 feature variables Review Text and Rating according to our requirement then I have removed the null values Because of the lack computational resources I have taken the 1st 8000 rows, If we have enough computational resources we can take the whole dataset (refer https://github.com/Srieswari/sentiment-analysis/blob/main/datapreprocessing.ipynb)

I have mapped the rating 1,2 for negative feedback , 3 for neutral , 4,5 for positive because the rating is from worst to best as given in the data description, after mapping the data is unbalanced so I have made the data a balanced one or else it might lead to biased model. (refer https://github.com/Srieswari/sentiment-analysis/blob/main/Sentimental_Analysis.ipynb)

# model 

BERT model selected           : https://tfhub.dev/tensorflow/small_bert/bert_en_uncased_L-4_H-512_A-8/1
Preprocess model auto-selected: https://tfhub.dev/tensorflow/bert_en_uncased_preprocess/3



ACCURACY


![image](https://github.com/Srieswari/sentiment-analysis/assets/99708903/706df4ce-7706-4db3-b26b-f825d539bf16)
