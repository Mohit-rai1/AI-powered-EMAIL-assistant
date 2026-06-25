# AI-Powered Email Assistant

An AI-powered email reply generator that helps users draft professional and context-aware email responses using Google's Gemini API. The project consists of a Spring Boot backend, a React frontend, and a Chrome Extension that integrates directly with Gmail to generate AI-powered replies inside the compose window.

---

## Features

* Generate AI-powered email replies from email content
* Gmail integration through a Chrome Extension
* Spring Boot REST API backend
* React-based frontend for testing and interaction
* Google Gemini API integration
* Secure configuration using environment variables
* Fast and user-friendly workflow

---

## Tech Stack

### Backend

* Java
* Spring Boot
* Maven
* REST APIs

### Frontend

* React.js
* JavaScript
* HTML
* CSS

### Browser Extension

* Chrome Extension APIs
* JavaScript
* Manifest V3

### AI Integration

* Google Gemini API

---

## Project Structure

```text
AI-EMAIL-ASSISTANT
│
├── email-assistant-backend
│   ├── src
│   ├── pom.xml
│   └── resources
│
├── email-assistant-frontend
│   ├── src
│   ├── public
│   └── package.json
│
└── email-assistant-extension
    ├── manifest.json
    ├── content.js
    ├── popup.js
    └── styles.css
```

---

## System Architecture

```text
+------------------+
|      Gmail       |
+--------+---------+
         |
         v
+------------------+
| Chrome Extension |
|  Content Script  |
+--------+---------+
         |
         v
+------------------+
| Spring Boot API  |
+--------+---------+
         |
         v
+------------------+
|   Gemini API     |
+--------+---------+
         |
         v
+------------------+
| Generated Reply  |
+------------------+
```

---

## Workflow

1. User opens Gmail.
2. Chrome Extension injects a "Generate Reply" button.
3. User clicks the button.
4. Email content is extracted.
5. Request is sent to the Spring Boot backend.
6. Backend calls the Gemini API.
7. Gemini generates a context-aware response.
8. Response is returned to the extension.
9. Generated reply is inserted into Gmail automatically.

---

## Setup Instructions

### Clone Repository

```bash
git clone https://github.com/Mohit-rai1/AI-powered-EMAIL-assistant.git
cd AI-powered-EMAIL-assistant
```

### Backend Setup

```bash
cd email-assistant-backend
```

Configure environment variables:

```properties
GEMINI_URL=<your-gemini-url>
GEMINI_KEY=<your-gemini-key>
```

Run the backend:

```bash
mvn spring-boot:run
```

### Frontend Setup

```bash
cd email-assistant-frontend
npm install
npm start
```

### Chrome Extension Setup

1. Open Chrome.
2. Navigate to `chrome://extensions/`
3. Enable Developer Mode.
4. Click **Load Unpacked**.
5. Select the extension folder.
6. Open Gmail and start generating AI-powered replies.

---

## Key Contributions

* Developed REST APIs using Spring Boot for AI-powered email generation.
* Integrated Google Gemini API for context-aware response generation.
* Built a Chrome Extension using Manifest V3 for Gmail integration.
* Developed a React-based interface for testing backend functionality.
* Implemented secure API key management using environment variables.
* Designed an end-to-end workflow connecting Gmail, Backend Services, and Gemini AI.

---

## Future Improvements

* Email summarization
* Multi-language support
* Custom reply styles and tones
* Response history management
* User authentication
* Email categorization and prioritization

---

## Acknowledgement

This project was inspired by educational content and implemented independently to gain hands-on experience with Spring Boot, React, Chrome Extension development, and AI integration using Google's Gemini API.

---

## License

This project was built as a learning project to explore AI integration, browser extension development, and full-stack application development.
