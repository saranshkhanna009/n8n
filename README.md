n8n AI Automation Workflows

This repository contains two production-ready n8n automation workflows leveraging modern Large Language Model (LLM) providers, vector databases for Retrieval-Augmented Generation (RAG), and cloud services integration.

🛠️ Project 1: RAG-Powered AI Knowledge Base Agent
<img width="1593" height="702" alt="Screenshot 2026-10-31 164126" src="https://github.com/user-attachments/assets/8655c230-0365-4d27-a4af-e0d37131ac39" />

📌 Overview

An end-to-end Retrieval-Augmented Generation (RAG) pipeline and autonomous AI Agent workflow built in n8n. The system ingests local documents, embeds them using OpenAI Embeddings, stores vector representations in Pinecone, and equips an interactive AI Agent with vector search capabilities to query context-aware responses.

🖼️ Workflow Architecture

⚙️ Workflow Breakdown

Trigger (Execute workflow): Initiates the ingestion and retrieval processes.

Document Ingestion & Indexing:

Read/Write Files from Disk: Reads target documents from local storage.

Embeddings OpenAI: Generates high-dimensional vector embeddings for text chunks.

Default Data Loader: Prepares document objects for database insertion.

Pinecone Vector Store: Indexes and stores vector embeddings for fast similarity search.

Data Extraction & Agent Querying:

Extract from File: Parses text files to feed structured queries to the AI Agent.

OpenAI Chat Model: Serves as the core reasoning LLM engine.

AI Agent & Pinecone Vector Store Tool: Connects the OpenAI Chat Model with Pinecone to enable contextual information retrieval before response generation.

🧰 Tech Stack & Integrations

Automation Platform: n8n

LLM Engine: OpenAI Chat Model

Embeddings: OpenAI Embeddings

Vector Database: Pinecone

I/O Handling: File System Reader, Text Extractor

🛠️ Project 2: Google Gemini Automated Email Drafting Agent
<img width="1672" height="652" alt="Screenshot 2026-10-31 164203" src="https://github.com/user-attachments/assets/ddcb7cb4-8dca-4654-975e-3424d3ab0cd4" />

📌 Overview

An automated lead/data processing workflow that extracts spreadsheet rows, processes data via a Google Gemini-powered AI Agent, and automatically drafts personalized email responses directly inside Gmail.

🖼️ Workflow Architecture

⚙️ Workflow Breakdown

Trigger (Execute workflow): Starts the automated batch processing pipeline.

Data Acquisition:

Get row(s) in sheet: Fetches customer, lead, or operational data rows from a designated Google Sheet.

Limit: Controls batch execution sizes to optimize API rate limits.

AI Content Generation:

Google Gemini Chat Model: Powers the central AI Agent with conversational intelligence and contextual understanding.

AI Agent: Processes row inputs, formulates customized email copy, and structures output parameters.

Action / Delivery:

Create a Draft (Gmail): Uses output from the AI Agent to automatically generate structured email drafts in Gmail for human review prior to sending.

🧰 Tech Stack & Integrations

Automation Platform: n8n

LLM Engine: Google Gemini Chat Model

Data Source: Google Sheets Integration

Email Platform: Gmail Integration

🚀 Setup & Execution Guide

Prerequisites

Self-hosted or Cloud n8n instance.

API Credentials Required:

OpenAI API Key 

Pinecone API Key & Index Details 

Google OAuth2 Credentials 

Google Gemini API Key 
