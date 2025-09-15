# n8n-daily-maintenance-report
Daily Maintenance Report workflow (n8n)

This n8n workflow automates the creation and distribution of a **daily maintenance report** from a database.
It queries the database for work orders, formats the results into an HTML report, and sends it via email to the maintenance team.

---

## Features
- Pulls **daily or weekly due work orders** from the database
- Generates a **formatted HTML report**
- Sends the report automatically via **SMTP email**
- Optional logging for record-keeping
- Fully compatible with **n8n Cloud** and **self-hosted n8n**

---

## Prerequisites

1. **n8n instance** (Cloud or self-hosted)
2. **Database** (MSSQL, Postgres, MySQL, etc.) with maintenance data
3. **SMTP server credentials** for sending emails

---

## Setup Instructions

1. **Import Workflow**
   - **n8n Cloud:** Use **Import from Clipboard** and paste the workflow JSON.
   - **Self-hosted:** Use **Import from File**.

2. **Configure Credentials**
   - **Database Credential:** Create a new credential in n8n for your database.
   - **SMTP Credential:** Create a new credential for sending emails.

3. **Test Workflow**
   - Click **Execute Workflow** to ensure the report generates correctly.

4. **Activate Workflow**
   - Toggle **Active** to let it run automatically on the schedule defined in the workflow (e.g., 07:00 daily).

---

## Workflow Diagram

![Workflow Diagram] (Daily_Maintenance_Report_Workflow.png)

---

## Notes

- **Credentials are not included** in this repository for security reasons.
- Update SQL queries in the **Database Query** node as per your database structure.
- You can extend the workflow to send reports to **Slack, Teams, or Telegram**

---

## License
This repository is shared for educational and internal workflow process. Modify as needed for your environment
