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
4. I used **OpenRefine** to organize the articles by the political bias of their source publication. 
5. I cleaned the .txt files using **NLTK** tools - removing stopwords, punctuation, and numbers. 
6. After tokenizing the clean text, I was able to run a series of **NLTK** sentiment analysis methods to:
- Display word frequency across all articles combined
- Display word frequency for left and right articles
- Display sentiment score across all articles combined
- Display sentiment score for left and right articles
- Generate a word cloud for all, left, and right articles.
  
## Further Uses 
A larger dataset that goes back at least 5 years would reveal stronger trends in vocabulary use, and it would be possible to create a timeline of media polarization of certain topics using language and sentiment analysis tools. Other sentiment analysis tools found through hugging face could be used to reveal additional language trends, such as toxicity. 


## Files List
1. README.md - a description of this project.
2. immigration_articles_BIG_2.csv - the master csv file with all article titles, descriptions, and sources on a particular topic, uncleaned by OpenRefine.
3. immigration-articles-BIG-CLEANED.csv - the master csv file with all article titles, descriptions, and sources on a particular topic, cleaned by OpenRefine (punctuation & numbers removed, all lowercase). 
4. immigration-articles-BIG-Left.csv - The csv file with a seclection of 100 left leaning articles - manually selected using OpenRefine filtering tools (New York Times, Alternet, BBC, and ABC News)
5. articles_right.csv - the csv file with all of the right leaning articles
6. The rest to follow...
