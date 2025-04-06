# Assignment

## Instructions

Use the following code as a starting point to load the rotten tomatoes dataset:

```python
from datasets import load_dataset

# Load the Rotten Tomatoes dataset
dataset = load_dataset("rotten_tomatoes")

# Print the dataset information
print(dataset)

# Example: Accessing the training split
train_dataset = dataset["train"]

# Print the first example in the training set
print(train_dataset[0])
```

**Model Application:**

- Load a pre-trained sentiment analysis model from Hugging Face Transformers.
- Apply the model to a subset of the chosen dataset (e.g., the first 1000 samples from the training set).
- Evaluate the model's performance. You can start with qualitative analysis (inspecting predictions) and then explore quantitative metrics.

```python
from transformers import pipeline
from datasets import load_dataset
import pandas as pd

# Load the Rotten Tomatoes dataset
dataset = load_dataset("rotten_tomatoes")
train_dataset = dataset["train"]

# Load a pre-trained sentiment analysis model
sentiment_analysis = pipeline("sentiment-analysis")

# Select a subset of the dataset (e.g., 1000 samples)
subset_size = 1000
subset_dataset = train_dataset.select(range(subset_size))

# Make predictions on the subset
predictions = sentiment_analysis([example["text"] for example in subset_dataset])

# Add predictions to the dataset
df = pd.DataFrame(subset_dataset)
df['sentiment'] = [prediction['label'] for prediction in predictions]
df['sentiment_score'] = [prediction['score'] for prediction in predictions]

print(df.head())

# Example of qualitative analysis: Inspecting predictions
for i in range(5):
    print(f"Review: {subset_dataset[i]['text']}")
    print(f"Predicted Sentiment: {predictions[i]['label']} (Score: {predictions[i]['score']:.4f})\n")

# Further steps: Quantitative analysis (e.g., accuracy, F1-score) would require ground truth labels
# and a defined evaluation metric.  This is more complex because the Rotten Tomatoes dataset
# provides 'label' as 0 or 1, while the sentiment analysis pipeline provides 'POSITIVE' or 'NEGATIVE'.
# A mapping would be required to compare the two.
```

## Submission

- Submit the URL of the GitHub Repository that contains your work to NTU black board.
- Should you reference the work of your classmate(s) or online resources, give them credit by adding either the name of your classmate or URL.
