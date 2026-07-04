<div align="center">

# NexusFlow Enterprise
### AI-Powered Intelligent Financial Invoice Intelligence Platform

<p align="center">
Enterprise-grade Multi-Agent AI platform that automates invoice verification, financial validation, discrepancy detection, intelligent ticket generation, and executive analytics using LangGraph, Google Gemini, FastAPI, and Streamlit.
</p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3.11-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-green)
![LangGraph](https://img.shields.io/badge/LangGraph-MultiAgent-orange)
![Gemini](https://img.shields.io/badge/Google-Gemini-red)
![SQLite](https://img.shields.io/badge/SQLite-Database-lightgrey)
![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-ff4b4b)
![License](https://img.shields.io/badge/License-MIT-blue)

</p>

---

## Table of Contents

- Overview
- Features
- Architecture
- AI Agent Pipeline
- Workflow
- Dashboard
- Project Structure
- Technologies Used
- Database Design
- Installation
- Running the Project
- Future Enhancements
- Author

---

# Overview

NexusFlow Enterprise is an AI-powered financial invoice intelligence platform designed to automate invoice auditing for finance teams.

Instead of manually verifying invoices, checking totals, identifying mismatches, and creating support tickets, NexusFlow performs the entire workflow automatically using a Multi-Agent AI architecture.

The platform combines OCR, Google Gemini, LangGraph orchestration, FastAPI APIs, SQLite storage, and Streamlit dashboards to create an intelligent invoice auditing ecosystem.

The system reduces manual effort, increases auditing accuracy, and provides finance executives with real-time operational insights.

---

# Why NexusFlow?

Traditional invoice verification requires finance teams to

- Read invoices manually
- Verify totals
- Compare invoice values
- Detect inconsistencies
- Raise support tickets
- Maintain audit records

NexusFlow automates the complete workflow with AI.

---

# Key Features

## Invoice Processing

- PDF Invoice Upload
- Image Invoice Upload
- OCR Text Extraction
- Structured Invoice Parsing
- Vendor Identification
- Invoice Metadata Extraction

---

## AI Intelligence

- Google Gemini Document Understanding
- Multi-Agent Financial Reasoning
- Invoice Amount Validation
- Financial Consistency Checking
- Intelligent Decision Making
- Context-aware Invoice Analysis

---

## Workflow Automation

- LangGraph State Machine
- Automated Validation
- Auto Correction
- Ticket Generation
- Decision Routing
- Database Synchronization

---

## Dashboard

- Executive KPIs
- Invoice Analytics
- Vendor Analytics
- Ticket Dashboard
- Decision Distribution
- Recent Activities
- AI Summary

---

## Backend

- FastAPI REST APIs
- SQLite Integration
- SQLAlchemy ORM
- Modular Architecture
- Scalable Services

---

# System Architecture

```
                    Invoice Upload
                           │
                           ▼
                  OCR Extraction Agent
                           │
                           ▼
               Document Understanding Agent
                           │
                           ▼
               Financial Validation Agent
                           │
            ┌──────────────┴──────────────┐
            │                             │
            ▼                             ▼
     Auto Correction Agent          Ticket Agent
            │                             │
            └──────────────┬──────────────┘
                           ▼
                    SQLite Database
                           │
                           ▼
                 Executive Dashboard
```

---

# AI Agent Architecture

NexusFlow is built using a Multi-Agent Architecture powered by LangGraph.

Each agent performs a dedicated responsibility within the workflow.

---

## 1. OCR Agent

Responsibilities

- Reads uploaded invoice
- Extracts raw text
- Converts scanned documents into machine-readable format

Input

Invoice PDF/Image

Output

Extracted invoice text

---

## 2. Document Intelligence Agent

Powered by Google Gemini

Responsibilities

- Understand invoice context
- Extract vendor details
- Extract invoice number
- Extract total amount
- Extract taxes
- Extract line items

Output

Structured Invoice JSON

---

## 3. Financial Validation Agent

Responsibilities

- Verify invoice totals
- Validate calculations
- Detect amount mismatches
- Identify inconsistencies

Decision

- Valid Invoice
- Invalid Invoice

---

## 4. Decision Agent

Business Logic

If invoice is correct

→ Auto Correction

Else

→ Raise Financial Ticket

---

## 5. Storage Agent

Responsibilities

- Save invoice
- Save validation result
- Save ticket
- Update dashboard

---

# LangGraph Workflow

```
Invoice

   │

   ▼

OCR Agent

   │

   ▼

Document Agent

   │

   ▼

Finance Agent

   │

   ▼

Decision Agent

   │

   ▼

Database

   │

   ▼

Dashboard
```

The workflow is orchestrated using LangGraph, enabling modular, scalable, and state-driven execution where every agent focuses on a single responsibility.

---

# Dashboard

The Streamlit Dashboard provides executive insights including

### Executive KPIs

- Total Invoices
- Vendors
- Amount Audited
- Open Tickets
- Auto Corrections
- Validation Accuracy

---

### Analytics

- Vendor Spending
- Monthly Invoice Trends
- Invoice Distribution
- Ticket Analysis
- Decision Distribution
- Highest Invoice Amount
- Average Invoice Value

---

### Activity

- Latest Processed Invoices
- Recent Tickets
- AI Validation Summary

---

# Workflow

```
Upload Invoice

↓

OCR Extraction

↓

Gemini Understanding

↓

Invoice Parsing

↓

Financial Validation

↓

Decision Engine

↓

Auto Correct
        OR
Raise Ticket

↓

Save Database

↓

Update Dashboard
```

---

# Project Structure

```
NexusFlow/
│
├── app/
│
├── agents/
│   ├── ocr_agent.py
│   ├── document_agent.py
│   ├── finance_agent.py
│   ├── action_agent.py
│
├── api/
│
├── workflow/
│
├── database/
│
├── schemas/
│
├── ui/
│
├── uploads/
│
├── tests/
│
├── requirements.txt
│
└── README.md
```

---

# Technologies Used

## Artificial Intelligence

- Google Gemini
- LangGraph
- OCR
- Multi-Agent AI

---

## Backend

- FastAPI
- SQLAlchemy
- SQLite
- Pydantic

---

## Frontend

- Streamlit
- Plotly

---

## Programming

- Python

---

# Database

SQLite stores

- Invoice Details
- Vendor Information
- Validation Results
- Ticket Status
- AI Decisions
- Audit Logs

---

# Installation

Clone Repository

```bash
git clone https://github.com/manasaavarmaa/NexusFlow.git
```

Move into Project

```bash
cd NexusFlow
```

Install Dependencies

```bash
pip install -r requirements.txt
```

Run Backend

```bash
python run_api.py
```

Run Dashboard

```bash
streamlit run app/ui/dashboard.py
```

---

# Dashboard Pages

- Executive Dashboard
- Invoice Center
- Analytics Dashboard
- Ticket Center
- Vendor Insights
- AI Summary

---

# Screenshots

## Executive Dashboard

(Add Screenshot)

---

## Invoice Center

(Add Screenshot)

---

## Analytics Dashboard

(Add Screenshot)

---

## Ticket Management

(Add Screenshot)

---

# Future Enhancements

- Purchase Order Matching
- ERP Integration
- SAP Integration
- Vendor Risk Scoring
- Fraud Detection AI
- Role-Based Authentication
- PostgreSQL Support
- Docker Deployment
- Kubernetes Deployment
- AWS Deployment
- Azure Deployment
- Email Notifications
- Slack Integration
- Predictive Invoice Analytics

---

# Highlights

- Enterprise-inspired Financial Platform
- Multi-Agent AI Architecture
- LangGraph Workflow Orchestration
- Google Gemini Integration
- Automated Invoice Validation
- Intelligent Ticket Generation
- Executive Analytics Dashboard
- Modular Scalable Architecture
- Production-ready Backend Design

---

# Author

## Samanuri Sri Manasa Varma

AI & Machine Learning Engineer

GitHub

https://github.com/manasaavarmaa

LinkedIn

https://www.linkedin.com/in/smanasavarma/

Portfolio

https://manasaportfolio-six.vercel.app

---

If you found this project helpful, consider giving it a ⭐ on GitHub!
