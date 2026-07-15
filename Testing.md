# 🧪 Testing

This folder contains the testing documentation for the **AI-Powered Lead Generation System using Salesforce Flow & Agentforce**.

## Testing Objective

The purpose of testing is to verify that all Salesforce automation, validation rules, AI integration, and security configurations work as expected.

---

# QA Strategy

| Test Type | Description |
|-----------|-------------|
| Unit Testing | Verified Lead creation and automation using different input values. |
| Validation Testing | Confirmed that Validation Rules prevent invalid Lead records from being saved. |
| AI Testing | Verified AI-generated Lead Summary using Prompt Builder and Agentforce. |
| Security Testing | Tested Profiles, Roles, and user permissions for different users. |

---

# Test Case Log

| # | Test Case | Expected Result | Actual Result | Status |
|---|-----------|-----------------|---------------|--------|
| 1 | Create Lead with valid email | Lead is created successfully | Lead created successfully without errors | ✅ Pass |
| 2 | Create Lead with personal email | Validation Rule blocks record | Validation message displayed and record not saved | ✅ Pass |
| 3 | Lead scoring (High Engagement) | Lead Score updated correctly | Score generated as expected | ✅ Pass |
| 4 | Lead scoring (Low Engagement) | Lower Lead Score generated | Score generated correctly | ✅ Pass |
| 5 | AI Summary Generation | AI Summary field populated | AI Summary generated successfully | ✅ Pass |
| 6 | Sales Representative Access | User can access only assigned Leads | Access restrictions worked correctly | ✅ Pass |
| 7 | Sales Manager Access | User can access all Leads | Role hierarchy worked correctly | ✅ Pass |

---

# Test Environment

- Salesforce Developer Edition
- Lightning Experience
- Salesforce Flow Builder
- Prompt Builder
- Agentforce
- Google Chrome Browser

---

# Test Summary

| Metric | Result |
|--------|--------|
| Total Test Cases | 7 |
| Passed | 7 |
| Failed | 0 |
| Success Rate | 100% |

---

# Evidence

Screenshots related to testing are available in the `../screenshots/` folder.

The screenshots include:

- Successful Lead Creation
- Validation Rule Error
- Record-Triggered Flow
- AI Summary Generation
- Reports
- User Access Verification

---

# Conclusion

All major functionalities of the system were successfully tested. The application met the expected functional requirements, and the Salesforce automation, AI integration, validation rules, and security configurations operated as intended.
