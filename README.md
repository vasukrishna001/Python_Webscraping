# Web Scraping Project

## Project Overview
This project involves **web scraping** to extract cricketer data and load them in an excel file using Python,Pandas,BeautifulSoup .

The web scraping script retrieves data about cricketers from an online source, but due to limitations with **BeautifulSoup** (which only extracts visible content before loading the entire page), not all players could be retrieved. The project aims to organize the resulting data files in a manner that makes it easier for users to access and analyze.

---

## Key Features:
1. **Web Scraping**: Extracts cricketer data from a web page. However, due to the limitation of BeautifulSoup's ability to scrape only visible content, the script may not retrieve the entire list of players.


---

## Challenges Faced:
- **Web Scraping Limitation**:
  The main challenge faced in this project was that **BeautifulSoup** could only extract content that was directly visible when the page was loaded. However, the cricketer data was revealed only after further page interactions, which BeautifulSoup wasn't able to handle. As a result, only a limited number of cricketers were scraped from the page.

## Key findings:
  **Problem**: BeautifulSoup does not handle dynamically loaded content (like data revealed after page buffering).
  **Solution**: Consider using other tools like **Selenium** or **Playwright** to handle dynamic content scraping.

---

