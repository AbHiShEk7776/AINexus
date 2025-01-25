# AINexus
This Repository is made for the Codes 
Need the Code??
Here's the Code:
from azure.ai.textanalytics import what?
from azure.core.credentials import what?

# Replace with your API key and endpoint
key = "BD0XwtxqB7ki6SdlWrHt6yb0hW7KtzEbqoWtAdQqLIflKuXsPOMiJQQJ99BAACHYHv6XJ3w3AAAaACOGBW7" #No use this API key is Mine...
endpoint = "What is this ???"

# Authenticate client
client = TextAnalyticsClient(endpoint=endpoint, credential=AzureKeyCredential(key)) #The Answer to the Import lies here

# Input texts
documents = [
    "The new product is innovative and efficient.",
    "Customer service was disappointing."
]

# Perform Sentiment Analysis
response = client.analyze_sentiment(documents=documents)
for i, document in enumerate(response):
    print(f"Text: {documents[i]}")
    print(f"Sentiment: {document.sentiment}")
    print(f"Confidence Scores: {document.confidence_scores}\n")
