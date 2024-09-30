# Flask Notes App

A web application built using Flask that allows multiple users to take notes. The application supports user authentication features like sign up, log in, and log out.

## Features

- **User Authentication**: 
  - **Sign Up**: Users can create an account.
  - **Login**: Users can log into their account.
  - **Logout**: Users can log out from their session.

- **Notes Management**:
  - **Create Notes**: Users can write and save notes.
  - **View Notes**: Users can view their own notes after logging in.
  - **Edit/Delete Notes**: Users can edit or delete their existing notes.

## Tech Stack

- **Backend**: [Flask](https://flask.palletsprojects.com/)
- **Database**: SQLite (can be swapped for any relational database)
- **Frontend**: HTML5, CSS3, Bootstrap
- **Authentication**: Flask-Login
- **Forms Handling**: Flask-WTF (for managing form submissions and validation)

## Setup Instructions

### Prerequisites

Ensure that you have the following installed:

- [Python 3.x](https://www.python.org/downloads/)
- [Flask](https://flask.palletsprojects.com/)
- [Flask-Login](https://flask-login.readthedocs.io/)
- [Flask-WTF](https://flask-wtf.readthedocs.io/)
- [SQLite](https://www.sqlite.org/index.html) (optional: used by default but can be replaced)

### Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/flask-notes-app.git
    cd flask-notes-app
    ```

2. Create a virtual environment (optional but recommended):

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # For Windows, use `venv\Scripts\activate`
    ```

3. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Initialize the database (optional, this step could be skipped due to running the application would create a new DB if the instance DB is deleted) :

    ```bash
    flask db init
    flask db migrate -m "Initial migration."
    flask db upgrade
    ```

5. Run the Flask application:

    ```bash
    Navigate to main.py and run Python file
    ```

6. Open your browser and go to `http://127.0.0.1:5000/` to access the app (seen in the command prompt).

## Project Structure

```plaintext
FlaskIntro/
│
├── website/
│   ├── __init__.py       # Initializes Flask app
│   ├── models.py         # Database models (User, Notes)
│   ├── routes.py         # Application routes (login, logout, signup, notes CRUD)
│   ├── templates/        # HTML templates
│   └── static/           # CSS, JS, and images
│
├
├── requirements.txt      # Project dependencies
└── README.md             # You're here!
