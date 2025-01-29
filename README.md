Overview

This project fetches and processes trending search topics from Google Trends using its RSS feed. The data is structured, enriched with additional details, and optionally categorized using external APIs before being stored in a Google Sheet.

Features

Fetches Google Trends RSS feed for the UK.

Extracts trend details such as titles, summaries, links, and approximate traffic.

Retrieves associated news headlines for each trend.

Converts UTC timestamps to UK time (Europe/London timezone).

Stores the processed data into a Pandas DataFrame.

Appends new data to a Google Sheet while avoiding duplicate entries.

Requirements

To run this script, you need the following Python packages installed:

pip install feedparser pandas requests openai gspread oauth2client pytz

Usage

1. Fetch Google Trends Data

The fetch_google_trends_rss() function:

Retrieves Google Trends RSS feed for the UK.

Parses the feed to extract relevant information.

Converts the extracted data into a Pandas DataFrame.

2. Categorizing Trends (Optional)

There is a placeholder function categorize_with_knowledge_graph(keyword), which can be used to categorize trends using external APIs.

3. Save and Append to Google Sheets

The processed data is saved to a Google Sheet:

Loads existing data from the sheet.

Appends new data while avoiding duplicates.

Updates the sheet with the latest data.

Setup for Google Sheets Integration

To integrate with Google Sheets:

Create a Google Cloud Project and enable the Google Sheets API.

Generate a service account key and download the JSON credentials.

Share your Google Sheet with the service account email.

Use gspread and oauth2client for authentication.

Running the Script

Open the script in Google Colab and execute the following:

!pip install feedparser gspread pandas requests oauth2client pytz

Then run the script to fetch and update Google Trends data.

Troubleshooting

If the feed does not return data, verify that the Google Trends RSS URL is accessible.

Ensure the service account has the correct permissions for Google Sheets.

Check for missing dependencies and install them using pip.

License

This project is licensed under the MIT License.
