# LLM Chatbot

This project is a simple chatbot application that uses OpenAI's GPT-3.5-turbo model to generate responses to user input. The chatbot runs on a Node.js server and interacts with a front-end interface where users can input their messages.


### Features

* Interactive Chat Interface: Users can interact with the chatbot via a simple web interface.
* Real-time Responses: The chatbot generates responses in real-time using OpenAI's API.
* Node.js Server: The backend is powered by a Node.js server that handles API requests and serves the front-end files.


### Project Structure

* public/: Contains static files for the front-end, including index.html, styles.css, and main.js.
* node_modules/: Contains Node.js dependencies (after running npm install).
* config.js: Stores the API key for OpenAI (not included in the repository for security reasons).
* openai.js: Contains the logic for interacting with the OpenAI API.
* server.js: The main server file that handles routes and API requests.
* package.json: Contains metadata about the project and its dependencies.


## Getting Started
### Prerequisites

* Node.js: Make sure you have Node.js installed on your machine.
* OpenAI API Key: You need an API key from OpenAI to use their models.

### Installation

1. Clone the repository:
```
git clone https://github.com/yourusername/llm-chatbot.git
cd llm-chatbot
```
2. Install dependencies:
```
npm install
```
3. Set up your OpenAI API key in the config.js file:
```
module.exports = {
    OpenAIAPIKey: 'your-openai-api-key'
};
```
4. Start the server:
```
node server.js
```
5. Access the application:
* Open your web browser and go to http://localhost:3000.

### Usage

1. Open the web interface in your browser.
2. Type a message into the input box and press "Enter" or click the send button.
3. The chatbot will respond with a generated message based on the input provided.

### Code Overview

* main.js:
Handles user input, sends the message to the server, and displays the chatbot's response on the page.

* server.js:
Sets up an Express server to serve the static files and handle API requests.
Defines a route /getChatbotResponse to handle POST requests from the client, using the OpenAI API to generate responses.

* openai.js:
Contains the logic for making requests to the OpenAI API.
Includes error handling and response processing.

### Customization

* Chatbot Personality: You can customize the chatbot's personality by modifying the system message in openai.js. For example, change the line:
```
{ role: 'system', content: 'You are a helpful assistant.' }
```
to something like:
```
{ role: 'system', content: 'You are a witty and humorous assistant.' }
```

   
