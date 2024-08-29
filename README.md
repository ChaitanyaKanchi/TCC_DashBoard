# Telugu Corpus Collection (TCC) Dashboard

## Overview

The **TCC Dashboard** is a data visualization tool built using Streamlit. It connects to an Appwrite backend to fetch, display, and analyze data related to user registrations, file uploads, and recordings. The dashboard provides a user-friendly interface for filtering, downloading, and visualizing data through interactive plots and tables.

## Features

- **User Management**: Fetch and display user registration data, including total users, registration dates, and filtering options by phone number, email, and date range.
- **File Management**: View and analyze uploaded files, with options to filter by file type (audio/video) and download selected data.
- **Recording Analysis**: Retrieve and visualize recording data, including total file sizes and distributions over time.
- **Interactive Visualizations**: Generate plots such as histograms and bar charts for better insights into user registrations and file uploads.
- **Downloadable Data**: Easily download filtered datasets in CSV format for further analysis.

## Setup and Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/tcc-dashboard.git
    cd tcc-dashboard
    ```

2. **Install Dependencies**:
    Ensure that you have Python 3.7 or later installed, then run:
    ```bash
    pip install -r requirements.txt
    ```

3. **Configure Environment Variables**:
    Create a `.streamlit/secrets.toml` file with your Appwrite credentials:
    ```toml
    [secrets]
    end_point = "your_appwrite_endpoint"
    project_id = "your_project_id"
    api_key = "your_api_key"
    database_id = "your_database_id"
    collection_id = "your_collection_id"
    bucket_id = "your_bucket_id"
    ```

4. **Run the Dashboard**:
    Start the Streamlit application:
    ```bash
    streamlit run app.py
    ```

5. **Access the Dashboard**:
    Open your browser and navigate to `http://localhost:8501` to view the dashboard.

## Dependencies

- **Streamlit**: A fast way to build and share data apps.
- **Appwrite**: Backend server for managing users, databases, and storage.
- **Pandas**: Data manipulation and analysis.
- **Plotly**: Interactive graphing library for creating visualizations.
- **Concurrent.futures**: For optimizing data fetching through concurrent processing.

## Pages Overview

The dashboard consists of the following pages:

1. **Users**:
   - Displays user registration data.
   - Allows filtering by phone number, email, and date range.
   - Provides options to download selected columns as CSV and visualize user registrations over time.

2. **Files**:
   - Shows information about uploaded files.
   - Filters files by type (audio/video) and provides options to download selected data.
   - Displays the number of file uploads and their sizes over time.

3. **Recordings**:
   - Provides an overview of recorded files.
   - Allows filtering by phone number, email, and date range.
   - Shows details and statistics about recordings, including total size and file types.

4. **Registration**:
   - Displays aggregated data on user registrations.
  
## Filters and Options

### Filters

The TCC Dashboard provides several filtering options to refine the data displayed on each page. Here's how you can use them:

#### Pages

- **Phone Number**: Enter a specific phone number to filter users by their phone number.
- **Email**: Enter an email address to filter users by their email.
- **Date Range**: Select a start and end date to filter users by their registration date. The data will be filtered to show only users registered within the selected date range.


### Options

Each page includes options that allow you to adjust how data is displayed:

#### Pages

- **Download Data**: Select the columns you want to include in the CSV file and click "Download data as CSV" to export the filtered user data.

- **Time Interval**: View user registrations aggregated by different time intervals (Daily, Weekly, Monthly). This option allows you to see trends over different periods.


### Example Usage

1. **Filter Data**: Use the sidebar filters on each page to refine the data based on your criteria (e.g., enter a phone number, select a date range).
   
2. **Select Time Intervals**: Choose a time interval to view aggregated data and trends over the selected period.

3. **Download Data**: After applying filters, you can download the filtered data by selecting the desired columns and clicking the "Download data as CSV" button.

4. **View Charts**: For pages that display charts (e.g., Users and Files pages), select different time intervals to view trends and visualize data.

These filters and options allow you to customize the data displayed on each page and perform detailed analysis based on your needs.

