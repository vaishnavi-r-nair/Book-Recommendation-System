# Book Recommendation System

## Overview
This project is a Book Recommendation System that includes:
- A **book scraping notebook** for collecting book data.
- A **Streamlit web application** for showcasing the recommendations and user interaction.

The system aims to provide users with personalized book recommendations based on their preferences or a selected genre.

## Project Structure
```
book-recommendation-system/
|-- dataset                  # The dataset file
|-- book_webscrap.ipynb      # A notebook of how book scraping is done
|-- mood.ipynb               # A notebok that adds moods column using `facebook/bart-large-mnli` LLM Model
|-- web                      # File for streamlit web scripts
|-- requirements.txt         # Required Python libraries
|-- README.md                # Project documentation (this file)
```

## Features
- **Data Scraping**: `book_webscrap.ipynb` extracts book details such as titles, authors, genres, reviews, and description from (https://www.wonderbk.com/)
- **User-Friendly Interface**: `web` provides a simple, interactive web interface for users to view book recommendations based on their input.

## Prerequisites
Ensure you have Python installed along with the following packages:
- `streamlit`
- `requests`
- `beautifulsoup4`
- `pandas`
- `scikit-learn`
- `transformer`

Install the dependencies using:
```bash
pip install -r requirements.txt
```

## Usage
1. **Run the book scrap notebook**:
   - This will create the dataset file for the book set that have been scraped.
   
2. **Launch the Streamlit application**:

   - Before starting the streamlit application you need to start the server:
   
     ```bash
     python ./web/api/chroma_server.py
     ```

   - Run the web app to interact with the system:
     ```bash
     streamlit run ./web/intialpage.py
     ```


3. **Navigate to the URL** provided by Streamlit (usually `http://localhost:8501`) to explore the recommendations.

## Customization
- Modify `book_webscrap.ipynb` on the genres to change the number of books and different genres needed to be scraped.

## Future Enhancements
- Integration with a larger dataset for diverse recommendations.
- Advanced machine learning models for better personalization.
- User authentication and profile management. (This will be done after online delopyment)
