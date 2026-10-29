# Books to Scrape — Python Web Scraping

A beginner-friendly Python project that collects book information from [Books to Scrape](https://books.toscrape.com/) using Requests and Beautiful Soup, then exports the results to a CSV file.

## What it does

- Requests catalogue pages from the practice website.
- Extracts each book's title, price, star-rating label, and product-page URL.
- Follows pagination to collect more than one catalogue page.
- Adds the date the scrape was run.
- Saves the results to `BooksToScrape.csv`.
- Uses pandas to inspect the collected data.

## Tools and libraries

- Python
- Requests
- Beautiful Soup 4
- pandas
- Jupyter Notebook

## Project files

- `books-to-scrape-web-scraping.ipynb` — the notebook containing the code and explanations.
- `BooksToScrape.csv` — a sample output from the original single-book version of the project. Run the cleaned notebook to generate a fresh CSV from the catalogue.
- `requirements.txt` — Python dependencies.

## How to run

1. Download or clone this repository.
2. Install Python 3.
3. Install the dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Open `books-to-scrape-web-scraping.ipynb` in Jupyter Notebook or VS Code.
5. Run the cells from top to bottom.

The notebook uses `max_pages=1` as a quick test by default. To scrape all catalogue pages, change the call to:

```python
books = scrape_books(max_pages=None)
```

The CSV is written to the same directory as the notebook.

## Data fields

| Field | Description |
|---|---|
| `Title` | Book title |
| `Price` | Price value without the £ symbol |
| `Rating` | Star-rating label from the website |
| `Product URL` | Link to the book's product page |
| `Scraped Date` | Date the data was collected |

## Notes

- This project uses the practice website Books to Scrape, intended for scraping exercises.
- Run the scraper manually when you want fresh data; it does not run continuously in the background.
- The CSV included here is retained from the original project and contains one book. Running the cleaned notebook creates a new output from the catalogue.
- Website structure can change, so selectors may need updating if the notebook stops finding book listings.

## Learning outcomes

This project demonstrates basic HTTP requests, HTML parsing with Beautiful Soup, extracting structured data, following pagination, saving data to CSV, and performing simple data inspection with pandas.
