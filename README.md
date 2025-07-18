Sentiment Analysis Dashboard
This project is a web-based sentiment analysis dashboard built using Streamlit and Hugging Face Transformers. It allows users to input text manually or upload a file (TXT or CSV) to perform sentiment analysis and visualize the results.

Features
Manual Text Input: Enter one or more lines of text directly into a text area for analysis.

File Upload: Upload .txt files (one text per line) or .csv files. For CSV files, you can select the column containing the text to be analyzed.

Sentiment Analysis: Utilizes a pre-trained sentiment analysis model from Hugging Face Transformers to classify text as positive, negative, or neutral.

Results Table: Displays the analyzed text along with its predicted sentiment and confidence score in a clear table format.

Interactive Visualizations:

Bar Chart: Shows the distribution of sentiments (positive, negative, neutral).

Pie Chart: Provides a percentage breakdown of sentiment categories.

Download Results: Export the sentiment analysis results as a CSV or JSON file.

Technologies Used
Streamlit for creating the interactive web application.

Hugging Face Transformers for the sentiment analysis model.

Pandas for data manipulation.

Matplotlib for plotting visualizations.

Setup and Installation
To run this application locally, follow these steps:

Clone the repository (if applicable, otherwise ensure you have app.py and requirements.txt in the same directory):

Bash

git clone <repository_url>
cd <repository_name>
Create a virtual environment (recommended):

Bash

python -m venv venv
Activate the virtual environment:

On Windows:

Bash

.\venv\Scripts\activate
On macOS/Linux:

Bash

source venv/bin/activate
Install the required dependencies:

Bash

pip install -r requirements.txt
The 

requirements.txt file specifies the exact versions of the libraries used:


How to Run
After installing the dependencies, run the Streamlit application from your terminal:

Bash

streamlit run app.py
This command will open the application in your default web browser.

Usage
Enter Text: Type or paste your text into the "Manual input" text area. Each line will be treated as a separate input for sentiment analysis.

Upload File:

Click "Browse files" to upload a .txt file (each line will be analyzed) or a .csv file.

If you upload a .csv file, a dropdown will appear, allowing you to select the column containing the text you want to analyze.

Analyze: Click the "🚀 Analyze" button to start the sentiment analysis.

View Results: The results will be displayed in a table showing the original text, predicted sentiment (Positive, Negative, or Neutral), and confidence score.

View Visualizations: Below the results table, you'll find a bar chart and a pie chart illustrating the overall sentiment distribution.

Download Results: Use the "Download CSV" or "Download JSON" buttons to save the analysis results.

Code Structure
app.py: The main Streamlit application script.

load_model(): Caches the Hugging Face sentiment analysis pipeline for efficient loading.

Input Section: Handles manual text input and file uploads (TXT and CSV).

Analysis Logic: Processes the input text(s) through the loaded model and formats the results into a Pandas DataFrame.

Display Results: Renders the DataFrame as an interactive table.

Visualizations: Generates and displays bar and pie charts using Matplotlib.

Download Buttons: Provides options to download results.

Styling: Uses st.markdown with unsafe_allow_html=True for custom styling of titles and footers.

requirements.txt: Lists all the Python dependencies required to run the application.
