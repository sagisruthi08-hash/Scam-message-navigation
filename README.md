# 🕵️ Scam Message Investigator

### AI-Powered Scam Message Detection Using Ollama, Python, and Streamlit

## 📌 Project Overview

**Scam Message Investigator** is an AI-powered application designed to analyze suspicious messages and help users identify potential scams, phishing attempts, and fraudulent communications.

The application uses a locally running Large Language Model (LLM) through **Ollama** to examine messages and provide an explanation of potential scam indicators. The user interface is developed using **Streamlit**, and the application is built and managed using **Visual Studio Code (VS Code)**.

The primary goal of this project is to improve digital awareness and help users make safer decisions when receiving suspicious messages.

## 🎯 Objectives

* Detect potential scam messages using Artificial Intelligence.
* Analyze suspicious text messages, emails, and promotional messages.
* Identify warning signs such as suspicious links, urgent requests, and requests for personal information.
* Provide explanations to help users understand why a message may be suspicious.
* Use a locally running AI model to analyze messages without requiring a cloud-based LLM API.
* Promote cybersecurity awareness and safe online communication.

## 🛠️ Technologies Used

| Technology         | Purpose                                       |
| ------------------ | --------------------------------------------- |
| Python             | Core programming language                     |
| Ollama             | Runs the local Large Language Model           |
| Gemma 3:1B         | AI model used for message analysis            |
| Streamlit          | Creates the interactive web application       |
| Visual Studio Code | Code development and project management       |
| Requests           | Sends requests to the local Ollama API        |
| JSON               | Handles structured data and API communication |

## ⚙️ System Requirements

* Windows 10 or Windows 11
* Python 3.10 or a compatible version
* Visual Studio Code
* Ollama installed on the system
* Internet connection for initial software and model downloads
* Sufficient RAM and storage to run the selected AI model

## 📂 Project Structure

```text
Scam-Message-Investigator/
│
├── app.py
├── requirements.txt
├── README.md
└── .gitignore
```

### File Description

* **app.py:** Contains the Python code for the Streamlit application and communication with Ollama.
* **requirements.txt:** Lists the Python libraries required to run the application.
* **README.md:** Documents the project, setup instructions, and usage.
* **.gitignore:** Specifies files that should not be uploaded to GitHub.

## 🚀 Installation and Setup

### Step 1: Install Python

Download and install Python from:

https://www.python.org/downloads/

During installation, enable **Add Python to PATH** if the installer provides that option.

Verify the installation:

```powershell
python --version
```

### Step 2: Install Visual Studio Code

Download VS Code from:

https://code.visualstudio.com/

Open VS Code and install the Python extension.

### Step 3: Install Ollama

Download Ollama from:

https://ollama.com/download

Install it and open PowerShell or the VS Code terminal.

Verify the installation:

```powershell
ollama --version
```

### Step 4: Download the AI Model

Run the following command in the terminal:

```powershell
ollama pull gemma3:1b
```

This downloads the Gemma 3 1B model to your computer.

To verify the downloaded model, run:

```powershell
ollama list
```

### Step 5: Create the Project Folder

Create a folder named:

```text
Scam-Message-Investigator
```

Open this folder in Visual Studio Code.

Create the following files:

```text
app.py
requirements.txt
README.md
.gitignore
```

### Step 6: Create a Virtual Environment

Open the VS Code terminal and run:

```powershell
python -m venv venv
```

Activate the virtual environment:

```powershell
.\venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, you can use Command Prompt instead:

```cmd
venv\Scripts\activate.bat
```

### Step 7: Install the Required Libraries

Add the following dependencies to `requirements.txt`:

```text
streamlit
requests
```

Install them using:

```powershell
python -m pip install -r requirements.txt
```

### Step 8: Start Ollama

Ollama must be running locally for the application to communicate with the AI model.

If Ollama is not already running as a background application, open another terminal and run:

```powershell
ollama serve
```

If Ollama is already running, you do not need to start another server.

The default local API endpoint is:

```text
http://localhost:11434/api/chat
```

### Step 9: Run the Application

In the VS Code terminal, navigate to your project folder and run:

```powershell
python -m streamlit run app.py
```

Streamlit will start the application and display a local URL, usually:

```text
http://localhost:8501
```

Open this URL in your browser to use the Scam Message Investigator.

## 🔍 How the Application Works

The application follows these steps:

1. **User Input:** The user enters a suspicious message into the Streamlit interface.
2. **Message Processing:** The application collects the message and prepares it for analysis.
3. **AI Analysis:** The Python application sends the message to the locally running Ollama API.
4. **Language Model Processing:** The Gemma 3 1B model analyzes the message for potential scam indicators.
5. **Result Generation:** The model generates an explanation and an assessment of the message.
6. **Result Display:** Streamlit displays the AI-generated response to the user.

### Workflow

```text
        User
         |
         v
  Enter Suspicious Message
         |
         v
  Streamlit User Interface
         |
         v
    Python Application
         |
         v
    Ollama Local API
         |
         v
     Gemma 3:1B Model
         |
         v
   Analyze the Message
         |
         v
  Generate AI Assessment
         |
         v
  Display Results in UI
```

## ✨ Key Features

### 1. AI-Based Message Analysis

Uses a Large Language Model to examine message content and identify possible warning signs.

### 2. Suspicious Message Detection

Helps users recognize potentially fraudulent messages involving fake offers, suspicious links, impersonation, and requests for money.

### 3. Explanation of Scam Indicators

Provides explanations of suspicious language, unusual requests, and other potential warning signs.

### 4. Interactive User Interface

Streamlit provides a simple interface for entering messages and viewing AI-generated results.

### 5. Local AI Processing

Uses Ollama to run the language model on the user's computer rather than sending prompts to a cloud-based LLM API.

### 6. No Separate Groq API Key Required

The project can use Ollama's local API without requiring a Groq API key.

## 🔐 Privacy and Security

This project is designed to perform AI analysis using a locally running Ollama model.

* Message prompts are processed by the local model when using the local Ollama endpoint.
* No separate cloud LLM API key is required.
* Users should avoid entering passwords, banking credentials, OTPs, or other sensitive personal information.
* External links and phone numbers should be verified independently before taking action.

**Important:** Local AI analysis does not guarantee that every message stays entirely offline. Network activity, other application components, and any external services used by the application may affect privacy.

## ⚠️ Limitations

* AI predictions may sometimes be incorrect.
* Legitimate messages may be classified as suspicious.
* Sophisticated scams may not be detected.
* The model's performance depends on its capabilities and the information contained in the message.
* The application cannot independently verify the identity of a sender or guarantee that a website is safe.

**Disclaimer:** This tool is intended for educational purposes and cybersecurity awareness. It should not be treated as a replacement for professional security tools or independent verification.

## 🔮 Future Enhancements

* Add a clear risk-level indicator: Low, Medium, or High.
* Support bulk message analysis.
* Add suspicious URL analysis.
* Provide recommendations for responding to suspicious messages.
* Add a message history feature.
* Support multiple languages.
* Improve results using structured AI-generated responses.
* Develop a mobile-friendly interface.
* Add optional integrations with trusted threat-intelligence services.

## 🎓 Learning Outcomes

Through this project, the developer gains practical experience in:

* Python application development.
* Integrating Large Language Models with applications.
* Running AI models locally using Ollama.
* Building interactive web applications with Streamlit.
* Sending HTTP requests to local APIs.
* Understanding basic scam detection and cybersecurity awareness.
* Managing software projects using Visual Studio Code.

## 👩‍💻 Developed Using

* Python
* Ollama
* Gemma 3:1B
* Streamlit
* Visual Studio Code

## 📜 License

This project is intended for educational and learning purposes. A suitable open-source license can be added if the project is distributed publicly.

---

**Scam Message Investigator — Use AI to Think Before You Click!** 🛡️
