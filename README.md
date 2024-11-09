
# Scraping 

Welcome to the **Scraping Class**! This project introduces web scraping fundamentals with a hands-on approach to extracting data from web pages using Python. The code covers important scraping methods, including HTML parsing, element selection, data extraction, and use of external libraries for enhanced functionality.


## Requirements

To run this project, you need the following Python packages:

- `requests` – For making HTTP requests to access webpage content.
- `beautifulsoup4` – For parsing and navigating HTML documents.
- `pandas` – For managing and organizing extracted data.
- `scrapethat` – (Optional) A library to simplify web scraping workflows.

Install the dependencies with:
```bash
pip install requests beautifulsoup4 pandas scrapethat
```

## Features

### 1. Parsing an HTML Document

The script begins by making an HTTP request to a sample webpage, parsing the HTML content with BeautifulSoup. This section sets up basic scraping functionality, where we analyze elements on the page using two main methods:

- `select` and `select_one`: Allow selection based on CSS selectors.
- `find` and `find_all`: Allow selection based on tag names.

This section explores the differences between `select` (CSS-based selection) and `find` (HTML tag-based selection), helping students understand when to use each approach.

### 2. Extracting University Names

Using `select` and list comprehensions, the script gathers and prints a list of university names from the sample page:
```python
uni_list = soup.select('.name')
university_names_list = [one_uni.text for one_uni in uni_list]
```
This segment demonstrates efficient data extraction through comprehension lists, showcasing how to quickly gather textual data from selected elements.

### 3. Iterating with Loops

The script includes several loop examples, such as iterating over a list of HTML elements and printing their content:
```python
for one_uni in uni_list:
    print(one_uni.text)
```
Here, students learn to work with loops for processing multiple items, an essential skill in data extraction tasks.

### 4. Scraping Data from GeekWire

After the initial webpage parsing, the script demonstrates an advanced example by scraping the **GeekWire** website:
```python
t = read_cloud('https://www.geekwire.com/startups/page/2')
titles = [x.text for x in t.select('.entry-title')]
```
In this section:
- We retrieve titles of articles from the page, providing a real-world example of how to scrape news headlines.
- The `scrapethat` library is used to simplify the scraping process by encapsulating certain common scraping functions.

### 5. Advanced Data Manipulation with `map`

The final section demonstrates the `map` function for applying transformations across multiple data items, enabling efficient data manipulation and showcasing another method for processing web content.

# Scraping Class Documentation

This repository contains files and scripts for the **VAPS Scraping Class**, where each week we dive deeper into web scraping techniques using Python. Each week's lesson builds on the previous one, providing both foundational and advanced scraping methods.


## Setup Instructions

1. Install the required packages:
   ```bash
   pip install requests beautifulsoup4 pandas scrapethat


## Weekly Topics

- **Week 1**: Introduction to HTML Parsing and Selection Methods
  - Explored the basics of parsing HTML documents.
  - Learned the differences between `find` and `select` methods in BeautifulSoup.
  - Scraped data from the GeekWire website as an example, focusing on article titles.

  [Link to Week 1 Script](session_1_on_class.ipynb)
