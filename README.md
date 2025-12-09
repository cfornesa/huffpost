# Classifying News Content From The Huffington Post

**Authors:** Aarad Ashraf, Marilyn Cleveland, and Christopher Fornesa.
**Institution:** Boston University.
**Date of Completion:** December 7, 2025.

Classifying news articles, and other media, into different media categories can be rendered difficult due to the constraints of limited categories (as news articles are posted in a single category). 

For this project, we used the <a href="https://huggingface.co/datasets/khalidalt/HuffPost">HuffPost dataset</a>, which was a collection of news articles collected between 2012 and 2018 from the Huffington Post, a noted news media publication.

The goal for this project was to develop a classifier to most accurately predict news articles into different media categories. 

Originally, there were 41 categories, which we later condensed into 30 categories. Additional issues that we handled included consolidating text into a single text column, cleaning this column of null or empty string values, and ensuring that categories made sense.

By developing a neural network classifier using the RoBERTa pretrained model, we were able to develop a model that predicts with 77% accuracy and a 0.67 macro F1 score (67% overall accuracy when accounting for accuracy per-class).

Upon looking at the results, we noticed that categories for women, impact, and other more femme-oriented categories, as well as other social minority-oriented categories for Black and Latino voices, yielded worse results than more general topics, such as food and drink and politics.

Part of this discrepancy had to do with differences in observations, as there were far more articles about politics and food and drink than there were for the aforementioned categories (as evidenced by their per-class F1 scores). 

However, we also noticed that some niche categories, such as style and beauty, which were also more femme-oriented, yielded high per-class F1 scores. It is apparent that we could have further condensed broader news categories.

Upon reflection, numerous improvements can be made in the future, such as further hyperparameter optimizations and condensing articles into less categories, to obtain higher figures for accuracy and per-class and macro F1 scores.
