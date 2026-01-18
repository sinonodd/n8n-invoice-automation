# n8n-invoice-automation

# Invoice Automation Workflow

## 🎯 Purpose
Automatically processes new orders:
- Sends invoices by email
- Saves data to Google Sheets  
- Notifies sales team on Slack for high-value orders (>$500)

## 🚀 Quick Setup

### 1. Import Workflow
Import `invoice_email_slack_authomation.json` into n8n

### 2. Set Up Credentials
**Three credentials needed:**

| Credential | Purpose |
|------------|---------|
| Google Sheets OAuth2 | Save order data to spreadsheet |
| Gmail OAuth2 | Send invoice emails |
| Slack OAuth2 | Send team alerts |

### 3. Activate Workflow
Turn on the workflow in n8n

### 4. Test It
Send this to webhook: `POST /new-order`

```json
{
  "order_id": "123",
  "customer_name": "Test Customer",
  "customer_email": "test@example.com",
  "total_amount": 700,
  "items": "Item A, Item B"
}
