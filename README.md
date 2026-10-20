# Abhishek Mishra Portfolio

Personal portfolio built with HTML, CSS, and JavaScript, with an optional Express and Gemini AI portfolio assistant.

## Run locally

1. Install Node.js.
2. Run `npm install`.
3. Run `npm start` and open `http://localhost:3000` to view the site and use its built-in portfolio Q&A.
4. To enable open-ended Gemini replies, create `.env` from `.env.example` and set your own `GEMINI_API_KEY` there.

The built-in answers for common portfolio questions work without an API key. Open-ended Gemini answers require the Node server and a Gemini API key. Never commit `.env` or API keys.

## Portfolio content

- `index.html` contains the portfolio page and chat interface.
- `server.js` contains the optional AI chat API.
- `images/photo.png` is the profile image.
- `images/certificates/` contains web-sized certificate previews.
- `certificates/` contains the original certificate PDFs linked from each preview.
- `resume/Abhishek_Mishra_Resume.pdf` is the downloadable resume.

Certificate images can be added to `images/certificates/` when available and linked from the Certifications section.
