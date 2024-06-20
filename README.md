# Web-Scraping-Project-Report
**Task: Extract Information from Websites (use any 100 websites)**

Web Scraping Solution

This project scrapes information from a list of websites and stores the data in a PostgreSQL database.

Prerequisites

1.Python 3.x

2.PostgreSQL server

3.Required Python libraries:

4.requests

5.BeautifulSoup (bs4)

6.psycopg2-connector-python

Installation

1.Clone the Repository:

git clone <repository_url>

cd <repository_directory>

2.Install the Python Libraries:

pip install requests bs4 psycopg2-connector-python

3.Set Up the PostgreSQL Database:

CREATE DATABASE project;

USE project;

CREATE TABLE companies_info;

 create_script = """ CREATE TABLE IF NOT EXISTS companies_info (
 
                          id  SERIAL PRIMARY KEY,
                          
                          company_name VARCHAR(255),
                          
                          contact_email   VARCHAR(255),
                          
                          contact_address  TEXT,
                          
                          contact_number  VARCHAR(50),
                          
                          company_website_url   VARCHAR(255),
                          
                          cms_mvc  TEXT);"""

Usage

1.In the source code, update the database connection parameters with your PostgreSQL username and password:

database = "project",

username = "postgres",

pwd = "your_password",

hostname = "localhost",

port_id = 5432

2.Run the Script:

python <script_name>.py

The script will:

a.Scrape data from the list of URLs.

b.Store the extracted data in the PostgreSQL database.

c.Display the stored data after scraping is complete.

Additional Notes

a.The script includes a 5-second delay between requests to avoid overwhelming the target servers and to comply with polite scraping practices.

b.Error handling is implemented to skip over any websites that fail to be scraped, ensuring that the script continues to run even if some URLs are problematic.
