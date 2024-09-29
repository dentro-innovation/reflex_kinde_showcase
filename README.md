# Reflex Kinde Showcase

Welcome to the **Reflex 🤝 Kinde**! This application demonstrates how to integrate **Kinde** authentication into a **Reflex** web application. It provides a basic example of user authentication, including login, logout, and retrieving user details.

This README was written by OpenAI's o1-preview, for a more in depth walkthrough check out Paul's video: 

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

The application relies on environment variables for configuration. Create a `.env` file in the project root:

