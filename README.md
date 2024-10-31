# Reflex Kinde Showcase

Welcome to the **Reflex 🤝 Kinde**! This application demonstrates how to integrate **Kinde** authentication into a **Reflex** web application. It provides a basic example of user authentication, including login, logout, and retrieving user details.

This README was written by OpenAI's o1-preview, for a more in depth walkthrough check out [Paul's video](https://www.youtube.com/watch?v=-TnZcQvPMfI)

Kinde Ref Link to get 50$ welcome bonus: https://kinde.com/r/?kinde_ref=afc49da00f2b5518

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [Key Components](#key-components)
- [License](#license)

## Prerequisites

- **Python 3.7 or higher**: Ensure Python is installed on your system. You can download it from [python.org](https://www.python.org/downloads/).
- **pip**: Python package manager (comes with Python).
- **Virtual Environment** (optional but recommended): To isolate project dependencies.

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/dentro-innovation/reflex_kinde_showcase.git
   cd reflex_kinde_showcase
   ```

2. **Create a Virtual Environment** (optional)

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

## Configuration

The application relies on environment variables for configuration. Create a `.env` file in the project root and add the following environment variables to the `.env` file:

```bash
KINDE_HOST=
KINDE_CLIENT_ID=
KINDE_CLIENT_SECRET=
KINDE_REDIRECT_URL=
KINDE_POST_LOGOUT_REDIRECT_URL=
```

- Replace placeholders with your actual Kinde credentials.
- Ensure the redirect URLs match those configured in your Kinde application settings.

## Running the Application

Start the Reflex application with:

```bash
reflex run
```

The app will be accessible at `http://localhost:3000`.

## Project Structure

- `reflex_kinde_showcase/reflex_kinde_showcase.py`: Main application file containing the Reflex components and authentication logic.
- `rxconfig.py`: Configuration file for the Reflex app.
- `requirements.txt`: Lists all Python package dependencies.
- `.gitignore`: Specifies files and directories to be ignored by Git (e.g., virtual environments, caches).
- `.env`: Contains environment variables (should not be committed to version control).

## Key Components

### Authentication State (`AuthState`)

Manages the user's authentication state and interactions with Kinde.

- **Properties**
  - `is_authenticated`: Indicates if the user is logged in.
  - `user_details`: Holds information about the authenticated user.

- **Methods**
  - `initiate_login()`: Redirects users to the Kinde login page.
  - `perform_logout()`: Logs out the user and redirects to the post-logout URL.
  - `process_authentication()`: Handles the authentication response from Kinde.
  - `update_auth_status()`: Updates the authentication state and retrieves user details.
  - `attempt_silent_auth()`: Tries to authenticate the user silently without prompting.
  - `clean_url_and_redirect()`: Cleans up URL parameters and redirects to the home page.

### User Interface

Defined in the `index` function, the UI adjusts based on authentication state:

- **Authenticated Users**
  - Display a welcome message with the user's given name.
  - Show a "Logout" button.

- **Unauthenticated Users**
  - Show a "Login" button.

### Logging

The application uses Python's `logging` module to output informative messages, aiding in debugging and monitoring.

## License

This project is licensed under the **MIT License**. Feel free to use and modify it according to your needs.

## Team

This repo is brought to you by DentroAI!

- [Dentro AI Integration and Implementation](https://dentroai.com)
- [Follow Paul on X](https://x.com/paul_dentro)
- [DentroChat](https://dentro.chat)
- [lmChatGPTtfy](https://let-me-chatgpt-that.com/)
- [Mailpal](https://mailpal.me)
- [NoteThisDown](https://note-this-down.com)
