# Scam Message Investigator

**An AI-powered digital safety application for identifying suspicious messages using locally running Large Language Models.**

https://scam-message-detector-nsbedfcimm4p68vcqff7ps.streamlit.app/

## About the Project

Scam Message Investigator is a Python-based application designed to help users examine suspicious digital messages and understand potential scam indicators.

With the increasing number of fraudulent SMS messages, phishing emails, fake job offers, payment requests and impersonation attempts, identifying suspicious communication has become important.

This project uses **Gemma 3:1B**, running locally through **Ollama**, to analyze user-submitted messages and generate structured investigation reports.

The application identifies potentially suspicious phrases, explains associated risks and provides practical safety recommendations through an interactive Streamlit dashboard.

## Key Features

### 1. Intelligent Message Analysis
Analyzes user-submitted SMS messages, emails, WhatsApp messages and online offers using a locally running AI model.

### 2. Risk Classification
Categorizes analyzed messages into three levels:

| Classification | Meaning |
|---|---|
| Low Concern | No clear suspicious indicators identified |
| Medium Concern | Some potentially suspicious patterns detected |
| High Concern | Significant warning signs identified |

### 3. Warning Sign Identification
Detects potential indicators such as:
- Urgent threats and unusual pressure.
- Requests for OTPs, passwords and banking information.
- Suspicious links and download requests.
- Advance payment requests.
- Fake job and prize announcements.
- Impersonation and unrealistic promises.

### 4. AI-Generated Investigation Report
Generates a structured report containing:
- Risk classification.
- Message category.
- Investigation summary.
- Identified warning signs.
- Recommended safety actions.
- Investigation limitations.

### 5. Local AI Processing
Uses Ollama to execute Gemma 3:1B locally rather than depending on a cloud-based AI API.

### 6. Investigation History
Maintains previously analyzed messages and their risk classifications during the current application session.

## How It Works

The application follows a simple AI investigation workflow:

```text
       User Input
           |
           v
   Suspicious Message
           |
           v
    Streamlit Interface
           |
           v
      Ollama API
           |
           v
      Gemma 3:1B
           |
           v
    Message Analysis
           |
           v
    JSON Response
           |
           v
   Investigation Report
           |
           v
    Safety Recommendations
```

## Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| Frontend | Streamlit |
| AI Model | Gemma 3:1B |
| Local AI Runtime | Ollama |
| API Communication | Requests |
| Response Format | JSON |
| Styling | Custom CSS |

## Project Structure

```text
Scam-Message-Investigator/
│
├── app.py
│
├── requirements.txt
│
└── README.md
```

## Installation Guide

### Prerequisites

Before running the application, ensure that you have:

- Python 3.9 or later.
- Ollama installed.
- Gemma 3:1B model downloaded.
- Required Python libraries installed.

### Step 1: Clone the Repository

```bash
git clone https://github.com/Jascinth-Rhema/Scam-Message-Investigator.git
```

### Step 2: Open the Project Directory

```bash
cd Scam-Message-Investigator
```

### Step 3: Install Python Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Install Ollama

Download Ollama from:

https://ollama.com/

### Step 5: Download the AI Model

```bash
ollama pull gemma3:1b
```

### Step 6: Verify the Model

```bash
ollama list
```

### Step 7: Start the Application

```bash
streamlit run app.py
```

The application will be available at:

http://localhost:8501

**Note:** Ollama must be running locally while using the application. The Streamlit interface communicates with the Ollama API through port 11434.

## Example Use Cases

The application can be used to investigate:

- Bank account verification messages.
- Suspicious payment and refund requests.
- Fake work-from-home job offers.
- Unexpected prize and lottery notifications.
- Phishing messages containing suspicious links.
- Messages requesting confidential personal information.

## Security and Privacy

- Message analysis is performed using a locally running AI model.
- The application does not require an external AI API key.
- Submitted messages are sent to the local Ollama service.
- The application does not independently verify message senders, websites or financial transactions.

## Limitations

- AI-generated classifications may not always be accurate.
- Message text alone cannot establish whether a sender is genuine.
- URL reputation and website authenticity are not independently checked.
- The application cannot guarantee detection of every scam.
- Results should be treated as guidance rather than definitive fraud verification.

## Future Improvements

- Phishing URL detection and reputation checking.
- Screenshot and image-based message investigation.
- Multilingual scam detection.
- Email sender and header analysis.
- Downloadable investigation reports.
- Integration with external threat intelligence sources.

## Project Objective

The primary objective of this project is to explore how locally running Large Language Models can support digital awareness and help users recognize potentially fraudulent communication.
