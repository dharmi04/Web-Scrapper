# Web-Scrapper

# Web Spider for URL Scrapping

This Python script is a simple web spider that scrapes URLs from a given website and checks if a specific keyword is present in those URLs. The script uses the `requests` library to send HTTP GET requests to web pages and the `BeautifulSoup` library to parse the HTML content.

## How to Use

1. **Prerequisites**:

   - Python installed on your system.
   - Install the required libraries (`requests`, `BeautifulSoup`) if you haven't already by running:
     ```bash
     pip install requests beautifulsoup4
     ```

2. **Running the Script**:

   - Run the script in your terminal or command prompt.
   - You will be prompted to enter the URL of the website you want to scrape and a keyword to search for in the URLs found on that website.

3. **Script Execution**:

   - The script will start by sending an HTTP GET request to the provided URL.
   - It will then parse the HTML content of the webpage using BeautifulSoup.
   - The script will find all the `<a>` (anchor) tags in the HTML, which typically contain links.
   - It extracts the `href` attribute from each `<a>` tag to get the URL.
   - If the URL contains the specified keyword, it will be printed to the console.
   - The script will also follow these URLs recursively, meaning it will visit the linked pages and repeat the process, checking for the keyword in those pages as well.
   - The set `visited_urls` is used to keep track of visited URLs to prevent revisiting the same URL.

4. **Exit**:

   - You can stop the script by closing the terminal or pressing `Ctrl+C`.

## Example Usage

Here's an example of how you might use this script:

1. Run the script and provide the following inputs:
   - Enter URL you want to scrape: `http://example.com`
   - Enter keyword to search for in URL provider: `example`

2. The script will start crawling `http://example.com` and its linked pages, printing URLs containing the keyword "example" to the console.

## Note

- Be cautious when scraping websites. Ensure you have permission and are complying with the website's terms of service.
- This is a basic web spider, and it may not handle complex websites with JavaScript-based content loading.
- The script does not implement depth-limiting or any complex crawling rules, so it can potentially crawl a large number of pages.

---

Feel free to adapt and enhance the `spider_urls` function to fit your specific needs or add more features to the script as required.
