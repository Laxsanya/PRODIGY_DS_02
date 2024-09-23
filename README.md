# PRODIGY_DS_04
import pandas as pd
from textblob import TextBlob
import matplotlib.pyplot as plt
col_names = ['ID', 'Entity', 'Sentiment', 'Content']
df = pd.read_excel('/content/2 boook.xlsx',names=col_names)
df.head()
sentiment_counts = df['Sentiment'].value_counts()
sentiment_counts
plt.figure(figsize=(6, 3))
sentiment_counts.plot(kind='bar', color=['red', 'green', 'yellow', 'blue'])
plt.title('Sentiment Distribution')
plt.xlabel('Sentiment')
plt.ylabel('Number of Tweets')
plt.xticks(rotation=0)
plt.show()
     
