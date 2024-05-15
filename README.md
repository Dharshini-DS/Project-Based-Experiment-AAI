<H3>NAME: Dharshini DS</H3>
<H3>REGISTER NO: 212221230022</H3>

<H1 Align="center">Project Based Experiment<H1>
  
<H3>Objective:</H3> 
  
Perform sentiment analysis using your Facebook data and filter the data that has only negative feedback for the code given in the following link.

<H3>Program:</H3>

```
pip install pandas textblob
import pandas as pd
from textblob import TextBlob

# Load the CSV file into a DataFrame
df = pd.read_csv('fb_sentiment.csv')

# Function to perform sentiment analysis using TextBlob
def analyze_sentiment(text):
    blob = TextBlob(str(text))
    return blob.sentiment.polarity

# Apply sentiment analysis to each row in the DataFrame
df['Sentiment'] = df['FBPost'].apply(analyze_sentiment)

# Output the DataFrame with sentiment analysis results
print(df.head())

# Filter out rows with negative sentiment (label 'N')
negative_feedback = df[df['Label'] == 'N']

# Output the negative feedback
print(negative_feedback)
```

<H3>Output:</H3>

![0](https://github.com/Dharshini-DS/Project-Based-Experiment-AAI/assets/93427345/3e22b78a-6166-4703-ade0-b05f3fc8dd8e)

![01](https://github.com/Dharshini-DS/Project-Based-Experiment-AAI/assets/93427345/43a625b0-a8f5-4a69-be6d-fc56494ed1f7)

<H3>Inference:</H3>

Thus sentiment analysis using your Facebook data ias done and filtering the data that has only negative feedback for the code is done.
