# WIP LLM Churn Advisor: Interactive Customer Intervention Assistant

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## Overview

This project demonstrates an advanced system for customer churn prediction and intervention. It goes beyond simple prediction scores by integrating **Explainable AI (XAI)** using SHAP to understand *why* a customer might churn and leverages **Large Language Models (LLMs) within an agentic framework (LangGraph)** to interpret these reasons and suggest personalized, actionable intervention strategies.

The goal is to provide customer support or marketing teams with not just a churn risk score, but context and concrete recommendations tailored to individual customer situations, based on the Telco Customer Churn dataset.

**Key Features:**
*   **ML Churn Prediction:** Uses XGBoost trained on the Telco dataset.
*   **XAI Explanations:** Provides SHAP values to identify key churn drivers for individual customers.
*   **LLM Interpretation:** A LangGraph agent translates technical scores and SHAP values into natural language summaries.
*   **Personalized Interventions:** A second LangGraph agent uses the interpretation and a custom intervention playbook to suggest actionable retention strategies.
*   **API Service:** FastAPI exposes endpoints for prediction (`/predict`) and explanation (`/explain`).
*   **MLOps Integration:** Includes Dockerization, CI/CD pipeline examples using Google Cloud Build, and deployment configurations for Google Cloud Run and Vertex AI Training.

## Problem Statement

Identifying customers likely to churn is valuable, but basic prediction scores lack context. Support/marketing teams need to understand the underlying *drivers* of churn for specific customers and receive guidance on the *most effective interventions* to retain them, considering their unique circumstances. This system aims to bridge that gap by providing explainable predictions and actionable, LLM-generated advice.
