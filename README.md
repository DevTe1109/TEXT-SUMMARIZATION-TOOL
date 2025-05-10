# TEXT-SUMMARIZATION-TOOL
*COMPANY*: CODTECH IT SOLUTIONS
*NAME* S DEVIPRASAD
*INTERN ID*:CT04DK151
*DOMAIN* ARTIFICIAL INTELLIGENCE
*DURATION*:4 WEEKS
*MENTOR*: NEELA SANTOSH


The script is a command-line tool that summarizes lengthy articles using a pre-trained NLP model from the Hugging Face Transformers library. It offers two input methods: manually pasting text or loading a .txt file. Then it generates a concise summary using the facebook/bart-large-cnn model.

🧠 Key Components Explained
1. Imports
python
Copy
Edit
from transformers import pipeline
import os
pipeline is used to easily load pre-trained models for tasks like summarization.

os is used for file path validation.

2. load_article() Function
This function allows the user to choose how to input the article:

Option 1: Paste the article manually.

Option 2: Load the article from a .txt file.

python
Copy
Edit
def load_article():
    ...
It returns the full article as a string.

3. summarize() Function
This is the core summarization function.

python
Copy
Edit
def summarize(text, min_length=60, max_length=200):
    summarizer = pipeline("summarization", model="facebook/bart-large-cnn")
    summary = summarizer(text, ...)
    return summary[0]['summary_text']
It loads the facebook/bart-large-cnn model.

This model is fine-tuned for summarization.

It returns a short, readable summary of the input article.

4. main() Function
This function controls the flow of the script:

Displays the welcome message.

Calls load_article() to get the article text.

Calls summarize() to get the summary.

Prints the result.

python
Copy
Edit
def main():
    ...
5. Execution Entry Point
python
Copy
Edit
if __name__ == "__main__":
    main()
This ensures the script runs when executed directly.

⚙️ What the Script Does
Accepts article input (manual or file).

Uses NLP summarization.

Outputs a clean, readable summary.
