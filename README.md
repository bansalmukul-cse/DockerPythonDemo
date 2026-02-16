# PythonApp

A Python application demonstrating API interactions, MySQL database operations, and Docker containerization.

## Features

- **API Demo**: Fetches random cat facts from a public API
- **SQL Demo**: Interactive MySQL database application for managing usernames
- **Docker Support**: Containerized setup with MySQL database

## Project Structure

- `api_demo.py` - Demonstrates API calls to fetch cat facts
- `sql_demo.py` - MySQL database interaction script (main application)
- `myapp.py` - Simple file reading utility
- `servers.txt` - Data file for storing usernames
- `Dockerfile` - Docker configuration for the Python application
- `docker-compose.yml` - Multi-container setup with MySQL

## Prerequisites

- Python 3.x
- Docker and Docker Compose (for containerized deployment)
- MySQL (if running locally without Docker)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/bansalmukul-cse/PythonApp.git
   cd PythonApp
   ```

2. Install Python dependencies (if running locally):
   ```bash
   pip install requests pymysql cryptography
   ```

## Usage

### Running Locally

1. **API Demo**:
   ```bash
   python api_demo.py
   ```

2. **SQL Demo** (requires MySQL setup):
   ```bash
   python sql_demo.py
   ```

3. **File Reader**:
   ```bash
   python myapp.py
   ```

### Running with Docker

1. Build and start the containers:
   ```bash
   docker-compose up --build
   ```

2. The application will start automatically and connect to the MySQL database.

3. Use the interactive menu in the SQL demo to:
   - Add usernames to the database
   - View all stored usernames
   - Quit the application

## Docker Services

- **mysqldb**: MySQL database container
  - Database: `userinfo`
  - Root password: `root`
  - Health check enabled

- **mypythonapp**: Python application container
  - Builds from local Dockerfile
  - Depends on MySQL service health
  - Interactive terminal enabled

## Database Schema

The application creates a `usernames` table with:
- `id` (INT, AUTO_INCREMENT, PRIMARY KEY)
- `name` (VARCHAR(255))

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source. Please check the license file for details.