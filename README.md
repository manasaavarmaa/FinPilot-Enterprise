# 💰 FinPilot Enterprise — AI Financial Operations Platform

An AI-powered financial operations platform that automates invoice auditing by extracting invoice information, validating financial data, comparing invoice totals against expected purchase order values, applying configurable business rules, and intelligently deciding whether an invoice can be processed automatically or requires manual review.

Instead of finance teams manually opening invoices, checking totals, verifying purchase orders, creating audit records, and raising support tickets, FinPilot Enterprise performs the complete workflow through an AI-driven LangGraph pipeline and presents the results through an interactive Streamlit dashboard.

The project demonstrates how modern AI Agents can be combined with deterministic business logic to build production-inspired financial automation systems.

---

# 📚 Table of Contents

- Overview
- Features
- System Architecture
- LangGraph Workflow
- Finance Agent Pipeline
- Project Structure
- How It Works — Step by Step
- Dashboard
- Database
- Analytics
- API Endpoints
- Installation
- Running the Project
- Folder Description
- Tech Stack
- Future Improvements

---

# 📖 Overview

Traditional invoice auditing is a repetitive manual process.

A finance executive typically performs the following tasks:

- Open the invoice
- Read vendor information
- Verify invoice totals
- Compare against purchase order values
- Calculate financial differences
- Decide whether the invoice is acceptable
- Raise a support ticket if required
- Store the audit result
- Update dashboards or reports

This process becomes time-consuming when hundreds or thousands of invoices are received every day.

FinPilot Enterprise automates this complete workflow.

When an invoice is uploaded, the system automatically:

- Extracts invoice information using OCR
- Converts unstructured data into structured financial information
- Retrieves expected purchase order values
- Compares invoice totals against expected amounts
- Applies configurable business rules
- Makes an intelligent business decision
- Generates audit records
- Creates support tickets when necessary
- Updates live dashboards and analytics

The objective is not simply document extraction.

The objective is to automate financial decision making while maintaining transparency, traceability, and auditability.

---

# ✨ Features

## 🤖 AI Financial Validation

Instead of only extracting invoice data, the system performs financial validation.

It compares

- Invoice Total
- Expected Purchase Order Amount
- Financial Difference

before making any decision.

---

## 🧠 LangGraph Workflow

Every uploaded invoice passes through a LangGraph workflow.

Each node performs one responsibility.

```
Upload Invoice

↓

OCR

↓

Extract Information

↓

Finance Agent

↓

Business Rules

↓

Action Agent

↓

Database

↓

Dashboard
```

Unlike traditional sequential Python scripts, every processing step remains isolated and reusable.

---

## 📄 Intelligent OCR

Invoices can be uploaded as

- PDF
- PNG
- JPG

OCR automatically extracts

- Vendor Name
- Invoice Number
- Invoice Date
- Invoice Total

The extracted information becomes structured input for the Finance Agent.

---

## 💰 Finance Agent

The Finance Agent performs financial reasoning.

Instead of trusting OCR output directly, it

- Retrieves expected purchase order values
- Compares invoice totals
- Calculates differences
- Applies financial validation
- Produces structured decisions

The Finance Agent never creates tickets or stores data.

Its only responsibility is financial validation.

---

## ⚖️ Business Rules

AI reasoning is combined with deterministic business rules.

Example

```
Difference <= Threshold

↓

AUTO CORRECT

Difference > Threshold

↓

RAISE TICKET
```

This hybrid approach provides predictable business behaviour while still benefiting from AI reasoning.

---

## 🎫 Automatic Ticket Generation

Whenever invoice discrepancies exceed acceptable thresholds,

FinPilot automatically

- Creates an audit record
- Generates a finance ticket
- Stores the result
- Displays the ticket inside the dashboard

No manual intervention is required.

---

## 📊 Interactive Dashboard

The Streamlit dashboard provides

- KPI Cards
- Invoice Trends
- Vendor Statistics
- Decision Distribution
- Audit History
- Recent Invoices
- Ticket Management

Every visualization is generated directly from the database.

No static data is used.

---

## 📈 Real-Time Analytics

The analytics engine automatically calculates

- Total Invoices
- Total Audited Amount
- Vendor Count
- Ticket Count
- Average Invoice Value
- Highest Invoice
- Decision Distribution
- Daily Invoice Trends

Every dashboard refresh reflects the latest database state.

---

## 🗄️ Persistent Storage

SQLite stores

- Invoices
- Audit Results
- Tickets
- Vendors
- Analytics

SQLite acts as the single source of truth for the entire application.

---

## 🚀 Modular Architecture

The project follows Separation of Concerns.

Each module owns one responsibility.

- UI
- API
- Workflow
- Agents
- Tools
- Database
- Utilities

Every component can be modified independently without affecting the rest of the application.
