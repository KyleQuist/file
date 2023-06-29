import requests
from bs4 import BeautifulSoup

# URL of the website you want to scrape
url = 'https://example.com'

# Send a GET request to the URL
response = requests.get(url)

# Create a BeautifulSoup object to parse the HTML content
soup = BeautifulSoup(response.text, 'html.parser')

# Find and extract specific elements from the HTML
# Here's an example of extracting all the links from the website
links = soup.find_all('a')

# Print the extracted links
for link in links:
    print(link.get('href'))
# file
git add scraping.py
git commit -m "Add web scraping code"
git push origin master
