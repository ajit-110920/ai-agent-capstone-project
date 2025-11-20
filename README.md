# **AI Study Assistant Agent**

**Google AI Agents Intensive — Capstone Project**
**Track:** Concierge Agents
**Author:** Ajit Bhandekar

## 🚀 Overview

The AI Study Assistant Agent is a multi-agent learning system designed to help students learn faster and more effectively. It automatically finds resources, generates study plans, answers questions, evaluates responses, and stores long-term memory.

This project is built entirely inside a Kaggle Notebook with a clean architecture and no external API keys.

## 🧠 Motivation

- Learning is often inefficient because students must:

- Search scattered resources

- Plan their sessions manually

- Validate answers

- Keep track of what they learned

- Switch between many tools

This agent automates all of that, providing a unified personal learning environment.

## 🏗 Architecture

The system uses a multi-agent architecture:

### 1. ResourceFinder Agent

- Finds learning materials using a safe, offline-friendly search tool.

### 2. StudyPlanner Agent

- Generates structured study plans with multiple sessions.

### 3. QnA Agent

- Answers conceptual, mathematical, and coding questions using:

- SearchTool

- CalculatorTool

- CodeExecTool

### 4. Evaluator Agent

- Scores answers using a heuristic scoring model.

### 5. Coordinator Agent

- Orchestrates the full learning pipeline.

### Session Memory

Stores:

- Interactions

- Plans

- Knowledge

- Evaluations

## 🔧 Tools
### SearchTool

- Fast local knowledge base

### Optional Wikipedia fallback (3-second timeout)

- Always returns results

### CalculatorTool

- Safe arithmetic evaluator

- Extracts math expressions from natural language

### CodeExecTool

- Restricted sandbox execution (safe on Kaggle)

## 📦 Folder / Code Structure

Inside the Kaggle Notebook:

Cell 1: Title  
Cell 2: Imports  
Cell 3: Config  
Cell 4–8: Tools & Memory  
Cell 9: Agents  
Cell 10: Build agent system  
Cell 11: Demo  
Cell 12: Memory summary  

## ▶️ Usage

Example run:

demo = agents["coordinator"].run_full(
    "logistic regression",
    ["What is logistic regression?", "Calculate 1+2*3"]
)
demo

**Output includes:**

- Study plan

- Resource list

- Q&A

- Evaluation

- Memory summary

## 🏆 Capstone Requirements Satisfied

✔ Multi-Agent System

✔ Tools (Search, Calculator, Code Execution)

✔ Memory & State

✔ Orchestration

✔ Context Engineering

✔ Clean Architecture

✔ Runs fully inside Kaggle

✔ No deployment required

## 📈 Future Enhancements

- LLM-based evaluator

- Quiz generator

- Notes summarizer

- Adaptive study plans

- Vector memory
