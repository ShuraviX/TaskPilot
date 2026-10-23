TaskPilot — AI Task Manager Companion

Plan your tasks. Manage your time. Study smarter.

TaskPilot is an AI-powered task management and study planning application designed to help students organize their work, manage deadlines, track priorities, and create personalized schedules with the help of a locally running open-weight AI model.

Instead of manually deciding what to work on next, users can organize their tasks and use AI-generated study plans to structure their available time.

Features

Task Management: Organize tasks, descriptions, deadlines, and priorities.

Study Planning: Generate personalized schedules based on task details and available study time.

Progress Tracking: View task progress, upcoming deadlines, overdue tasks, and planned study hours.

Personalized Workspace: Maintain a personalized study space.

Light and Dark Themes: Switch between themes for a comfortable viewing experience.

AI-Powered Planning: Use Gemma 3 1B through Ollama for locally generated study plans.

Student-Friendly Interface: Use a clean dashboard to organize tasks and study activities.

Technology Stack

Technology

Purpose

HTML5

Application structure

CSS3

Styling, responsive layout, themes, and animations

JavaScript

Application logic, task interactions, and AI communication

Gemma 3 1B

Open-weight language model for AI study planning

Ollama

Runs the AI model locally

Browser Local Storage

Stores supported application data in the browser

How the AI Works

TaskPilot uses Gemma 3 1B through Ollama to generate study plans from relevant task information.

The workflow is:

The user creates tasks and provides relevant details.

The user requests an AI-generated study plan.

The application sends the relevant planning information to the locally running Ollama service.

Gemma generates a proposed schedule.

The application displays the generated plan to the user.

This approach avoids requiring a paid hosted-model API for AI inference. The model runs on the user's machine, although initial installation and model downloads require an internet connection.

Getting Started

Prerequisites

Install the following:

Python 3

Ollama

A modern web browser

1. Download the Project

Clone the repository:

git clone YOUR_GITHUB_REPOSITORY_URL
cd TaskPilot

Alternatively, download the repository as a ZIP file from GitHub and extract it.

Replace YOUR_GITHUB_REPOSITORY_URL with the actual repository URL.

2. Download the AI Model

Open a terminal and run:

ollama pull gemma3:1b

Wait until the model download finishes.

3. Start Ollama

Ensure Ollama is running and the model is available.

You can check the installed models with:

ollama list

4. Configure Local AI Access

TaskPilot communicates with Ollama's local chat API:

http://localhost:11434/api/chat

The browser origin must be allowed by Ollama's CORS configuration. For the local development server below, configure Ollama to allow requests from:

http://localhost:8000

Restart Ollama after changing its environment configuration, if necessary. Do not expose the local AI service publicly without appropriate security measures.

5. Start the Web Application

Open a terminal in the project directory and run:

python -m http.server 8000

Open the following address in your browser:

http://localhost:8000/index.html

Keep the terminal running while using the application.
## Open Innovation

TaskPilot explores how open-weight AI models can make AI-powered study tools more accessible, customizable, and useful for students.

## Project Status

Student project developed as part of an open-source AI dev challenge.
