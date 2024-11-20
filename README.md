# IoT Log Parser
This project implements a robust IoT log parser that extracts, structures, and visualizes data from IoT sensors and devices. The parser handles Base64-encoded images, web server logs, and various data types while incorporating error handling and informative visualizations.

# Installation Instructions/Setup
1. Clone the Repository
Clone this repository to your local machine:
git clone https://github.com/your_username/your_repo.git

2. Install Dependencies
Install the required Python libraries:
pip install pandas matplotlib pillow

3. Add Log File
Place the log file in the root directory of the project or specify its path in the parser script.

# How to Run
1. Run the Parser Script
Execute the parser.py file from the terminal:
python parser.py

2. Output
Parsed Data:
Saved as parsed_data.csv in the working directory.
Decoded Images:
Base64-encoded images are saved as .png files in the working directory.
Visualizations:
Graphs and charts are displayed and saved as .png files.

# Assumptions
Log Entry Format:
Log entries are newline-separated, with key-value pairs in the format:
makefile
Temperature=28.92 Humidity=65.4 Timestamp=2024-11-20T12:00:00Z Base64Image=...

Data Types:
The parser assumes correct key-value pair syntax.
Missing values (null) are handled gracefully.

Base64 Decoding:
Base64-encoded strings represent valid images.

Web Server Logs:
Metrics like request counts and response codes are extracted if logs are in Apache/Nginx format.

# Features

Data Extraction:
Extracts key-value pairs, assigns correct data types, and handles missing values.

Data Structuring:
Stores extracted data in a Pandas DataFrame for analysis.

Base64 Image Decoding:
Decodes Base64-encoded images and saves them as .png files.

Visualization:
Generates visualizations, such as temperature trends and request counts.

Error Handling:
Skips invalid entries while logging errors for debugging.

# Performance Analysis
Average processing time for 1,000 log entries: X seconds.
Visualization rendering time: Y seconds.
