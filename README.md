# Abhishek Mishra Portfolio

Personal portfolio built with HTML, CSS, and JavaScript, with an Express server and optional Gemini AI portfolio assistant.

## Run locally

1. Install Node.js.
2. Run `npm install`.
3. Run `npm start` and open `http://localhost:3000` to view the site and use its built-in portfolio Q&A.
4. Copy `.env.example` to `.env` and set two different passwords: `RESUME_PASSWORD` and `CONTACT_ADMIN_PASSWORD`.
5. Set `CONTACT_REPLY_EMAIL` and/or `CONTACT_REPLY_PHONE` to the details you are willing to share after approving a request.
6. Optionally set `GEMINI_API_KEY` for open-ended AI replies. Built-in answers work without it.

Never commit `.env`, passwords, API keys, or `.contact-requests.json`. Visitors can request contact through the form; requests are stored privately, and your details appear in a reply draft only after you approve a request in `/manage-requests.html`. You still review and send the email yourself.

The resume PDF is served only after the resume password is accepted. Unlock access expires after 30 minutes in that browser. Use the portfolio through `npm start`; direct `file://` previews cannot access the protected server routes.

Contact requests are saved to `.contact-requests.json` by default. On a hosting service whose filesystem resets during deploys, configure `CONTACT_REQUESTS_PATH` to a private persistent disk path or requests may be lost.

The protected resume route and contact inbox need the Express server and environment variables; a static-only host such as GitHub Pages cannot run these server checks. Deploy to a Node.js host and set the environment variables there. Keep the GitHub repository private: it contains the resume and certificate PDFs, which can be downloaded directly by anyone who can access the repository, regardless of the website password. Do not make this repository public unless those files are removed and the exposed Git history is cleaned first.

## Portfolio content

- `index.html` contains the portfolio page and chat interface.
- `server.js` contains the optional AI chat API.
- `images/photo.png` is the profile image.
- `images/certificates/` contains web-sized certificate previews.
- `certificates/` contains the original certificate PDFs linked from each preview.
- `resume/Abhishek_Mishra_Resume.pdf` is available only through the password-protected resume route.
- `manage-requests.html` is the password-protected owner inbox for reviewing requests.

Certificate previews are in `images/certificates/`; their source PDFs are in `certificates/`.
