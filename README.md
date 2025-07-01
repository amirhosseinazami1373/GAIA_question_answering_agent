# GAIA Tool-Routing Question Answering Agent using smolagents, LangChain, and GPT-4

This project implements a **tool-routing AI agent** capable of answering questions from the [GAIA benchmark](https://huggingface.co/learn/agents-course/en/unit4/what-is-gaia), as part of the final assignment from the [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit4/hands-on). The agent uses **GPT-4**, prompt engineering, and multiple external tools to reason through complex queries and return precise, structured answers.

The minimum requirement is to correctly answer **7 out of 20 Level-1 GAIA questions**. This project meets that benchmark using dynamic prompting and modular tool routing.

---

## Technologies Used

<table>
  <tr>
    <td align="center">
      <img src="https://huggingface.co/datasets/huggingface/documentation-images/resolve/main/smolagents/smolagents.png" width="200"/><br>
      <b><a href="https://github.com/huggingface/smolagents">smolagents</a></b>
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/langchain-ai/.github/main/profile/logo-dark.svg" width="200"/><br>
      <b><a href="https://www.langchain.com/">LangChain</a></b>
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/TypingMind/model-icons/refs/heads/main/icons/gpt-4.webp" width="100"/><br>
      <b><a href="https://openai.com/gpt-4">GPT-4</a></b>
    </td>
  </tr>
</table>


---

## Features

- 🧠 **Tool-based question answering** with `ToolCallingAgent` from smolagents  
- 🧭 **Dynamic prompt routing** for different question types:
  - Numeric questions
  - Location-based queries
  - YouTube transcript extraction
  - Historical reasoning
  - Identifier/code lookups
  - Reversed logic puzzles
- 🧰 **Custom tools implemented**:
  - Wikipedia search
  - YouTube transcription
  - Python script execution
  - File downloading
  - Reverse string decoding
- ✅ **Structured outputs** in the format: `FINAL ANSWER: [your answer]`
- 🌐 **Gradio interface** for Hugging Face OAuth, running, and result display
- 📦 **Submission-ready pipeline** for GAIA scoring via Hugging Face API

---

## Installation

 **1. Clone the repository:**

   ```bash
   git clone https://github.com/your-username/gaia-tool-routing-agent.git
   cd gaia-tool-routing-agent
   ```

**2. Install dependencies:**

```bash
pip install -r requirements.txt
```

**3. Add Your API Keys as Environment Variables**

To access **OpenAI**, set your API keys as environment variables. This ensures secure access and prevents hard-coding sensitive information in the code.

  ### For Mac/Linux:
  Open your terminal and run:
  ```bash
  export OPENAI_API_KEY="your-openai-api-key"
   ```
  ### For Windows (Command Prompt):

  ```bash
  set OPENAI_API_KEY="your-openai-api-key"
  ```
  ### For Windows (PowerShell):

  ```bash
  $env:OPENAI_API_KEY="your-openai-api-key"
  ```
  ## Usage
  **1. Run the Gradio interface:**
  ```bash
  python app.py
```
  **2. Intract with the agent:**
  
  Log in via Hugging Face

  Click “Run Evaluation & Submit All Answers”

  Review the table of results and see your GAIA score

  ## Agent workflow:

  🔍 Question Classification: Determines type (e.g., numeric, name, historical)

  📄 Prompt Injection: Constructs a prompt tailored to that question type

  🔧 Tool Execution: LLM (GPT-4) uses external tools via ToolCallingAgent

  🧠 LLM Reasoning: Reasoning chain up to 7 steps

  ✅ Answer Extraction: Regex pattern parses and cleans FINAL ANSWER: ...

  📤 Submission: Posts all answers and code reference to the GAIA server




  
