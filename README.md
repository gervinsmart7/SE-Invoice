# SE Invoice — installable offline web app

A lightweight Progressive Web App (PWA) for creating invoices and receipts. It stores records in this browser on this device, supports backup/restore, uses an A4 print stylesheet, and can be added to a phone's home screen.

accessible via https://seinvoicereceipt.netlify.app/
## Run locally on a computer
PWAs require `localhost` or HTTPS for service workers and installation. From this folder, run a local web server, for example:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080` in a browser on that computer. For installation on an Android phone, publish this folder to an HTTPS static host (or use a local-network server and a trusted HTTPS setup); open the HTTPS URL in Chrome and choose **Install app** or **Add to Home screen**. Simply opening `index.html` as a file will let you test much of the app, but offline PWA installation will not work in file mode.

## Features

- Create and save invoices and receipts
- Automatic document numbers
- Multiple saved company profiles with company logo, contact details, services, payment details and authorised signature
- Choose the issuing company separately for each invoice or receipt; saved company details remain until changed
- Documents store a snapshot of the issuing company details so older documents retain their original company profile
- Local document history and search
- A4 print layout (use Print / Save PDF, then choose A4 in the print dialog)
- Share document summary through the system share menu when available
- Local JSON backup and restore
- Service-worker caching for offline use after the app has been opened online once

## Important notes

- Data is stored in this browser's local storage. Export backups regularly. Clearing browser data can remove records.
- For reliable installation/offline use, serve over HTTPS (or localhost during development).
- Sharing currently shares document details as text. To share a PDF, use **Print / Save PDF**, save the PDF, then share that PDF from your phone's Files app.
- This is a starter app; validate calculations and test on your target device before relying on it for business records or tax compliance.
