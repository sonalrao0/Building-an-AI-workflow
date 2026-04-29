# 🤖 Building an AI Workflow with n8n

## 📌 Overview

This project demonstrates how to build an AI-powered workflow automation system using **n8n**, **OpenAI (GPT)**, and **Google Calendar**.

The workflow allows a user to send a simple text message, which is processed by an AI agent to automatically schedule an event in Google Calendar.

📄 Documentation reference: 

---

## 🚀 Features

* AI-powered workflow automation
* Natural language processing using OpenAI GPT
* Automated event scheduling in Google Calendar
* Dynamic data handling with JSON expressions
* Debugging using AI agent logs
* Real-time execution via chat trigger

---

## 🏗️ Architecture

```
User Input (Chat Trigger)
        ↓
   AI Agent (OpenAI GPT)
        ↓
Data Processing (JSON Expressions)
        ↓
 Google Calendar API
        ↓
 Event Scheduled
```

---

## 🧰 Tech Stack

* **n8n** – Workflow automation
* **OpenAI GPT** – AI processing
* **Google Calendar API** – Event scheduling
* **JSON** – Data formatting and expressions

---

## ⚙️ Workflow Setup

### 1. Trigger

* Chat-based trigger initiates the workflow
* Alternatives: scheduled or manual trigger

### 2. AI Agent

* Connected to the trigger
* Uses OpenAI GPT to interpret user input

### 3. OpenAI Integration

* Processes natural language into structured data

### 4. Google Calendar Integration

* Creates events based on AI-generated inputs
* Requires proper authentication and permissions

---

## 🧪 Testing & Debugging

### Initial Issues

* Events scheduled at incorrect times
* Multiple events created instead of one
* Missing input data for event timing

### Debugging Approach

* Analyzed AI agent logs
* Identified missing start and end time inputs

---

## 🔧 Fixes

### JSON Expressions

Replaced static values with dynamic AI inputs:

```
{{ $fromAI('start_time') }}
{{ $fromAI('end_time') }}
```

### System Message Improvements

* Added instructions to guide AI behavior
* Ensured correct date and time handling

### Expression-Based Configuration

* Used dynamic expressions instead of fixed values
* Enabled accurate real-time scheduling

---

## ✅ Final Outcome

* Accurate event scheduling
* Correct date and time processing
* Single execution per request
* Fully functional AI workflow

---

## 🧠 Key Concepts

* AI workflows vs AI agents
* Event-driven automation
* JSON expressions
* Prompt engineering
* API integration and debugging

---

## 🔒 Security Notes

* Remove credentials after use
* Avoid exposing API keys
* Limit access permissions

---

## 👤 Author

**Sonal Rao**
NextWork Student

---
