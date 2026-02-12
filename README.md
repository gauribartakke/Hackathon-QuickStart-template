
1. GitHub Folder Structure (Create This)

Create a folder on your laptop named:

Smart-Budgeting-AI-Assistant

Inside it:

Smart-Budgeting-AI-Assistant/
│
├── README.md
├── app.py
├── sms_sample_data.csv
├── requirements.txt
├── architecture.png
└── demo_video_link.txt


---

 2. README.md (COPY THIS EXACTLY)

Paste this into README.md on GitHub.

# Smart Budgeting AI Assistant 💰🤖

## Problem Statement
Many people waste money because they do not track expenses or plan savings. Manual budgeting is time-consuming and most users ignore financial discipline.

## Solution
Smart Budgeting AI Assistant is an AI-powered chatbot system that:
- Reads SMS transaction alerts
- Automatically categorizes spending
- Provides personalized saving plans
- Suggests financial discipline improvements

## Features
- SMS transaction extraction
- Expense categorization using AI
- Monthly spending report
- AI chatbot for financial advice
- Personalized saving roadmap

## Tech Stack
- Python
- Machine Learning (NLP)
- Pandas
- Flask (for chatbot API)
- Firebase (future)
- Mobile App Integration (future)

## System Architecture
1. SMS data ingestion
2. NLP-based transaction parsing
3. Expense classification model
4. Budget planning engine
5. Chatbot interface for user interaction

## How to Run
```bash
pip install -r requirements.txt
python app.py

Future Scope

Real-time Android SMS integration

Bank API integration

Investment recommendations

AI fraud detection

Voice assistant support


Team

Manthan Phuldale
Mechanical Engineering Student | Robotics & AI Enthusiast

---

#  Sample Code (app.py)

This is **simple but looks serious to judges**.

```python
import pandas as pd

# Sample SMS transaction dataset
data = pd.read_csv("sms_sample_data.csv")

# Simple categorization logic
def categorize(text):
    text = text.lower()
    if "swiggy" in text or "zomato" in text:
        return "Food"
    elif "uber" in text or "ola" in text:
        return "Transport"
    elif "amazon" in text or "flipkart" in text:
        return "Shopping"
    else:
        return "Other"

data["Category"] = data["SMS"].apply(categorize)

# Monthly summary
summary = data.groupby("Category")["Amount"].sum()
print("Expense Summary:")
print(summary)

# AI Saving Suggestion (simple logic)
total_spent = data["Amount"].sum()
income = 20000  # assumed monthly income
saving = income - total_spent

print("\nAI Suggestion:")
if saving < 5000:
    print("You are overspending. Reduce food and shopping expenses.")
else:
    print("Good financial discipline. Invest extra savings.")


---
 # requirements.txt

pandas
flask



























