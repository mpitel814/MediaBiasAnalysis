# MediaCoverageAnalysis 
## Project Description
This is a final project for INFO-664 - Programming for Cultural Heritage. 

It uses sentiment analysis tools to analyze how a particular topic is covered by various news outlets. 

This project explores if there is a difference in vocabulary use across the political spectrum. 

## Rationale Statement 
I was curious to know how the language use and sentiment of news articles on a particular contentious topic differed depending on whether they were published by a left- or right-leaning publication. By comparing tone and vocabulary, this project aims to reveal subtle tonal differences that may influence how audiences interpret the same issue depending on which news outlet they follow. 

## Workflow 
1. I used **requests** to return a large dataset of articles from the MediaStack API. 
3. I used **pandas** to save the dataset as a CSV, and then used **pandas** to further export it to a txt.file.
4. I used **OpenRefine** to clean and organize the articles by the political bias of their source publication. 
5. I further cleaned the .txt files using **NLTK** tools - removing stopwords, punctuation, and numbers. 
6. After tokenizing the clean text, I was able to run a series of **NLTK** sentiment analysis methods to:
- Display word frequency across all articles combined
- Display word frequency for left and right articles
- Display sentiment score across all articles combined
- Display sentiment score for left and right articles
7. Use **WordCloud** to generate a word cloud for all, left, and right articles.
  
## Further Uses 
A larger dataset that goes back at least 5 years would reveal stronger trends in vocabulary use, and it would be possible to create a timeline of media polarization of certain topics using language and sentiment analysis tools. Other sentiment analysis tools found through hugging face could be used to reveal additional language trends, such as toxicity or perceived emotion. 


## Files List
1. **README.md** - a description of this project.
2. **DataCollection.ipynb** - the python script which calls the MediaStack API to retrieve the dataset.
3. **Sentiment_Analysis.ipynb** - the python notebook in which I performed various sentiment analysis methods.
4. **immigration_articles_Raw.csv** - the master csv file with all article titles, descriptions, sources, and URLs, **uncleaned** by OpenRefine.
5. **immigration_articles_Cleaned.csv** - the csv file with all article titles, descriptions, sources, and URLs, **cleaned** by OpenRefine (punctuation & numbers removed, all lowercase).
6. **immigration-articles-Left.csv** - The csv file with a seclection of 106 left-leaning articles - manually selected using OpenRefine filtering tools (New York Times, Alternet, BBC, and ABC News). 
7. **immigration-articles-Right.csv** - The csv file with a seclection of 100 right-leaning articles - manually selected using OpenRefine filtering tools (Fox News, New York Post, Daily Mail).
8. **descriptions_raw.txt** - A .txt file containing article descriptions from immigration_articles_Raw.csv, used for **polarity scores**.
9. **descriptions_left.txt** - A .txt file containing only article descriptions from immigration-articles-Left.csv, used for **polarity scores**.
10. **descriptions_right.txt** - A .txt file containing only article descriptions from immigration-articles-Right.csv, used for **polarity scores**.
11. **descriptions_cleaned.txt** - A .txt file containing only article descriptions from immigration-articles-Cleaned.csv, used for **word frequency**.
12. **descriptions_left_fq.txt** - A .txt file containing only article descriptions from immigration-articles-Left.csv, used for **word frequency**.
13. **descriptions_right_fq.txt** - A .txt file containing only article descriptions from immigration-articles-Right.csv, used for **word frequency**.
14. **WordCloud_Images Folder** - Folder containing the the generated wordclouds, saved as PNGs. 
