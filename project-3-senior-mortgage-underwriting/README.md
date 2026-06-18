<div align="center">

# 🏦 Project 3 — Senior Mortgage Underwriting System

[![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)](https://github.com)
[![Type](https://img.shields.io/badge/Type-Multi_Agent_System-orange?style=for-the-badge)](https://github.com)
[![RAG](https://img.shields.io/badge/RAG-Enabled-412991?style=for-the-badge)](https://github.com)
[![Accuracy](https://img.shields.io/badge/Test_Accuracy-100%25-brightgreen?style=for-the-badge)](https://github.com)
[![Program](https://img.shields.io/badge/Johns_Hopkins-Agentic_AI_Certificate-002D72?style=for-the-badge)](https://online.lifelonglearning.jhu.edu/jhu-online-certificate-program-agentic-ai)

Senior Mortgage Underwriting System is a multi-agent AI workflow built as part of the Johns Hopkins University Agentic AI Certificate Program.

</div>

---

## 📋 Overview

This project builds a fully automated mortgage underwriting system using **LangGraph, OpenAI, ChromaDB, and RAG**. Six specialized AI agents collaborate through a supervised workflow to analyze loan applications and generate audit-ready underwriting decisions, replicating the process a real mortgage underwriting team would follow.

---

## 🚀 What It Does

🔒 **Sanitizes borrower PII before passing data to any LLM**
Names, SSNs, addresses, and phone numbers are masked before any data reaches the language model.

📚 **Retrieves relevant lending policies dynamically using RAG**
ChromaDB stores the full underwriting policy document and returns only the most relevant sections for each agent query.

💳 **Analyzes credit history, payment behavior, and derogatory items**
Reviews bankruptcies, foreclosures, late payments, and collections against policy minimums.

💵 **Verifies employment stability and calculates DTI ratio**
Confirms income sources, employment history, and debt-to-income ratios using deterministic Python tools.

💰 **Confirms down payment adequacy and flags large deposits**
Verifies liquid assets cover closing costs and reserves while identifying undocumented deposits.

🏠 **Assesses property value and calculates LTV ratio**
Evaluates appraisal results, property condition, and loan-to-value ratio against collateral standards.

🔎 **Cross-validates all analyses for consistency and policy compliance**
A dedicated Critic Agent reviews all specialist outputs for contradictions and gaps before a decision is made.

⚖️ **Generates a final risk score and audit-ready credit memo**
The Decision Agent synthesizes all findings into a 0-100 risk score and a comprehensive credit memo.

👤 **Routes high-risk and denied applications to human review**
Applications scoring above 65 or flagged for bias automatically trigger a mandatory senior underwriter review.

---

## 🤖 Agents Built

<div align="center">

| Agent | Role | Tools Used |
|-------|------|------------|
| 💳 Credit Analyst | Evaluates credit score and payment history | check_credit_score_policy |
| 💵 Income Analyst | Verifies employment and calculates DTI | calculate_dti_ratio, calculate_housing_expense_ratio |
| 💰 Asset Analyst | Confirms down payment and flags deposits | calculate_reserves, check_large_deposits |
| 🏠 Collateral Analyst | Assesses property value and LTV | calculate_ltv_ratio |
| 🔎 Critic Agent | Cross-validates all analyses | — |
| ⚖️ Decision Agent | Generates final risk score and credit memo | — |

</div>

---

## 🧪 Test Cases

<div align="center">

| Applicant | Credit Score | DTI | Expected | AI Decision | Human Decision |
|-----------|-------------|-----|----------|-------------|----------------|
| 👤 Sarah Johnson | 760 ✅ | 30.4% ✅ | APPROVED | ✅ APPROVED | ✅ APPROVED |
| 👤 Michael Chen | 680 ✅ | 42% ⚠️ | CONDITIONAL | ✅ CONDITIONAL | ✅ CONDITIONAL |
| 👤 Robert Martinez | 595 ❌ | 50% ❌ | DENIED | ✅ DENIED | ✅ DENIED |

**100% accuracy across all three test cases**

</div>

---

## 🛠️ Technologies Used

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-00B4D8?style=for-the-badge&logo=chainlink&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B35?style=for-the-badge&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-00B4D8?style=for-the-badge&logoColor=white)
![PyPDF](https://img.shields.io/badge/PyPDF-red?style=for-the-badge&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

</div>

---

## 🎯 Skills Demonstrated

<div align="center">

![Multi Agent](https://img.shields.io/badge/Multi_Agent_System_Design-orange?style=for-the-badge)
![LangGraph](https://img.shields.io/badge/LangGraph_State_Management-00B4D8?style=for-the-badge)
![RAG](https://img.shields.io/badge/Retrieval_Augmented_Generation-412991?style=for-the-badge)
![Vector DB](https://img.shields.io/badge/Vector_Database_Retrieval-FF6B35?style=for-the-badge)
![PII](https://img.shields.io/badge/PII_Sanitization-brightgreen?style=for-the-badge)
![Tools](https://img.shields.io/badge/Deterministic_Tool_Calculations-blue?style=for-the-badge)
![HITL](https://img.shields.io/badge/Human_In_The_Loop_Design-purple?style=for-the-badge)
![Compliance](https://img.shields.io/badge/Financial_Compliance_ECOA-red?style=for-the-badge)

</div>

---

## 📁 Deliverable Included

| File | Description |
|------|-------------|
| 📓 `Learners_Notebook__4_.ipynb` | Completed project notebook from the Johns Hopkins Agentic AI Certificate Program |

---

<div align="center">

[![Johns Hopkins](https://img.shields.io/badge/Johns_Hopkins_University-Agentic_AI_Certificate-002D72?style=for-the-badge)](https://online.lifelonglearning.jhu.edu/jhu-online-certificate-program-agentic-ai)
[![By](https://img.shields.io/badge/Built_by-Daniel_Cohen_Collazo-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniel-cohen-collazo)

</div>
