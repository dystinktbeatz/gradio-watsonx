# 📌 **Gradio + Watsonx.ai LLM Chatbot**

*A hands-on project integrating Gradio interfaces with IBM Watsonx.ai Large Language Models.*

---

## 🚀 **Overview**

This project demonstrates how to build an **interactive web-based interface** using **Gradio** and connect it to IBM’s **watsonx.ai LLMs** (such as Granite 3.3 8B or Mixtral 8×7B).

The goal is to create a simple, clean, and effective **customer support–style chatbot** with:

* a front-end built using Gradio
* a backend powered by watsonx.ai
* additional demo applications (sum calculator, UI component demo, etc.)

This repository follows the structure and steps from the **IBM Coursera Generative AI course**, rewritten in a clean, easy-to-understand format.

---

## 🎯 **Key Features**

### ✔ Gradio-based Web Interface

* Fast, no-HTML-required UI for interacting with Python functions
* Input/output widgets such as

  * Textbox
  * Number
  * Slider
  * Dropdown
  * Checkbox
  * File upload
  * Radio buttons

### ✔ Watsonx.ai LLM Integration

* Connects to IBM’s Granite 3.3 8B or Mixtral 8×7B
* Sends user queries to LLM
* Receives generated text responses
* Easy model switching by changing `model_id`

### ✔ Full Lab Implementation

Includes:

* Virtual environment setup
* Dependency installation
* Multiple Gradio demos
* LLM quickstart examples
* A complete chatbot interface

---

## 🧠 **What You Will Learn**

* How to build **Gradio interfaces**
* How to work with different **Gradio input/output types**
* How to set up **IBM watsonx.ai** LLM models
* How to wrap LLMs using **LangChain + WatsonxLLM**
* How to integrate LLM inference into a web app
* How to deploy and test interactive Python applications

---

# 🛠️ **Project Structure**

```
.
├── gradio_demo.py            # Simple text echo & calculator demo
├── common_input_types.py     # Demonstration of common Gradio components
├── simple_llm.py             # Terminal-based LLM Q&A bot
├── llm_chat.py               # Full Gradio chatbot connected to watsonx.ai
├── requirements.txt          # Project dependencies
└── README.md                 # This documentation
```

---

# 🔧 **Setup Instructions**

### 1️⃣ **Clone the repository**

```bash
git clone https://github.com/dystinktbeatz/gradio-watsonx.git
cd gradio-watsonx
```

---

### 2️⃣ **Create and activate virtual environment**

```bash
pip install virtualenv
virtualenv my_env
source my_env/bin/activate
```

---

### 3️⃣ **Install dependencies**

```bash
pip install -r requirements.txt
```

---

# 🖥️ **Run the Demo Projects**

---

## ▶️ **1. Gradio Basics: Text Echo Demo**

```bash
python3.11 gradio_demo.py
```

Opens a Gradio interface with:

* text input
* text output
* real-time display

---

## ▶️ **2. Common Components Demo**

```bash
python3.11 common_input_types.py
```

This app demonstrates:

* sliders
* dropdowns
* checkbox groups
* multiselect
* radio buttons
* examples table

Useful for understanding Gradio UI design.

---

## ▶️ **3. Terminal-only LLM Q&A Bot**

```bash
python3.11 simple_llm.py
```

You can type questions inside your terminal and receive answers from:

* Granite 3.3 8B
  OR
* Mixtral 8×7B (switchable)

---

## ▶️ **4. Full Gradio + Watsonx Chatbot**

```bash
python3.11 llm_chat.py
```

Features:

* Gradio chatbot UI
* User textbox for input
* Multi-line output response
* Live LLM inference
* Customizable parameters
* Title + description

---

# ⚡ **Switching Models (Granite ↔ Mixtral)**

Inside any LLM script, modify:

```python
# Granite 3.3 8B
model_id = 'ibm/granite-3-3-8b-instruct'

# Mixtral 8×7B
# model_id = 'mistralai/mistral-small-3-1-24b-instruct-2503'
```

Restart the script to use the new model.

---

# 🧩 **How LLM Integration Works**

This project uses:

### 🔹 **WatsonxLLM (LangChain Wrapper)**

* Handles authentication
* Manages API calls
* Sends user prompts
* Receives generated text

### 🔹 **Gradio Interface**

* Captures user input
* Sends it to backend function
* Displays formatted response
* Creates interactive front end

Together, they form a complete **chat pipeline**.

---

# 🧪 **Example LLM Call**

```python
from langchain_ibm import WatsonxLLM
response = watsonx_llm.invoke("Explain what a data scientist does.")
```

---

# 🛡️ **Notes on API Access**

This project uses a special `"skills-network"` project ID provided for the IBM Cloud IDE labs.
For local use, you must generate proper credentials from your own IBM Cloud account.

---
---

# 📘 **Future Improvements**

* Add RAG using Watsonx + ChromaDB
* Add chat history
* Add style customization (CSS)
* Deploy to HuggingFace Spaces
* Docker containerization
* Notebook version

---

---

# 🙌 **Acknowledgements**

This project is inspired by the IBM coursera course materials on:

* Gradio
* Watsonx.ai
* LangChain
* LLM Application Development

