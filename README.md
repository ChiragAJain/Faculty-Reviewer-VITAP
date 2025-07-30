# University Faculty Review System

An anonymous faculty review platform that allows students to evaluate faculty members while maintaining complete anonymity through university email verification.

## Setup Instructions

### Prerequisites
- Python 3.8 or higher
- MySQL database server
- Redis server (for rate limiting)

### Installation

1. Clone the repository and navigate to the project directory

2. Create a virtual environment:
```bash
python -m venv venv
```

3. Activate the virtual environment:
```bash
# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate
```

4. Install dependencies:
```bash
pip install -r requirements.txt
```

5. Copy the environment configuration:
```bash
cp .env.example .env
```

6. Edit `.env` file with your database and email configuration

7. Initialize the database:
```bash
python run.py init-db
```

### Running the Application

```bash
python run.py
```

The application will be available at `http://localhost:5000`

## Project Structure

```
app/
├── __init__.py          # Application factory
├── models/              # Database models
├── routes/              # API routes and blueprints
├── templates/           # HTML templates
└── static/              # Static files (CSS, JS, images)
    ├── css/
    ├── js/
    └── images/
config.py                # Configuration settings
run.py                   # Application entry point
requirements.txt         # Python dependencies
```

## Development

- The application uses Flask with SQLAlchemy for database operations
- Email verification is handled through Flask-Mail
- Rate limiting is implemented using Flask-Limiter
- CORS is configured for frontend-backend communication
