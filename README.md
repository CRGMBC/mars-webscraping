# mars-webscraping
Challenge 11

# Part 1: Scrape Titles and Preview Text from Mars News

Automated browsing with Splinter was used to visit the Mars news site, and the HTML code was extracted with Beautiful Soup
The titles and preview text of the news articles were scraped and extracted.  
Titles and preview information was extracted using find. function on classes of 'content_title' and 'article_teaser_body'.
This data was joined in a new dictionary called article_dict and appended into articles_list.

# Part 2: Scrape and Analyse Mars Weather Data

Automated browsing with Splinter was used to visit the Mars temperature data site, and the HTML code was extracted with Beautiful Soup
The HTML table was found using the find function and all rows of data were extracted (including the header row)
The scraped data was assembled into a Pandas Dataframe using the same column headers as the website.
This was managed by creating a weather_data list and looping through the rows to find all the cells with data ('td').  These cells were appended to the weather_data list.
A Pandas Dataframe was created with the Column headings from the website and then adding the weather_data list.

Some data types were updated to enable future analysis:

The terrestrial date was converted to a date format, columns sol, ls and month were converted to integers, and min_temp and pressure were converted to float types.

Data was then analysed as below;

The number of 'Martian' day's worth of data was calculated using the pandas function of unique terrestrial dates in the data frame.

The average temperature by month was calculated by using the group.by function on the month field and returning the mean (average) of min_temp field for each month.  This was then displayed in a bar graph.
A second bar graph was created of the same data but sorted by the average temperature for the easy visual identification of the lowest & highest months by average temperature.

The average atmospheric pressure by Martian month on Mars was calculated by using the group.by function on the month field and returning the mean (average) of the pressure field for each month.  This was plotted in a bar graph, sorted by the average pressure value for the easy identification of the lowest & highest month atmospheric pressure average.

This final dataframe was exported to a csv file, called mars_table.csv.