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
      <img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/GPT4-logo.png" width="100"/><br>
      <b><a href="https://openai.com/gpt-4">GPT-4</a></b>
    </td>
  </tr>
</table>


---

## Features

- **Tool-based question answering** with `ToolCallingAgent` (smolagents)
- **Dynamic prompt routing** based on question type (e.g., numeric, video, historical)
- **External tools** integrated:
  - Wikipedia search
  - YouTube transcription
  - Python script execution
  - File downloading
  - Reverse text decoding
- **Regex-based answer extraction** using the `FINAL ANSWER: ...` format
- **Gradio interface** for OAuth login, agent execution, and benchmark submission

---

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/gaia-tool-routing-agent.git
   cd gaia-tool-routing-agent
