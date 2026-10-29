# Books to Scrape — Python Web Scraping

A beginner Python project that extracts the **title and price of one book** from the practice website [Books to Scrape](https://books.toscrape.com/), then saves the result to a CSV file with the date it was collected.

## What this project does

1. Sends a request to one book page using `requests`.
2. Parses the page with `BeautifulSoup`.
3. Extracts the book title and price.
4. Saves the values and collection date to `BooksToScrape.csv`.
5. Optionally reads the CSV with `pandas` to check the output.

This project intentionally keeps the original single-book scope. It does **not** scrape the entire catalogue or run on a schedule.

## Tools used

- Python
- Requests
- BeautifulSoup
- CSV
- pandas (optional, for viewing the output)

## How to run it

1. Install Python 3.
2. Download or clone this repository.
3. Open `books-to-scrape-web-scraping.ipynb` in Jupyter Notebook or VS Code.
4. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

5. Run the notebook cells from top to bottom.

The notebook saves `BooksToScrape.csv` in the current working directory. Running it again overwrites the CSV with the latest title, price, and date.

## Files

- `books-to-scrape-web-scraping.ipynb` — notebook with the scraping steps.
- `BooksToScrape.csv` — example output from the project.
- `requirements.txt` — Python libraries used by the notebook.

## Learning goals

- Sending an HTTP request to a webpage
- Parsing HTML with BeautifulSoup
- Selecting elements with CSS selectors
- Cleaning extracted text
- Saving results to a CSV file

## Note

Books to Scrape is a practice website intended for web-scraping exercises. This project demonstrates a small, single-page example; it is not a full catalogue scraper.
