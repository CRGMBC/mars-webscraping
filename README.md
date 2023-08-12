# mars-webscraping
Challenge 11

Part 1: Scrape Titles and Preview Text from Mars News
Automated browsing with Splinter was used to visit the Mars news site, and the HTML code was extracted with Beautiful Soup
The titles and preview text of the news articles were scraped and extracted.  
Titles and preview information was extracted using find. function on classes of 'content_title' and 'article_teaser_body'.
This data was joined in a new dictionary called article_dict and appended into articles_list.

Part 2: Scrape and Analyse Mars Weather Data
Automated browsing with Splinter was used to visit the Mars temperature data site, and the HTML code was extracted with Beautiful Soup
The HTML table was found using the find function and all rows of data were extracted (including the header row)
The scraped data was assembled into a Pandas Dataframe using the same column headers as the website.
This was managed by creating a weather_data list and looping through the rows to find all the cells with data ('td').  These cells were appended to the weather_data list.
A Pandas Dataframe was created with the Column headings from the website and then adding the weather_data list.