# Project 3 — Senior Mortgage Underwriting System

Senior Mortgage Underwriting System is a multi-agent AI workflow built as part of the Johns Hopkins Agentic AI Certificate Program.

## Overview

This project builds a fully automated mortgage underwriting system using LangGraph, OpenAI, ChromaDB, and RAG. Six specialized AI agents collaborate through a supervised workflow to analyze loan applications and generate audit-ready underwriting decisions, replicating the process a real mortgage underwriting team would follow.

## What It Does

- Sanitizes borrower PII before passing data to any LLM
- Retrieves relevant lending policies dynamically using RAG
- Analyzes credit history, payment behavior, and derogatory items
- Verifies employment stability and calculates DTI ratio
- Confirms down payment adequacy and flags large deposits
- Assesses property value and calculates LTV ratio
- Cross-validates all analyses for consistency and policy compliance
- Generates a final risk score and audit-ready credit memo
- Routes high-risk and denied applications to human review

## Agents Built

- Credit Analyst
- Income Analyst
- Asset Analyst
- Collateral Analyst
- Critic Agent
- Decision Agent

## Test Cases

- Sarah Johnson — Credit score 760, DTI 30.4% — APPROVED
- Michael Chen — Credit
