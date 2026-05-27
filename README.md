# 🏋️ Gym Subscription Management System

A workflow automation project built with **n8n** and **Airtable** to manage gym memberships, automate user registration, and handle expiry notifications.

##  Project Structure
This repository contains the following workflows:

- **Project 1: User Registration** (`gym-registration-workflow.json`)
  - Validates new member data.
  - Checks for duplicates in Airtable.
  - Creates member records automatically.
  - Sends welcome emails to new members.
  - Notifies gym management of new sign-ups.

##  Tech Stack
- **Automation:** n8n
- **Database:** Airtable
- **Email:** Gmail / SMTP
- **Testing:** Postman

##  How to Import to n8n
1. Open your n8n dashboard.
2. Go to **Workflows** -> **Add Workflow**.
3. Open the **Menu (⋮)** -> **Import from File**.
4. Select `gym-registration-workflow.json`.
5. Configure your **Airtable** and **Gmail** credentials.
6. Add your **Airtable Base ID** to the workflow variables.
7. Activate the workflow!

##  Webhook Usage
To register a user, send a POST request to the webhook URL:
```json
POST /webhook/gym-register
{
  "full_name": "John Doe",
  "email": "john@example.com",
  "phone": "+123456789",
  "plan_type": "monthly",
  "amount_paid": 5000
} 
