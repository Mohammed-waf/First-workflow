# n8n Form Submission Workflow

This repository contains an **n8n workflow** that collects user data via a form, processes it automatically, and stores it in Google Sheets based on age conditions.

## 📋 Overview

The workflow uses an **On Form Submission** trigger to collect user information and applies simple logic to classify and store the data.

## 🧩 Workflow Steps

1. **Form Submission**
   - Users submit a form containing:
     - Full name
     - Age
     - Phone number
     - Email
   - A submission timestamp is automatically generated.

2. **Date Formatting**
   - The submission date is converted from ISO format  
     (`2026-02-01T13:29:44.211+01:00`)
   - Into a clean format:  
     `YYYY/MM/DD`

3. **Age Classification**
   - If age **> 18** → data is sent to the *greater than 18* sheet
   - If age **≤ 18** → data is sent to the *less than 18* sheet

4. **Google Sheets Storage**
   - Each submission is appended as a new row
   - Stored fields:
     - Name
     - Phone number
     - Email
     - Date of submission

## 📊 Google Sheets Structure

- One spreadsheet
- Two sheets:
  - `greater than 18`
  - `less than 18`

## 🚀 How to Use

1. Download or clone this repository.
2. Import the workflow JSON file into **n8n**.
3. Configure your **Google Sheets credentials**.
4. Adjust sheet names or form fields if needed.
5. Activate the workflow.
6. Share the form link and start collecting data.

## 🎯 Use Cases

- Registration forms
- Age-based surveys
- Event sign-ups
- Learning automation with n8n

## 🛠 Requirements

- n8n (self-hosted or cloud)
- Google account with access to Google Sheets

---

**Author:** Mohamed  
**Tool:** n8n
