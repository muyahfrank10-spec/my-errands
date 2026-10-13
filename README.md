# My Errands — working prototype

## Included
- Responsive customer home screen and service categories
- Booking request form with Kenya's 47 counties
- Booking lookup by phone number (on the same browser/device)
- Admin dashboard with status changes, assistant assignment, service quote and customer update fields
- CSV export
- Browser-local demo storage

## Run locally
1. Extract the ZIP.
2. Open `index.html` in Chrome, Edge, Firefox or another modern browser.
3. Use the Customer home tab to create a request.
4. Open Admin dashboard and use demo passcode `2468`.
5. Update a booking and press **Save updates**.
6. Use My bookings and enter the same phone number to see its status.

You can also serve it with a local web server:
- Python: `python -m http.server 8000`
- Then open `http://localhost:8000`

## Important prototype limitations
- Data is saved in the current browser's local storage only. It does not sync across devices or users.
- The admin passcode is a demo-only client-side gate, not secure authentication.
- No real M-Pesa payments, SMS, email, maps, or live tracking are connected.
- Booking requests are not automatically sent to the owner.
- The prototype uses customer-provided phone numbers and locations; add a privacy notice and secure data handling before a public launch.

## Suggested production deployment
1. Put the files in a GitHub repository.
2. Deploy the static interface on Netlify, Vercel or Cloudflare Pages.
3. Create a Supabase project (or another backend) for authentication and shared bookings.
4. Move booking creation, status changes and admin permissions into server-side rules. Never rely on a browser-only PIN.
5. Integrate Safaricom Daraja STK Push only after business and callback setup. Verify payment status on the server; never ask for a customer's M-Pesa PIN.
6. Add official support phone/WhatsApp details, privacy policy, terms, assistant verification and service-area/availability rules.
7. Test with fake bookings and sandbox payments before launch.

## Before real customers use it
- Secure owner and assistant accounts, with role-based access.
- Restrict each customer to their own bookings.
- Protect customer contact details and precise locations.
- Define cancellation/refund policy, service fees and assistant safety procedures.
- Confirm applicable Kenyan business, data-protection and payment requirements.
