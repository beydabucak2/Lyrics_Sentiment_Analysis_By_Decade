# Firstly, please check the presentation: Presentation Link: https://publuu.com/flip-book/767516/1702331 🎶

## Project Description 📂
**projectI.ipynb**  
This project involves the analysis of song lyrics from different eras. With a dataset categorized by eras and artists, the aim is to interpret which emotions were predominant in each era.

## Project Limitations 🛠️

- **Insufficient Data Variety**: Due to the limitations of the free API and the character limit of the Hugging Face model, the project was done with limited data. Since I couldn't directly pull the eras, I recorded each artist separately and later associated them with specific eras. As a result, the project duration was extended and a lot of time was spent on data preparation.

- **Insufficient Emotion Categories**: Only three categories (positive, negative, neutral) were used in the project. Due to "label" limitations in the Hugging Face model, I couldn’t access additional categories. In my Project II course, I plan to add themes like war, love, separation, and dance and expand the project without using Hugging Face.

## Project Content 📂

- **Finding the Dataset**: Using the Genius API and the lyricsgenius library, I gathered song lyrics from artists who had popular songs in different eras. The artists were categorized by era, and separate datasets were created. This enabled analysis based on both the artists and the eras.

- **Data Cleaning and Preparation**: Unnecessary words were cleaned from the lyrics. Explanations were removed using the NLTK module. JSON files were converted into DataFrames, then into pickle files to make them suitable for analysis.

- **Analysis**: A model from the Hugging Face library was integrated to perform sentiment analysis. The model classified the song lyrics into "positive", "negative", and "neutral" labels.

- **Data Visualization**: It was determined and visualized which words were used more frequently in each era. Additionally, an analysis was done on which words were used in relation to specific word groups in different eras.

## Libraries:

- **transformers**: The Hugging Face Transformers library was used for sentiment analysis of song lyrics.
- **torch**: The PyTorch library is necessary for running the model.
- **pandas**: Used for data analysis and processing.
- **matplotlib**: Used for graphing and visualization.
- **scikit-learn**: Performs text vectorization for word frequency analysis.
- **nltk**: Used for natural language processing, such as word cleaning and stopword handling.
- **collections**: The `Counter` class was used for counting words.
- **re**: Regular expressions (regex) were used for text cleaning and extracting specific words.
- **pickle**: Used for loading and saving data files (pkl format).
- **os**: Used for file path operations.
- **CountVectorizer (scikit-learn)**: Used for vectorizing words and performing word frequency analysis.
- **stopwords (nltk)**: Used to create a stopwords (unnecessary words) list.

## Analysis and Results 📈

**Sentiment Analysis**  
The Twitter-roBERTa model was used for sentiment analysis. The model classified song lyrics as positive, negative, or neutral.
