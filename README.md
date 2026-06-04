# Enterprise AI Assistant Requirements

## Project Overview

Create a reusable AI assistant platform that can answer questions about company tools, projects, documentation, and onboarding processes.

The system should support multiple AI agents that can be added over time without major code changes.

Initial supported platforms:

* SharePoint
* Jira
* Databricks

Future platforms:

* GitHub
* Confluence
* ServiceNow
* Power BI
* Tableau

---

# Business Goals

1. Reduce onboarding time for new hires.
2. Allow employees to self-serve answers instead of contacting support.
3. Provide project visibility through Jira and Databricks.
4. Create a reusable framework for future enterprise AI assistants.

---

# Users

## New Hires

Need help with:

* Jira usage
* Databricks usage
* Internal processes
* Onboarding documentation

## Project Managers

Need help with:

* Project status
* Sprint progress
* Blockers
* Completion percentages

## Engineers and Analysts

Need help with:

* Databricks projects
* SQL logic
* Data lineage
* Notebook documentation

---

# SharePoint Agent

## Purpose

Answer questions using documents stored in SharePoint.

## Capabilities

* Search PDF documents
* Search Word documents
* Search PowerPoint files
* Search onboarding guides
* Return source links

## Example Questions

How do I create a Jira ticket?

How do I request access to Databricks?

Where is the onboarding checklist?

---

# Databricks Agent

## Purpose

Answer questions about Databricks projects and data pipelines.

## Data Sources

* Notebooks
* SQL files
* Project documentation
* Job metadata
* Pipeline metadata

## Capabilities

* Explain project purpose
* Summarize SQL
* Identify source tables
* Identify target tables
* Explain pipeline flow
* Summarize notebook contents

## Example Questions

What does the Customer Churn project do?

Which notebook updates the customer_gold table?

What tables are used in Project X?

---

# Jira Agent

## Purpose

Provide project and sprint insights.

## Data Sources

* Jira Projects
* Epics
* Stories
* Tasks
* Sprints

## Capabilities

* Project status
* Sprint status
* Completion percentage
* Blocker identification
* Progress summaries

## Example Questions

What percentage of Project Alpha is complete?

What is currently blocking Project Alpha?

What stories are still in progress?

---

# Non-Functional Requirements

## Authentication

* Microsoft Entra ID
* Role-based access control
* Respect source system permissions

## Security

* Users can only access data they are authorized to view
* Log all AI interactions
* No storage of sensitive credentials

## Performance

* Response time under 10 seconds
* Support at least 100 concurrent users

## Monitoring

* Usage tracking
* Error logging
* Query history

---

# Technical Architecture

## AI Layer

* OpenAI GPT
* Retrieval-Augmented Generation (RAG)

## Vector Database

Preferred:

* Databricks Vector Search

Alternative:

* Azure AI Search

## Connectors

Reusable connector architecture:

* SharePoint Connector
* Jira Connector
* Databricks Connector

Future connectors should follow the same interface.

---

# MVP Scope

Phase 1:

* SharePoint Agent
* Document ingestion
* Vector search
* Chat interface

Phase 2:

* Jira Agent
* Project status questions

Phase 3:

* Databricks Agent
* SQL and project understanding

---

# Success Metrics

* Reduce onboarding questions by 50%
* Reduce project status requests to project managers
* Increase documentation usage
* Positive user satisfaction feedback
