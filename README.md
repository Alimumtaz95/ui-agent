# Logistics AI Assistant

Welcome to the Logistics AI Assistant! This project is designed to provide a helpful chatbot assistant using advanced AI models. Below, you'll find a detailed explanation of the project, its setup, and how to use it.

## Table of Contents
1. [Overview](#overview)
2. [Features](#features)
3. [Setup Instructions](#setup-instructions)
4. [How It Works](#how-it-works)
5. [Usage](#usage)
6. [Troubleshooting](#troubleshooting)

---

## Overview
The Logistics AI Assistant is a chatbot application built using Python. It leverages the `chainlit` library and Google's Gemini API to provide intelligent and context-aware responses. The assistant is designed to help users with logistics-related queries or any other tasks it is configured for.

## Features
- **Interactive Chatbot**: Engages users in a conversational manner.
- **Powered by Gemini API**: Utilizes Google's Gemini API for advanced AI capabilities.
- **Session Management**: Maintains chat history for context-aware responses.
- **Customizable**: Easily adaptable to different use cases by modifying the agent's instructions.

## Setup Instructions
Follow these steps to set up and run the project:

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd ui-agent
   ```

2. **Install Dependencies**:
   Ensure you have Python installed. Then, install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Environment Variables**:
   Create a `.env` file in the project root and add your Gemini API key:
   ```env
   GEMINI_API_KEY=your_api_key_here
   ```

4. **Run the Application**:
   Start the chatbot application:
   ```bash
   python hello.py
   ```

## How It Works

1. **Environment Setup**:
   - The application loads environment variables from a `.env` file using the `dotenv` library.
   - It retrieves the `GEMINI_API_KEY` to authenticate with the Gemini API.

2. **Chat Initialization**:
   - When a user starts a chat, the `start` function initializes the session.
   - It sets up the AI model (`gemini-2.0-flash`) and creates an agent with predefined instructions.

3. **Message Handling**:
   - Incoming messages are processed by the `main` function.
   - The assistant generates responses based on the chat history and updates the session.

4. **Error Handling**:
   - If an error occurs (e.g., missing API key), the application provides a clear error message.

## Usage
- Start the application by running `python hello.py`.
- Open the chat interface (if applicable) and interact with the assistant.
- Ask logistics-related questions or any queries the assistant is configured to handle.

## Troubleshooting
- **Missing API Key**:
  Ensure the `GEMINI_API_KEY` is set in the `.env` file.
- **Dependencies Not Installed**:
  Run `pip install -r requirements.txt` to install missing packages.
- **Application Errors**:
  Check the console logs for detailed error messages.

---

Feel free to customize the assistant's behavior by modifying the `hello.py` file. Happy coding!