# 🚀 AI Attendance Monitoring & Warning System

An AI-powered attendance automation workflow built using **n8n**, **OpenAI**, **Google Calendar**, **Gmail**, and **Webhooks**. The system automatically processes employee attendance Excel files, detects late arrivals, generates personalized warning emails with escalating tone, and schedules meetings for repeated violations.

---

## 📌 Overview

This project automates the complete employee attendance monitoring process, eliminating manual HR effort. It analyzes attendance records, identifies late arrivals, tracks strike counts, generates AI-based warning emails, and schedules meetings for employees with repeated violations.

---

## ✨ Features

- ✅ Webhook-based Excel file upload
- ✅ Automatic attendance data extraction
- ✅ Employee master data parsing
- ✅ Date and time normalization
- ✅ Missing punch handling
- ✅ Late arrival detection
- ✅ Monthly late count calculation
- ✅ AI-generated personalized emails
- ✅ Different email tone for 1st, 2nd, and 3rd strikes
- ✅ Automatic Google Calendar meeting creation on 3rd strike
- ✅ Calendar link attached inside email
- ✅ Fully automated workflow with zero manual intervention

---

## 🛠 Tech Stack

| Technology | Purpose |
|------------|---------|
| n8n | Workflow Automation |
| OpenAI | AI Email Generation |
| Gmail API | Sending Emails |
| Google Calendar API | Meeting Scheduling |
| Webhooks | Trigger Workflow |
| JavaScript | Data Transformation |
| Excel (.xlsx) | Attendance Source |

---

# ⚙️ Workflow Architecture

```text
Excel Upload
      ↓
Webhook Trigger
      ↓
Extract Employee Data
      ↓
Extract Attendance Records
      ↓
Date Formatting
      ↓
Split In-Time / Out-Time
      ↓
Late Detection Logic
      ↓
Monthly Late Count Calculation
      ↓
1st / 2nd / 3rd Strike Classification
      ↓
OpenAI Email Generation
      ↓
Clean Subject & Body
      ↓
Google Calendar Event Creation
      ↓
Attach Meeting Link
      ↓
Send Email via Gmail
```

---

## 🤖 AI Email Escalation Logic

### 🟢 First Strike

- Friendly reminder email
- Professional and supportive tone
- Encourages punctuality

---

### 🟡 Second Strike

- Warning email
- Stronger language
- Highlights impact on team productivity

---

### 🔴 Third Strike

- Final warning email
- Escalated tone
- Automatic 5 PM meeting scheduled
- Google Calendar invitation link included

---

## 📂 Folder Structure

```text
AI-Attendance-Monitoring-and-Warning-System
│
├── workflow/
│     attendance-workflow.json
│
├── docs/
│     Architecture_Document.pdf
│
├── sample-data/
│     attendance.xlsx
│
├── images/
│     workflow.png
│
└── README.md
```

---

## 📊 Attendance Processing

The system performs:

- Employee master data extraction
- Attendance data extraction
- Date conversion from Excel serial numbers
- In-Time and Out-Time splitting
- Check-In and Check-Out generation
- Monthly late count calculation
- Strike tracking

---

## ⚠️ Edge Case Handling

### Missing OUT Punch

#### Detection

- Empty Out Time field

#### Fallback Behavior

- Marks record as "Missing OUT Punch"
- Skips work-hour calculation
- Adds status flag for reporting

#### Alerts Generated

- Employee notification
- Optional manager escalation
- Calendar follow-up meeting

---

## 📈 Scalability Plan

Designed to support:

- 500+ employees
- Multiple office locations
- Batch processing
- Parallel execution
- Location-specific attendance rules
- Future database integration

---

## 📋 Example Output

```json
{
  "Employee ID": "GD00164",
  "Name": "Ashfa Islam",
  "Date": "02 Feb 2026",
  "Check-In": "12:11",
  "Check-Out": "19:11",
  "Late Flag": "Yes",
  "Current Monthly Late Count": 3
}
```

---

## ✉️ AI Generated Email

### Subject

```text
Final Warning Regarding Attendance Concerns
```

### Body

```text
Dear Employee,

This email serves as a final warning regarding repeated late arrivals.

A meeting has been scheduled for 5:00 PM today to discuss this matter further.

Best Regards,
HR Department
```

---

## 📅 Calendar Automation

For employees reaching the third strike:

- Google Calendar event is automatically created.
- Meeting scheduled for 5:00 PM.
- Calendar invitation link is embedded inside the email.
- Helps HR conduct follow-up discussions efficiently.

---

## 🚀 Business Impact

- Reduced manual HR effort by **80%**
- Automated attendance analysis for **500+ employees**
- Eliminated manual email drafting
- Improved compliance and punctuality tracking
- Standardized employee communication
- Increased operational efficiency

---

## 💡 Key Capabilities

- Event-Driven Architecture
- AI Integration
- Prompt Engineering
- Workflow Automation
- API Integration
- Data Transformation
- Error Handling
- Scalable System Design
- HR Process Automation

---

## 🏆 Resume Highlights

- Built an AI-powered attendance monitoring system using n8n, OpenAI, Gmail, and Google Calendar to automate late-arrival detection and employee communication, reducing manual HR effort by 80%.
- Designed a webhook-driven pipeline that processes Excel attendance files, transforms raw records into structured datasets, and calculates monthly late counts automatically.
- Integrated OpenAI to generate personalized warning emails with escalating tone based on strike count and automated Google Calendar meeting scheduling for repeated violations.
- Developed a scalable workflow capable of handling 500+ employees across multiple locations with robust date normalization, missing punch handling, and notification automation.

---

## 🔮 Future Enhancements

- Database integration (PostgreSQL/MySQL)
- Employee dashboard using Power BI or Looker Studio
- Slack and Microsoft Teams notifications
- Multi-location attendance policies
- Advanced analytics and reporting
- Leave management integration

---

## 🏷 GitHub Topics

```text
n8n
openai
workflow-automation
ai-agent
gmail-api
google-calendar
webhook
attendance-management
employee-management
javascript
excel-processing
prompt-engineering
hr-automation
```

---

## 👨‍💻 Author

**Praveen Kumar**

AI Automation | Data Analytics | n8n | OpenAI | Workflow Automation

---
⭐ If you found this project useful, consider giving it a star!
