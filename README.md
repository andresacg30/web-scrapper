# web-scrapper
This is a Web Scrapper for retrieving nature.com's articles using Python and Beautiful Soup.

### Libraries used:
- requests
- string
- BeautifulSoup
- os

# How does it works?
The program will ask for the number of pages and the type of article that we want to be scrapped.
It will create a folder for each page with the name "Page_N" where N is the number of page. In each folder the program will save the article as a .txt file, with the name of the article. The program will also replace any whitespace in the filename with an underscore, to prevent further errors. 
The program will print messages when the connection to every page is successfull, when each file is created and when all articles are saved. If there's a wrong website, or the page doesn't content an article, the program will display that error.

# My approach
I defined 4 functions:
- retrieve_url: used for retrieving url and checking connection errors
- get_articles: used for find the <article> tag in the retrieved url, get the article type and create a list of links to all the articles of the type specified by the user
- create_directories: used for create N folders in the working directory, where N correspond to the number of pages that the user wants to be scrapped. The folders will be created as "Page_n", where n is the page number.
- save_scrapper_files: used for iterate over each link in the list returned by get_articles function. In each link, this function will get the title of the article, replace punctuation to underscores, and save the article as .txt file in the corresponding folder.
