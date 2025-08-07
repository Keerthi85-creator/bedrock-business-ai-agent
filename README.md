# bedrock-business-ai-agent

# 🤖 Cloud-powered AI Business Assistant using Amazon Bedrock & Lambda

This project showcases an end-to-end **AI Agent** using **Amazon Bedrock**, **Lambda**, and **Manus AI-style action groups** to compute daily revenue from retail sales inputs.

## 📌 Project Use Case

The AI agent assists small business owners by calculating total revenue based on sales inputs(daily bases) — e.g., “I sold 50 books at ₹200 and 100 pens at ₹50”.

## 🏗️ Architecture Overview

- **Amazon Bedrock**: Hosts the AI agent using a foundation model
- **Action Group**: Maps natural prompts to structured inputs
- **AWS Lambda**: Executes revenue calculation logic
- **IAM Roles**: Provides permissions for Bedrock ↔ Lambda integration



## ⚙️ Setup Guide

1. **Request Bedrock Model Access** from AWS Console
2. **Create AI Agent**:
   - Add agent instructions
   - Create an Action Group named `bussiness-assistant-action_group`
   - Define parameters: `product1_name`, `product1_price`, etc.
3. **Write Lambda Function** (see `/lambda/lambda_function.py`)
4. **Attach Lambda to Action Group**
5. **Test Agent** with prompts like:
   > “I sold 100 apples at ₹10 each and 200 oranges at ₹15 each”
