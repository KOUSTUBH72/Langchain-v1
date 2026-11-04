# LangChain Introduction – Building AI Agents

## 1. Project Overview

This project is a hands-on introduction to building AI agents using **LangChain v1** and Large Language Models (LLMs).

The primary objective is to understand the fundamentals of AI agent development, including agent initialization, LLM integration, tool creation, tool calling, system prompts, and agent execution.

This project is part of my practical learning journey toward becoming an **AI Security Engineer**, focusing on understanding how AI agents work internally before exploring their security vulnerabilities and protection mechanisms.

## 2. Learning Objectives

The project covers the following concepts:

- Introduction to LangChain v1.
- Understanding the LangChain framework.
- Checking the installed LangChain version.
- Managing environment variables using Python-dotenv.
- Initializing AI agents using `create_agent()`.
- Integrating different LLM providers.
- Understanding system prompts and agent instructions.
- Creating custom Python tools for AI agents.
- Registering tools with an AI agent.
- Understanding tool calling and execution.
- Executing agents using `agent.invoke()`.
- Understanding agent responses and message history.
- Extracting final responses from agent execution.

## 3. Technologies and Tools Used

| Technology | Purpose |
|---|---|
| Python 3.13+ | Programming language |
| LangChain | AI agent development framework |
| LangChain Community | Additional integrations |
| LangChain OpenAI | OpenAI model integration |
| LangChain Groq | Groq model integration |
| LangChain Google GenAI | Google Gemini integration |
| Python-dotenv | Environment variable management |
| Jupyter Notebook | Interactive development |
| IPython Kernel | Notebook execution |
| UV | Python package and dependency management |

## 4. Project Structure

```text
AI-Agent-Project/
│
├── updatedlangchain/
│
├── 1-langchainintro.ipynb
├── main.py
├── README.md
├── requirements.txt
├── pyproject.toml
├── uv.lock
├── .gitignore
└── .env.example
```

## 5. Key Concepts and Implementation

### 5.1 Environment Configuration

Environment variables are used to manage API credentials securely.

The project uses `python-dotenv` to load environment variables from a local `.env` file.

This approach helps separate sensitive credentials from application source code.

### 5.2 AI Agent Initialization

The project demonstrates how to initialize an AI agent using LangChain's `create_agent()` function.

An agent is configured with:

- An LLM model.
- A collection of tools.
- A system prompt defining the agent's behavior.

### 5.3 Custom Tool Creation

A basic weather function is created using Python.

Example:

```python
def get_weather(city: str) -> str:
    """Get the weather for a city."""
    return f"The weather is {city} is Sunny."
```

This function demonstrates how custom Python functions can be registered as tools and made available to an AI agent.

**Note:** This is a demonstration function that returns hardcoded weather information. It does not retrieve real-time weather data from an external API.

### 5.4 LLM Integration

This function demonstrates how custom Python functions can be registered as tools and made available to an AI agent.

Note: This is a demonstration function that returns hardcoded weather information. It does not retrieve real-time weather data from an external API.

5.4 LLM Integration

The project explores integrations with different LLM providers, including:

Google Gemini.

Groq.

OpenAI integration dependencies.

These integrations provide an understanding of how different model providers can be connected to LangChain-based applications.

5.5 Agent Execution

The agent is executed using LangChain's invoke() method.

Example:

response = agent.invoke({
    "messages": [
        {
            "role": "user",
            "content": "What is the weather like in New York?"
        }
    ]
})

The final response can be extracted using:

response['messages'][-1].content

The returned message history can also be inspected to understand the agent's execution and response flow.

6. Installation and Setup

Prerequisites

Python 3.13 or newer.

Git.

UV package manager (recommended).

API credentials for the LLM provider being used.

Step 1: Clone the Repository

git clone <YOUR_GITHUB_REPOSITORY_URL>

Step 2: Navigate to the Project Directory

cd AI-Agent-Project

Step 3: Install UV

If UV is not installed:

pip install uv

Step 4: Install Project Dependencies

Using UV:

uv sync

Alternatively, using pip:

pip install -r requirements.txt

Step 5: Configure Environment Variables

Create a .env file in the root directory.

Add the API credentials required by your selected LLM provider.

Example:

GROQ_API_KEY=your_groq_api_key
GOOGLE_API_KEY=your_google_api_key
OPENAI_API_KEY=your_openai_api_key

Only configure the credentials required by your implementation.

Security Warning: Never upload your actual .env file or API keys to GitHub.

Step 6: Run the Jupyter Notebook

Start Jupyter Notebook:

uv run jupyter notebook

Open the following notebook:

1-langchainintro.ipynb

Execute the notebook cells sequentially.

7. Dependency Management

This project uses UV for Python dependency management.

The project contains the following dependency files:

File

Description

pyproject.toml

Project metadata and dependency definitions

uv.lock

Locks resolved dependency versions

requirements.txt

Alternative dependency installation using pip

Main Dependencies

ipykernel>=7.4.0
langchain>=1.4.8
langchain-community>=0.4.2
langchain-google-genai>=4.4.2
langchain-groq>=1.1.3
langchain-openai>=1.7.3
python-dotenv>=1.2.4

8. Future Improvements

This project establishes the foundation for exploring more advanced AI agent development concepts.

Planned improvements include:

Integrating real-world APIs.

Building AI agents with multiple tools.

Exploring multi-agent architectures.

Understanding agent memory and state management.

Implementing input validation and output filtering.

Exploring secure tool execution.

Implementing access control mechanisms.

Studying prompt injection attacks.

Understanding jailbreak vulnerabilities.

Exploring sensitive information disclosure.

Testing AI agents against security vulnerabilities.

Implementing security guardrails and monitoring.

9. AI Security Learning Focus

Understanding AI agent architecture is an important foundation for AI application security.

This project provides an opportunity to understand:

How agents interact with LLMs.

How user instructions are processed.

How tools are registered and executed.

How agents interact with external capabilities.

How agent responses are generated.

The next stage of development will focus on identifying potential security weaknesses in AI agents and implementing appropriate security controls.

10. Project Status

Current Status: Beginner-level practical implementation – In Progress.

Learning Track: AI Engineering → AI Agent Development → AI Security Engineering.

The project will be extended with additional agent capabilities, security testing, and practical security implementations as part of the ongoing learning journey.

