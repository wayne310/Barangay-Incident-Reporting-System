# Barangay Incident Reporting and Management System

A frontend prototype for the proposed Barangay Incident Reporting and Management System.

## Files

- `index.html` - main HTML entry point
- `assets/style.css` - complete CSS styling
- `assets/app.js` - complete JavaScript application logic
- `API-INTEGRATION-NOTES.md` - guide for connecting PHP + MySQL later

## Run immediately

### Option 1: Open directly
Double-click `index.html`.

### Option 2: Use a local server (recommended)
If PHP is installed:

```bash
php -S localhost:8000
```

Then open:

`http://localhost:8000`

If you have VS Code, you can also use a Live Server extension.

## Demo accounts

Resident:
- Email: `resident@example.com`
- Password: `123456`

Admin:
- Email: `admin@barangay.gov`
- Password: `admin123`

## What already works

- Login/logout
- Resident dashboard
- Incident reporting
- Mobile camera/photo upload
- Photo preview
- Browser geolocation
- Incident categories
- Server-side AI incident priority recommendation (OpenAI Responses API)
- Resident report tracking
- Admin dashboard
- Search and filters
- Human verification of AI priority
- Official priority/status changes
- Incident history/audit trail
- Responsive mobile layout
- localStorage UI/session cache

## Important

Incident reports are submitted to the PHP/MySQL API. PHP sends only the incident category and description to OpenAI for a suggested priority; report photos, location, and reporter details are not sent. The AI result remains a recommendation, and an authorized barangay official must verify the official priority.

Copy `.env.example` to `.env` and fill in your local database and service settings. PHP loads `.env` on the server; values already configured in the MAMP/Apache environment take precedence. Never put secret keys in frontend code or commit `.env` to the project.
