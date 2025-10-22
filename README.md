# DisasterTweetPredictions
Predicting whether or not a tweet refers to a disaster using a dataset of 10,000 labeled tweets from https://www.kaggle.com/competitions/nlp-getting-started/data

# notebooks
`DisasterTweetPrediction.ipynb` contains the data cleaning, model training, and analysis.

# models
Variants of Logistic Regression, Multinomial Naive Bayes, and XGBoost were trained and evaluated. The best models resulting from grid search runs and their associated metrics are stored in a dictionary called `model_comparisons` and have been pickled. 

## sample usage 

1. Loading
- If running from Google Colab:

```
import pickle
# modify the path to where you saved the pickle file
file_path = '/content/drive/MyDrive/YOUR_FOLDER/model_comparisons.pkl'


with open(file_path, 'rb') as f:
    model_comparisons = pickle.load(f)
```

2. Predict

```
# get a specific model based on a label
model = model_comparisons['Logistic Regression f1']['model']

# call predict
y_pred = model.predict(X_test)

```

🎬 [Download or watch video (33 MB)](https://raw.githubusercontent.com/JericCantos/DisasterTweetPredictions/main/reports/video_walkthrough.mp4)

