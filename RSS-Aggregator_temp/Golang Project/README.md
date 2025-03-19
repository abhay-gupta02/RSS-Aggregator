# RSS Aggregator

## Overview
The RSS Aggregator is a web-based application that fetches and displays RSS feeds from multiple sources. It is designed to streamline the process of collecting and viewing news, blogs, and other content feeds in one centralized platform. The backend is developed using Go, with PostgreSQL as the database, and Flask for handling API endpoints.

## Features
- **RSS Feed Parsing**: Fetches and processes RSS feeds from multiple sources.
- **REST API**: Provides endpoints to retrieve and manage feed data.
- **Database Storage**: Uses PostgreSQL to store feed information for efficient retrieval.
- **Scalability**: Designed to handle multiple feeds with optimized performance.

## Tech Stack
- **Backend**: Go (main processing), Flask (API layer)
- **Database**: PostgreSQL
- **Developer Tools**: Postman (API testing), Git, Visual Studio Code

## Installation
### Prerequisites
Ensure you have the following installed:
- Go (>=1.18)
- Python (>=3.8)
- PostgreSQL
- pip
- Virtual Environment (recommended)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/abhay-gupta/rss-aggregator.git
   cd rss-aggregator
   ```
2. Set up PostgreSQL database:
   ```sql
   CREATE DATABASE rss_aggregator;
   ```
3. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```
4. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
5. Run the backend services:
   ```bash
   go run main.go  # Start the Go backend
   python app.py  # Start the Flask API
   ```

## API Endpoints
### 1. Fetch Feeds
- **Endpoint**: `GET /feeds`
- **Description**: Returns a list of stored RSS feeds.
- **Response Format**:
  ```json
  [
    {
      "title": "Tech News",
      "link": "https://example.com/rss",
      "description": "Latest tech updates"
    }
  ]
  ```

### 2. Add Feed Source
- **Endpoint**: `POST /add_feed`
- **Description**: Adds a new RSS feed source.
- **Request Format**:
  ```json
  {
    "url": "https://example.com/rss"
  }
  ```

## Future Enhancements
- Implement user authentication for personalized feed management.
- Optimize feed fetching with background jobs.
- Deploy the application to a cloud platform.

## Contribution
Contributions are welcome! Fork the repo, create a new branch, and submit a pull request.

## Contact
For queries or contributions, reach out to:
- **Email**: ag770527@gmail.com
- **LinkedIn**: [Abhay Gupta](https://www.linkedin.com/in/abhay-gupta-30017021b/)

