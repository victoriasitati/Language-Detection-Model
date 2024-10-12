Language Detection Model
This Python project demonstrates a machine learning model that can detect and classify over 10 different languages. The model leverages a combination of natural language processing (NLP) techniques, logistic regression, and character-level N-gram feature extraction to perform language detection. Below is an overview of the key components of this project:

Key Libraries Used:
Pandas: For handling data, specifically loading and processing the dataset.
Scikit-learn: Provides utilities for data processing, model building, and evaluation.
Numpy: Supports numerical operations on arrays.
Matplotlib & Seaborn: For visualizing data.
Pickle: Used for saving the trained model for future use.
Steps in the Project:
Data Loading: The dataset is loaded using pandas, containing text data with their corresponding languages. This dataset serves as the training and testing set for the language classification task.

Data Preprocessing:

The project includes a function, rem_pun, which removes punctuation and converts all text to lowercase. This is essential for normalizing the text data and making it consistent for model training.
Feature Extraction:

A character-level N-gram model is implemented using the TfidfVectorizer from scikit-learn, which converts text into a matrix of TF-IDF features. The N-gram range is set to (1,2), meaning both unigrams and bigrams are used as features.
Model Training:

The dataset is split into training and testing sets using train_test_split.
A logistic regression model is built within a pipeline, which combines feature extraction and classification in a single step. The pipeline ensures the continuous flow from converting text to vectors and training the model.
Model Evaluation:

The model is evaluated based on accuracy and confusion matrix metrics.
The model achieves an accuracy of over 97% on the test set.
Model Saving:

The trained model is saved using the pickle library to allow for future use without retraining.
Usage:

The model can be used to predict the language of new text input, for example: model_pipe.predict(["Hola, ¿cómo estás?"]) will classify the language as Spanish.
Conclusion:
This project demonstrates the basics of language detection using machine learning, specifically logistic regression and character-level feature extraction. The trained model can be integrated into applications where language identification is crucial, such as content moderation, multilingual platforms, or text translation systems.


