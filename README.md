<h1 align="center">🚀 Prompt2Code - Agentic AI Software Engineer 👩‍💻</h1>

## Table of Contents

- [About](#about)
- [Key Features](#key-features)
- [System Architecture](#system-architecture)
- [Getting Started](#getting-started)
  - [Requirements](#requirements)
  - [Installation](#installation)
  - [How to use](#how-to-use)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [Help and Support](#help-and-support)
- [License](#license)

## About

Prompt2Code is an advanced AI software engineer that can understand high-level human instructions, break them down into steps, research relevant information, and write code to achieve the given objective. Prompt2Code utilizes large language models, planning and reasoning algorithms, and web browsing abilities to intelligently develop software.

Prompt2Code aims to revolutionize the way we build software by providing an AI pair programmer who can take on complex coding tasks with minimal human guidance. Whether you need to create a new feature, fix a bug, or develop an entire project from scratch, Prompt2Code is here to assist you.

> [!NOTE]
> Prompt2Code is modeled after [Devika](https://github.com/stitionai/devika) which was modeled after [Devin](https://www.cognition-labs.com/introducing-devin) by Cognition AI. 

## Key Features

- 🤖 Supports **Claude 3**, **GPT-4**, **Gemini**, **Mistral** , **Groq** and **Local LLMs** via [Ollama](https://ollama.com). For optimal performance: Use the **Claude 3** family of models.
- 🧠 Advanced AI planning and reasoning capabilities
- 🔍 Contextual keyword extraction for focused research
- 🌐 Seamless web browsing and information gathering
- 💻 Code writing in multiple programming languages
- 📊 Dynamic agent state tracking and visualization
- 💬 Natural language interaction via chat interface
- 📂 Project-based organization and management
- 🔌 Extensible architecture for adding new features and integrations

## System Architecture

Read [**README.md**](docs/architecture) for the detailed documentation.


## Getting Started

### Requirements
```
Version's requirements
  - Python >= 3.10 and < 3.12
  - NodeJs >= 18
  - bun
```

- Install uv - Python Package manager [download](https://github.com/astral-sh/uv)
- Install bun - JavaScript runtime [download](https://bun.sh/docs/installation)
- For ollama [ollama setup guide](docs/Installation/ollama.md) (optinal: if you don't want to use the local models then you can skip this step)
- For API models, configure the API keys via setting page in UI.


### Installation

To install Prompt2Code, follow these steps:

1. Clone the Prompt2Code repository:
   ```bash
   git clone https://git.telavivmakers.space/ro/prompt2code.git
   ```
2. Navigate to the project directory:
   ```bash
   cd prompt2code
   ```
3. Create a virtual environment and install the required dependencies (you can use any virtual environment manager):
   ```bash
   python -m venv venv
   
   # On macOS and Linux.
   source .venv/bin/activate

   # On Windows.
   .venv\Scripts\activate

   uv pip install -r requirements.txt
   ```
4. Install the playwright for browsering capabilities:
   ```bash
   playwright install --with-deps # installs browsers in playwright (and their deps) if required
   ```
5. Start the Prompt2Code server:
   ```bash
   python devika.py
   ```
6. if everything is working fine, you see the following output:
   ```bash
   root: INFO   : Prompt2Code is up and running!
   ```
7. Now, for frontend, open a new terminal and navigate to the `ui` directory:
   ```bash
   cd ui/
   bun install
   bun run start
   ```
8. Access the Prompt2Code web interface by opening a browser and navigating to `http://127.0.0.1:3001`

### How to use

To start using Prompt2Code, follow these steps:

1. Open the Prompt2Code web interface in your browser.
2. To create a project, click on 'select project' and then click on 'new project'.
3. Select the search engine and model configuration for your project.
4. In the chat interface, provide a high-level objective or task description for Prompt2Code to work on.
5. Prompt2Code will process your request, break it down into steps, and start working on the task.
6. Monitor Prompt2Code's progress, view generated code, and provide additional guidance or feedback as needed.
7. Once Prompt2Code completes the task, review the generated code and project files.
8. Iterate and refine the project as desired by providing further instructions or modifications.

## Configuration

Prompt2Code requires certain configuration settings and API keys to function properly:

when you first time run Prompt2Code, it will create a `config.toml` file for you in the root directory. You can configure the following settings in the settings page via UI:

- API KEYS
   - `BING`: Your Bing Search API key for web searching capabilities.
   - `GOOGLE_SEARCH`: Your Google Search API key for web searching capabilities.
   - `GOOGLE_SEARCH_ENGINE_ID`: Your Google Search Engine ID for web searching using Google.
   - `OPENAI`: Your OpenAI API key for accessing GPT models.
   - `GEMINI`: Your Gemini API key for accessing Gemini models.
   - `CLAUDE`: Your Anthropic API key for accessing Claude models.
   - `MISTRAL`: Your Mistral API key for accessing Mistral models.
   - `GROQ`: Your Groq API key for accessing Groq models.
   - `NETLIFY`: Your Netlify API key for deploying and managing web projects.

- API_ENDPOINTS
   - `BING`: The Bing API endpoint for web searching.
   - `GOOGLE`: The Google API endpoint for web searching.
   - `OLLAMA`: The Ollama API endpoint for accessing Local LLMs.
   - `OPENAI`: The OpenAI API endpoint for accessing OpenAI models.

Make sure to keep your API keys secure and do not share them publicly. For setting up the Bing and Google search API keys, follow the instructions in the [search engine setup](docs/Installation/search_engine.md)


