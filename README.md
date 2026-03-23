#  Agentic Chatbot with LangGraph

An **agent-based chatbot system** built using modular components and graph-based orchestration. This project demonstrates how to design scalable AI workflows using nodes, tools, and LLM integrations.

---

##  Project Structure

```
AGENTIC_CHATBOT/
│
├── AINews/
│   └── monthly_summary.md        # Generated AI news summaries
|   ├── weekly_summary.md
│   └── daily_summary.md
|
├── src/
│   ├── Langgraph_Agentic_Ai/
│   │
│   │   ├── graph/
│   │   │   └── graph_builder.py  # Builds the agent workflow graph
│   │
│   │   ├── LLMs/
│   │   │   └── groqllm.py        # LLM integration (Groq or similar)
│   │
│   │   ├── nodes/
│   │   │   ├── ai_news_node.py
│   │   │   ├── basic_chatbot_node.py
│   │   │   └── chatbot_with_Tool_node.py
│   │
│   │   ├── state/
│   │   │   └── state.py          # Shared state across graph nodes
│   │
│   │   ├── tools/
│   │   │   └── search_tool.py    # External tool integrations
│   │
│   │   └── ui/
│   │       └── streamlit_ui/
│   │           ├── display_result.py
│   │           └── loadui.py     # Streamlit UI logic
│   │
│   ├── uiconfigfile.ini         # UI configuration
│   ├── uiconfigfile.py
│   └── main.py                  # Entry point
│
├── .venv/                      # Virtual environment
└── .gitignore
```

---

##  Features

*  **Agentic Architecture** using graph-based execution
* Modular **nodes for different tasks**
*  Tool integration (e.g., search functionality)
* Multiple chatbot modes:

  * Basic chatbot
  * Tool-augmented chatbot
  * AI news summarizer
*  **Streamlit UI** for interactive usage
*  Scalable and extensible design

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd AGENTIC_CHATBOT
```

### 2. Create virtual environment

```bash
python -m venv .venv
source .venv/bin/activate   # Mac/Linux
.venv\Scripts\activate      # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```


---

## ▶ Running the Project

### Run the main application

```bash
python src/main.py
```

### Run Streamlit UI

```bash
streamlit run src/Langgraph_Agentic_Ai/ui/streamlit_ui/loadui.py
```

---

##  Core Components

### 1. Graph Builder

* Defines workflow between nodes
* Controls execution flow of agents

### 2. Nodes

* `basic_chatbot_node` → simple LLM chat
* `chatbot_with_Tool_node` → chat + tool usage
* `ai_news_node` → generates AI news summaries

### 3. State Management

* Centralized state shared across nodes

### 4. Tools

* External capabilities like search APIs

### 5. LLM Integration

* Handles communication with language models

---

