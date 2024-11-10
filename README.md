from textblob import TextBlob

def analyze_sentiment(text):
    """
    Analyzes the sentiment of the provided text.
    
    Parameters:
    text (str): Text input to analyze.
    
    Returns:
    str: Sentiment category (positive, negative, neutral).
    """
    blob = TextBlob(text)
    sentiment_score = blob.sentiment.polarity

    if sentiment_score > 0:
        return "Positive"
    elif sentiment_score < 0:
        return "Negative"
    else:
        return "Neutral"

# Example usage
text = "I absolutely love using TextBlob for sentiment analysis!"
result = analyze_sentiment(text)
print(f"The sentiment of the text is: {result}")
