# AI-Powered Real Estate Lead Generation & Qualification Automation

## Project Overview

An end-to-end lead generation and qualification automation built with **n8n, Google Gemini AI, Google Sheets, and Gmail**.

The system captures property enquiries through an online form, uses AI to analyse and qualify each lead, assigns a score, categorises prospects based on their purchasing intent, stores the results in Google Sheets, and sends personalised follow-up emails automatically.

The goal is to reduce manual lead processing, improve response times, and help real estate agencies prioritise promising prospects.

## Problem Statement

Real estate agencies often receive property enquiries through different channels. Manually reviewing each enquiry, identifying serious prospects, recording customer information, and following up can be time-consuming.

This automation addresses these challenges by creating a centralised process for lead capture, AI-powered qualification, data storage, and customer follow-up.

## Workflow Architecture

1. **Lead Capture – n8n Form Trigger**
   - Captures prospective customers' information through a property enquiry form.
   - Collects name, email, phone number, preferred location, budget, and property interest.

2. **Data Preparation – Edit Fields**
   - Organises and standardises submitted information.
   - Prepares the lead data for AI analysis.

3. **AI Lead Qualification – Google Gemini**
   - Analyses each property enquiry.
   - Identifies buying, selling, or renting intent.
   - Evaluates budget, location, urgency, and level of interest.
   - Assigns a lead score from 0–100.
   - Categorises leads as Hot, Warm, or Cold.
   - Generates a recommended action and personalised follow-up message.

4. **AI Response Processing – JavaScript**
   - Extracts the structured JSON response from Gemini.
   - Combines the AI assessment with the original lead information.

5. **Lead Storage – Google Sheets**
   - Automatically records lead information and qualification results.
   - Maintains a centralised lead database.

6. **Automated Follow-up – Gmail**
   - Sends personalised follow-up emails using the AI-generated message.

## Lead Scoring and Classification

| Score | Category | Meaning |
|---|---|---|
| 70–100 | Hot | Strong buying or selling interest |
| 40–69 | Warm | Moderate interest or developing requirements |
| 0–39 | Cold | Low or unclear immediate interest |

The AI considers the information submitted by each prospect when generating its assessment.

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation and orchestration |
| Google Gemini API | AI-powered lead qualification |
| JavaScript | Response parsing and data transformation |
| Google Sheets | Lead database and record management |
| Gmail | Automated personalised email follow-up |
| n8n Forms | Lead capture interface |

## Example Lead Assessment

A prospective customer submits an enquiry with the following details:

- Property Interest: Buying a property
- Preferred Location: Karu
- Budget: ₦50 million–₦100 million

Example AI assessment:

- Lead Score: 85/100
- Category: Hot
- Intent: Buying a property
- Urgency: High
- Recommended Action: Contact the prospect to understand their requirements and discuss suitable properties.

## Business Benefits

- Reduces manual lead processing.
- Automates lead qualification and segmentation.
- Improves lead response times.
- Centralises customer information.
- Enables more personalised communication.
- Helps real estate teams prioritise promising enquiries.

## Setup Requirements

- n8n installation (self-hosted or cloud).
- Google Gemini API key.
- Google Sheets account.
- Gmail account and configured n8n credentials.

## How to Run

1. Import the n8n workflow into your n8n instance.
2. Configure the Google Gemini API credentials.
3. Connect your Google Sheets account and select your lead spreadsheet.
4. Configure Gmail authentication.
5. Test the workflow using the property enquiry form.
6. Activate the workflow and use its production form URL.

## Project Status

**Development:** Built and tested through AI qualification and Google Sheets lead storage. Gmail delivery and full production execution should be verified before deployment.

## Future Improvements

- Add duplicate lead detection.
- Introduce automated lead routing based on qualification category.
- Add WhatsApp notifications for high-priority leads.
- Integrate property listing databases to recommend verified properties.
- Implement error handling and execution monitoring.
- Add lead analytics and reporting dashboards.

## Author

**Esther Happiness Ogbudu**

Junior AI Automation Specialist

Portfolio: https://esther-happiness-ogbudu.netlify.app

