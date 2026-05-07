# ✍️ LangGraph Blog Writing Agent

An automated, multi-agent workflow for generating high-quality, research-backed technical blog posts. This project leverages the power of **LangGraph** for orchestration, **Google Gemini 2.5 Flash** for blazing-fast text and image generation, and **Streamlit** for an interactive, easy-to-use frontend.

## ✨ Features

* **Multi-Agent Orchestration:** Utilizes a graph-based workflow (Router → Researcher → Orchestrator → Workers → Reducer) to mimic a real editorial team.
* **Smart Web Research:** Integrates with the **Tavily API** to fetch up-to-date information, cite sources, and pull in the latest news.
* **Automated Image Generation:** Automatically decides if a section needs an image, writes a prompt, and generates contextual diagrams/images using **Gemini 2.5 Flash Image**.
* **Interactive UI:** A sleek Streamlit dashboard to input topics, monitor the agent's thought process (node by node), and preview the generated markdown.
* **Past Blog Management:** Automatically saves generated blogs as `.md` files and allows you to load and review past generations locally.
* **Export Options:** Download your final blog as a plain `.md` file or as a bundled `.zip` containing both the markdown and the locally saved images.

## 🛠️ Tech Stack

* **Frontend:** [Streamlit](https://streamlit.io/)
* **Orchestration:** [LangGraph](https://python.langchain.com/v0.1/docs/langgraph/)
* **LLM & Image Generation:** [Google Gemini 2.5 Flash](https://ai.google.dev/) (`langchain-google-genai` & `google-genai`)
* **Search / Grounding:** [Tavily API](https://tavily.com/)
* **Data Validation:** Pydantic

## 🚀 Getting Started

### 1. Prerequisites

You will need Python 3.9+ installed on your machine. You also need to obtain API keys for both Google and Tavily:
* **Google API Key:** Get it from [Google AI Studio](https://aistudio.google.com/) (Free tier works perfectly).
* **Tavily API Key:** Get it from [Tavily](https://tavily.com/) (Offers a free tier for researchers).

### 2. Installation

Clone the repository and install the required Python packages:

```bash
# Clone the repository

# Install dependencies
pip install pydantic langgraph langchain-google-genai streamlit pandas google-genai tavily-python python-dotenv
