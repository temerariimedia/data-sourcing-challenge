# Data Sourcing Challenge

## Overview
This project extracts movie reviews from the **New York Times API** and movie details from **The Movie Database (TMDB) API**, merges the two datasets, and cleans the data for export into a CSV file. The final output combines movie reviews and movie metadata, including genres, spoken languages, release dates, and more.

## Project Workflow
The project involves the following key steps:

1. **Access the New York Times API**:
   - Fetch movie reviews with "love" in the headline, sectioned under "Movies" and categorized as "Reviews."
   - Use pagination to retrieve multiple pages of reviews, store results in a list, and convert the data into a Pandas DataFrame.

2. **Access The Movie Database (TMDB) API**:
   - Query movie details using movie titles retrieved from the New York Times API.
   - Extract relevant fields such as genres, languages, runtime, popularity, etc., and store results in a DataFrame.

3. **Merge and Clean the Data**:
   - Merge the reviews and movie metadata on the `title` column.
   - Clean the columns containing lists (e.g., genres, spoken languages) by removing brackets and quotation marks.
   - Drop unnecessary columns (e.g., `byline.person`) and remove duplicate rows.

4. **Export to CSV**:
   - Save the final cleaned dataset to a CSV file.

## Prerequisites

Before running this script, ensure you have the following installed:
- Python 3.x
- The required Python packages (install via `pip`):
  - `requests`
  - `pandas`
  - `python-dotenv`
  - `fuzzywuzzy` (optional, for fuzzy matching)

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/data-sourcing-challenge.git
cd data-sourcing-challenge