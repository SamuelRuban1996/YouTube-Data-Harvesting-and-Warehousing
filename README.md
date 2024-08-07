# YouTube Data Harvesting and Warehousing

## Overview

This project is a Streamlit application that allows users to harvest data from YouTube channels, store it in a SQL database, and perform various analyses on the collected data. It uses the YouTube Data API to fetch channel, video, comment, and playlist information, and provides a user-friendly interface for data retrieval, storage, and analysis.

## Features

- Fetch detailed information about YouTube channels, including videos, comments, and playlists
- Store harvested data in a SQL database (MySQL)
- Migrate data from temporary storage to SQL database
- Execute predefined queries to analyze the collected data
- User-friendly interface built with Streamlit

## Requirements

The project requires Python 3.7+ and the following libraries:

- google-api-python-client==2.86.0
- pandas==1.5.3
- SQLAlchemy==2.0.15
- mysql-connector-python==8.0.33
- streamlit==1.22.0
- python-dotenv==1.0.0

These dependencies are listed in the `requirements.txt` file.

## Setup

1. Clone the repository:
git clone https://github.com/your-username/youtube-data-harvesting.git
cd youtube-data-harvesting

2. Install the required packages:
pip install -r requirements.txt

3. Set up your YouTube Data API key:
- Go to the [Google Developers Console](https://console.developers.google.com/)
- Create a new project or select an existing one
- Enable the YouTube Data API v3
- Create credentials (API key)
- Replace the `api_key` variable in the script with your API key

4. Set up your MySQL database:
- Install MySQL if not already installed
- Create a new database named `youtube_data`
- Update the database connection string in the `create_engine_and_session()` function

5. Configure the application:
- Replace Enter your image path in the code with the path to your background image.
- Replace Enter your API key here with your actual YouTube Data API key.
- Update the database connection string in the create_engine_and_session() function if necessary.

## Usage

1. Run the Streamlit app:
streamlit run app.py

2. Open the provided URL in your web browser

3. Enter a YouTube channel ID in the input field and click "Get Results and Store Data"

4. Once data is retrieved, select a channel from the dropdown to migrate data to SQL

5. After migration, use the query selector to analyze the data

## Workflow

1. **Data Retrieval**: 
- Enter a YouTube channel ID
- App fetches channel details, videos, comments, and playlists using YouTube Data API
- Retrieved data is temporarily stored in the application's memory

2. **Data Storage**: 
- Select a channel from the dropdown menu
- Click "Migrate Data to SQL" to store the data in the MySQL database

3. **Data Analysis**: 
- Choose from predefined queries in the dropdown menu
- App executes the selected query on the SQL database
- Results are displayed in a tabular format

## Project Structure

- `app.py`: Main Streamlit application file
- `requirements.txt`: List of required Python packages
- `README.md`: Project documentation (this file)

## Dependencies

The `requirements.txt` file contains the following dependencies:
google-api-python-client==2.86.0
pandas==1.5.3
SQLAlchemy==2.0.15
mysql-connector-python==8.0.33
streamlit==1.22.0
python-dotenv==1.0.0

To install these dependencies, run:
pip install -r requirements.txt

## Contributing

Contributions to improve the project are welcome. Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature-branch`)
3. Make your changes and commit them (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin feature-branch`)
5. Create a new Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
