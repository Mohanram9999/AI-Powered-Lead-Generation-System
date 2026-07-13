# AI-Powered Lead Generation System using Salesforce Flow

<p align="center">
  <b>APSHE Short-Term Virtual Internship</b><br>
  Salesforce Certified Administrator with Agentforce Specialization
</p>



Project Overview
This project implements an AI-augmented Lead Management System on the Salesforce platform that automates lead capture, validation, enrichment, and qualification using Record-Triggered Flows, Validation Rules, and Agentforce/Prompt Builder generative AI. Instead of relying on manual data entry and static lead review, the system automatically summarizes incoming leads, flags high-quality prospects, and routes them to the right sales rep — reducing lead response time and improving conversion tracking from day one.
Internship Details
Detail
Description
Program
APSHE Short-Term Virtual Internship
Track
Salesforce Certified Administrator with Agentforce Specialization
Duration
Short-Term (Virtual)
Mode
Remote / Trailhead-based hands-on labs
Focus Areas
Salesforce Admin, Flow Automation, Agentforce, Prompt Builder
Intern
K. Mohan Ram
Problem Statement
Sales teams using CRM systems often struggle with:
Manually reviewing every incoming lead, causing delayed follow-up
Inconsistent or incomplete lead data entering the system
No automated way to gauge lead quality before a rep spends time on it
Lack of a quick, digestible summary of a lead's context for the assigned rep
Human error in field validation (missing phone/email, wrong lead source, etc.)
This leads to slow response times, wasted effort on low-quality leads, and lost revenue opportunities.
Proposed Solution
An automation-first Lead Management pipeline built entirely on native Salesforce tools:
Record-Triggered Flows fire the moment a Lead is created or updated, running validation and enrichment logic instantly
Validation Rules enforce mandatory, clean data before a Lead is allowed to save
Agentforce + Prompt Builder generate a natural-language AI Summary of each Lead (intent, urgency, fit) directly on the record
Role & Profile-based access ensures the right users see and act on the right leads
Lightning App + Reports give managers a real-time view of lead volume, quality, and conversion trends
Objectives
Automate lead intake and eliminate manual data validation
Use generative AI to produce an instant, human-readable summary of every lead
Reduce average lead response time through automatic routing/alerts
Maintain clean, standardized lead data using validation rules
Provide sales managers with real-time visibility via reports and dashboards
Demonstrate a scalable, low-code AI-powered CRM automation pattern
Key Features
🔁 Record-Triggered Flow on the Lead object for create/update events
✅ Validation Rules to enforce required fields (email format, phone number, lead source)
🤖 Agentforce-powered AI Summary field auto-generated via Prompt Builder
🧩 Custom Fields to capture AI-derived insights (Lead Quality, Summary, Next Best Action)
👥 Profile & Role hierarchy for Sales Rep vs Sales Manager visibility
📊 Reports & Dashboards for lead volume, source, and conversion tracking
⚡ Lightning App as a unified workspace for the sales team
System Architecture
Text
Workflow
A new Lead is created (manually, via Web-to-Lead, or import).
Validation Rules check that mandatory fields (Email, Phone, Company, Lead Source) are correctly filled before the record saves.
A Record-Triggered Flow fires on create/update and calls a Prompt Builder prompt template.
Agentforce generates a concise AI Summary of the lead — covering intent, urgency, and fit — and writes it into the custom AI Summary field along with a derived Lead Quality value.
Based on the Lead Quality outcome, the Flow updates ownership/assignment and can trigger a notification to the relevant Sales Rep.
Sales Reps and Managers view leads through a dedicated Lightning App, with Reports and Dashboards surfacing volume, source performance, and conversion metrics.
Technologies Used
Salesforce Platform (Lightning Experience)
Salesforce Flow Builder
Agentforce
Prompt Builder
Salesforce Trailhead (learning/sandbox environment)
Salesforce Reports & Dashboards
Salesforce Components Used
Lead Object
Custom Fields
Record-Triggered Flow
Validation Rules
Profiles
Roles
Users
Prompt Builder
Agentforce
AI Summary Field
Lightning App
Reports
AI & Agentforce Integration
The core AI capability is delivered through Prompt Builder, using a custom prompt template grounded in Lead record fields (Name, Company, Lead Source, Description, Industry). The template instructs the model to:
Summarize the lead's context in 2–3 sentences
Infer an approximate urgency/quality signal from available data
Suggest a recommended next action for the sales rep
This output is written back to the Lead record via a custom AI Summary text field, invoked from within the Record-Triggered Flow using an Agentforce (Prompt) action. This keeps the AI layer fully native to Salesforce — no external API keys or middleware required.
Business Benefits
⏱️ Faster lead response time through automatic summarization and routing
🎯 Sales reps focus on high-quality leads first, guided by AI-derived scoring
🧹 Cleaner CRM data thanks to enforced validation rules
📈 Better visibility for managers via reports/dashboards
💰 Zero additional licensing cost — built entirely with native Salesforce/Agentforce tools already available in the org
Implementation Steps
Create custom fields on the Lead object: AI_Summary__c, Lead_Quality__c, Next_Best_Action__c
Define Validation Rules for mandatory field enforcement (email format, phone presence, lead source required)
Build a Prompt Builder template referencing relevant Lead fields
Create a Record-Triggered Flow (Before Save / After Save) on the Lead object
Add an Agentforce Prompt action inside the Flow to call the prompt template and capture its output
Map the AI output to the custom fields via Flow assignment elements
Configure Roles and Profiles to control visibility (Sales Rep vs Sales Manager)
Build a Lightning App combining Lead list views, the AI Summary field, and key reports
Create Reports and Dashboards for lead volume, source breakdown, and quality distribution
Testing
✅ Validated Flow trigger behavior on Lead creation and field updates
✅ Verified Validation Rules correctly block incomplete/invalid lead submissions
✅ Tested Prompt Builder output across leads with varying data completeness
✅ Confirmed AI Summary and Lead Quality fields populate correctly and consistently
✅ Verified role/profile-based visibility restrictions using multiple test user personas
✅ Checked report and dashboard accuracy against sample lead data sets
Results
Leads are automatically enriched with an AI-generated summary within seconds of creation
Data quality improved due to enforced validation at point of entry
Sales managers gained a real-time dashboard view of lead health and volume
Demonstrated a working, low-code, AI-augmented CRM automation pipeline suitable for small-to-mid sales teams
Screenshots
(Add screenshots of Flow Builder canvas, Prompt Builder template, Lead record with AI Summary field, Lightning App, and Dashboard here — place image files in the screenshots/ folder and reference them below.)
Markdown
Project Demonstration
Demo Video
Click below 👇
https://drive.google.com/file/d/1U25804Kk4feYUzGfOyd0uMNtEuriGvhy/view?usp=drivesdk
Project Documentation
Software Requirements Specification is available in the docs folder.
Learning Outcomes
Salesforce Administration
Salesforce CRM
Salesforce Flow Builder
Agentforce
Prompt Builder
CRM Automation
Business Process Automation
Workflow Design
Validation Rules
Profiles & Roles
AI-powered Business Solutions
Challenges Faced
Designing record-triggered flows that fire reliably without recursion issues
Configuring validation rules without blocking legitimate edge-case leads
Testing automation across multiple Lead data scenarios (complete vs. partial data)
Understanding and correctly applying Salesforce's security model (Profiles, Roles, sharing rules)
Integrating Agentforce/Prompt Builder output cleanly into Flow field assignments
Future Enhancements
AI-based Lead Scoring using historical conversion data
Email Automation for follow-up sequences
WhatsApp Notifications for instant rep alerts
Analytics Dashboard with deeper conversion funnel tracking
External CRM Integration (e.g., syncing with third-party marketing tools)
Predictive Lead Conversion modeling using Einstein/Agentforce
Internship Highlights
This project was successfully completed during the APSHE Short-Term Virtual Internship under the Salesforce Certified Administrator with Agentforce Specialization program. The internship provided hands-on experience in building real-world CRM automation solutions using Salesforce technologies.
Repository Structure
Text
Author
K. Mohan Ram
Artificial Intelligence and Machine Learning Student
Ideal Institute of Technology, Kakinada
Acknowledgements
APSHE
Salesforce
Salesforce Trailhead
Ideal Institute of Technology, Kakinada
Connect With Me
LinkedIn: (Add your LinkedIn profile)
GitHub: (Add your GitHub profile)

```text
AI-Powered-Lead-Generation-System/
├── README.md
├── docs/
├── screenshots/

```

## Author

**K. Mohan Ram**

Artificial Intelligence and Machine Learning Student

Ideal Institute of Technology, Kakinada

## Acknowledgements

- APSHE
- Salesforce
- Salesforce Trailhead
- Ideal Institute of Technology, Kakinada.
