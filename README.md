<H3>ENTER YOUR NAME:BALA MURUGAN</H3>
<H3>ENTER YOUR REGISTER NO:212222230017.</H3>
<H3>DATE:13.05.2024</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
Perform sentiment analysis using your Facebook data and filter the data that has only Positive feedback for the code given in the following link.
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

# Filter out rows with positive sentiment (label 'P')
positive_feedback = df[df['Label'] == 'P']

# Output the negative feedback
print(positive_feedback)
```
<H3>Output:</H3>

![329946701-54ebfee7-e1df-4fbe-aebd-82d75898206b](https://github.com/Bala1511/Project-Based-Experiment-AAI/assets/118680410/1cb8403a-70d9-47fb-bb66-40914cb078b3)

<H3>Inference:</H3>
Write about your learning experience out of this project. (What you have learned)
