# GitBud - AI-Powered GitHub Repository Visualizer

![React](https://img.shields.io/badge/React.js-Frontend-61DAFB?style=for-the-badge&logo=react)
![D3.js](https://img.shields.io/badge/D3.js-Visualization-orange?style=for-the-badge)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-Backend-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Hugging Face](https://img.shields.io/badge/LLaMA--3-HuggingFace-yellow?style=for-the-badge)

**Transform GitHub repositories into interactive visual knowledge maps with AI-powered code understanding.**

---

## Overview

GitBud is an AI-powered full-stack developer tool designed to simplify repository exploration and codebase understanding.

Large GitHub repositories can be difficult to navigate, especially for new contributors, students, or developers working with unfamiliar codebases. GitBud solves this by converting repository structures into **interactive hierarchical knowledge maps**, enabling users to visually explore folders, files, and code relationships in an intuitive way.

Beyond visualization, GitBud integrates **Large Language Models (LLaMA-3 via Hugging Face)** to provide intelligent repository analysis, including automated summaries, code explanations, logic interpretation, and potential bug detection.

This makes GitBud a powerful assistant for **code onboarding, architecture understanding, documentation support, and developer productivity**.

---

## Key Features

### Interactive Repository Visualization
Explore any public GitHub repository as a dynamic visual graph.

- Hierarchical tree visualization of repository structure
- Interactive node expansion for folders and files
- Zoom, pan, and navigation support
- Real-time structural exploration

---

### AI-Powered Repository Intelligence
Understand code faster with integrated AI analysis.

- Repository summary generation
- Code logic explanation
- Function/module interpretation
- AI-assisted bug detection
- Developer-friendly code insights

---

### Smart File Exploration
Inspect repository contents without leaving the platform.

- Hover previews for quick file inspection
- Click-to-view complete file content
- Backend proxy for secure GitHub content fetching
- Faster code browsing experience

---

### Search & Highlight
Quickly locate relevant files in large repositories.

- Instant repository search
- Dynamic node highlighting
- Fast navigation across complex codebases

---

### Modular Backend Architecture
Built with scalability and maintainability in mind.

- RESTful API architecture using Spring Boot
- GitHub API integration for repository metadata
- AI service integration for LLM interactions
- Structured backend service layers

---

## Problem Statement

Understanding unfamiliar repositories often requires manually browsing dozens or hundreds of files, making onboarding slow and inefficient.

GitBud addresses this challenge by combining:

- **visual repository mapping**
- **interactive exploration**
- **AI-powered code understanding**

to drastically reduce the time needed to understand complex projects.

---

## Tech Stack

### Frontend
- **React.js**
- **D3.js**
- **Tailwind CSS**
- **Vite**

### Backend
- **Java Spring Boot**
- **REST APIs**
- **GitHub REST API**

### AI Integration
- **Hugging Face Inference API**
- **LLaMA-3**

---

## System Architecture

```text
                        +----------------------+
                        |      Frontend        |
                        | React + D3.js UI     |
                        +----------+-----------+
                                   |
                                   |
                                   v
                        +----------------------+
                        |   Spring Boot API    |
                        |  Business Logic      |
                        +----------+-----------+
                                   |
            +----------------------+----------------------+
            |                                             |
            v                                             v
+--------------------------+                 +---------------------------+
|     GitHub REST API      |                 |    Hugging Face LLaMA-3   |
| Repository Metadata      |                 | AI Code Intelligence      |
+--------------------------+                 +---------------------------+
                                   |
                                   v
                        +----------------------+
                        |       Output       |
                        +----------------------+
```

---

## Workflow

### 1. Repository Input
The user enters a public GitHub repository URL.

Example:

```bash
https://github.com/facebook/react
```

---

### 2. Repository Parsing
The Spring Boot backend:

- validates the repository URL
- extracts owner/repository details
- communicates with the GitHub REST API
- fetches repository file structure

---

### 3. Data Processing
The backend organizes repository metadata into a hierarchical structure suitable for visualization.

---

### 4. Visualization Rendering
The frontend uses **D3.js** to generate an interactive radial knowledge map where:

- folders become expandable nodes
- files become terminal nodes
- relationships are visually connected

---

### 5. File Exploration
When users interact with nodes:

- hover → preview file contents
- click → fetch complete file content

This is securely handled through backend proxy APIs.

---

### 6. AI Analysis
Selected repository content is sent to **LLaMA-3 via Hugging Face**, enabling:

- code explanation
- repository summarization
- logic interpretation
- potential issue detection

---

## Installation

## Prerequisites

Make sure you have:

- Node.js (v18+)
- npm
- Java 17+
- Maven
- GitHub API token (optional)
- Hugging Face API key

---

## Backend Setup

Clone the repository:

```bash
git clone https://github.com/yourusername/gitbud.git
cd gitbud/backend
```

Configure application properties:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/gitbud
spring.datasource.username=your_username
spring.datasource.password=your_password

github.api.token=your_github_token
huggingface.api.key=your_hf_api_key
```

Install dependencies and run:

```bash
./mvnw spring-boot:run
```

Backend runs at:

```bash
http://localhost:8080
```

---

## Frontend Setup

Navigate to frontend:

```bash
cd ../frontend
```

Install dependencies:

```bash
npm install
```

Run:

```bash
npm run dev
```

Frontend runs at:

```bash
http://localhost:5173
```

---

## Example Use Cases

### New Contributors
Understand unfamiliar repositories visually before contributing.

### Students
Learn project architecture faster for academic or personal projects.

### Developers
Explore open-source repositories efficiently.

### Code Review Support
Use AI explanations to understand complex modules quickly.

### Documentation Assistance
Generate summaries of repository structure and logic.

---

## Future Enhancements

- Private repository support via GitHub OAuth
- PR/Issue summarization
- AI-generated documentation
- Commit message generation
- Architecture diagram export
- Team collaboration analytics
- Bug severity classification
- Code dependency graph visualization

---

## Screenshots

Add screenshots here:

```markdown
/assets/homepage.png
/assets/repo-visualizer.png
/assets/ai-analysis.png
```

---

## Why GitBud?

GitBud combines **visual repository exploration** with **AI-assisted code understanding**, making repository navigation significantly faster and smarter than traditional file browsing.

It is especially useful for:

- onboarding developers
- understanding open-source projects
- architecture learning
- AI-assisted debugging
- rapid repository analysis

---

## Author

**Vedant**  
Computer Engineering Student

GitHub: https://github.com/yourusername

---

## License

MIT License
