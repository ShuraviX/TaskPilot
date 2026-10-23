# TaskPilot — AI Task Manager Companion

TaskPilot is an AI-powered task manager and study companion designed to help students to organize their tasks, manage deadlines, and create task schedules.

## Features

- Manage tasks, study tasks, deadlines, and priorities.
- Track tasks and planned study hours.
- Generate study plans using a locally running open-weight AI model.
- Switch between light and dark themes.
- Maintain a personalized study space.

## AI Technology

TaskPilot uses Gemma 3 1B through Ollama for local AI-powered study planning.

## How to Run

1. Install Python and Ollama.
2. Download the required Gemma model using Ollama.
3. Start the local web server in the project folder:

   `python -m http.server 8000`

4. Open `http://localhost:8000/index.html` in your browser.
5. Ensure the local AI service is running and configured to allow requests from the app's origin.

## Open Innovation

TaskPilot explores how open-weight AI models can make AI-powered study tools more accessible, customizable, and useful for students.

## Project Status

Student project developed as part of an open-source AI dev challenge.
