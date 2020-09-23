# Music Lyrics Wordcloud: Project Overview
- Created a word cloud visualization based on a musical artist's lyrics
- Scraped data from the Genius Lyrics website using BeautifulSoup
- Processed and cleaned the data using RegEx

## Code and Resources Used
**Python Version:** 3.7\
**Packages:** pandas, numpy, matplotlib, regex, beautifulsoup, requests, wordcloud\
**Genius Scarping Help:** https://www.johnwmillr.com/scraping-genius-lyrics/\
**Project Inspiration:** https://towardsdatascience.com/3-super-simple-projects-to-learn-natural-language-processing-using-python-8ef74c757cd9

## Data Sources
Genius Lyrics - https://genius.com/

## Web Scraping
Tweaked the web scraper code from  John Miller (link above) to scrape select song lyrics from genius.com. Each request yielded a string of preprocessed lyrics.

# Data Cleaning/Processing
After scraping the data, I needed to clean it in order to generate a word cloud from it. Here are the steps I took:
1. Split the string to create a list of words
2. Iterate through each word and remove punctuation, special characters, and numbers
3. Remove words that tagged sections of the song (e.g. chorus)
4. Removed any empty strings from the list of words

# WordCloud
I defined a custom list of stop words to try and isolate unique words that artists may use. I then utilized the WordCloud library and fed it my processed lyrics list to generate a word cloud. Below are the results for 5 songs belonging to the artist NF.

![alt text](https://github.com/nkrajew/lyrics_wordcloud/blob/master/images/NF_wordcloud.png "NF Word Cloud")

# Potential Next Steps
1. Utilize the Genius API to make requests to artists then scrape their songs
    - Better yet, utilize the library by John W. Miller (https://www.johnwmillr.com/scraping-genius-lyrics/)
2. Try to extract themes from an artists songs
3. Split an artist's songs into to 2 (past and present) to see how their words/themes have changed
