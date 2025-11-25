# Hospital Management System

Flask web application for managing hospital patients and doctors with comprehensive tabbed registration forms, stored in Excel workbooks (`patients.xlsx` and `doctors.xlsx`).

## Requirements

- Python 3.10+
- `pip install -r requirements.txt`

## Running the web app

```bash
python app.py
```

Visit `http://127.0.0.1:5000/` to access the Patient module, or `http://127.0.0.1:5000/doctors` for the Doctor module.

## Patient Module

1. **Tabbed registration** – Personal Info, Contact, Identification, Emergency Contacts, Medical Background, Treatment, Insurance/Billing, and Consent. Mandatory fields are validated server-side, hospital IDs are auto-generated (MRN). Use the top-right search to find patients by name/MRN/phone, preview them in-place (read-only), and jump into edit mode with one click.
   - When a date of birth is provided, the age field auto-calculates both on the page and when persisting to Excel.
2. **View module** – Search and preview patient records in read-only mode.
3. **Edit module** – Edit form reuses the same tabs with existing data prefilled; MRN remains read-only.

## Doctor Module

1. **Tabbed registration** – Personal Details, Professional/Qualification, Employment/Hospital, Consultation & Service, Availability/Scheduling, Banking & Payroll, and Login/Access. Includes fields for qualifications, specializations, OPD/IPD fees, surgery details, availability schedules, and access credentials.
   - Age auto-calculates from date of birth.
   - Search by name, registration number, or contact.
2. **View module** – Search and preview doctor records in read-only mode.
3. **Edit module** – Edit form with all doctor details across tabs.

All changes sync to Excel workbooks, which auto-create with the latest headers on first run. Data persists between sessions.
