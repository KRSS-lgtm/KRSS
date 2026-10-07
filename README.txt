KRSS SECURE WEBSITE

Admin login: open /admin after starting the Node server.
The owner password supplied by the owner is stored only as a one-way scrypt hash in .env.

Run:
1. Install Node.js 18+.
2. In this folder run: node server.js
3. Open: http://localhost:3000
4. Admin: http://localhost:3000/admin

For production: use HTTPS/reverse proxy, a persistent database, backups, antivirus/file scanning, and change the admin password/hash.
Private applicant uploads are stored under private/uploads and are not publicly served.


OWNER LOGIN
The /admin login screen now visibly asks for Owner Name and Password. Authorized owner names: Amit Tiwari and Sonali Passawed. Both use the configured ADMIN_PASSWORD_HASH.

CHATWORKS PRIVATE MESSAGING
- Open http://localhost:3000/chatworks
- Create a Chatworks account or log in.
- Search registered users by name or username.
- Select a user to start a one-to-one private conversation.
- The server returns messages only when the authenticated user is one of the two participants.
- Passwords are stored as scrypt hashes; private messages are stored server-side, not in browser localStorage.


ATTENDANCE MODULES
- /owner/amit — dedicated Amit Tiwari owner login page.
- /owner/sonali — dedicated Sonali Passawed owner login page.
- /owner-attendance — protected Owner Entry & Exit dashboard. A logged-in owner can record only their own entry/exit.
- /guard-attendance — protected Guard Attendance dashboard. Add guards and mark Present/Absent; records are stored server-side.

ADVANCED UPDATE
- Added Admin 4 login. Admin 4 initial password is 1234; change ADMIN4_PASSWORD_HASH before production.
- Guard Attendance now includes Payment status, payment amount, payment date, payment remarks, and a Payment Received action.
- Payment records are protected behind admin authentication.
