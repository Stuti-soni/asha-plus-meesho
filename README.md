Here’s a detailed README for our project, including setup, environment variables, and how to run both the frontend and backend locally.
ASHA+ Meesho Health Assistant
A full-stack AI-powered health assistant for ASHA workers and rural communities, built with React (Vite), Firebase Functions, and Google Gemini AI.  
Provides health Q&A, document analysis, government scheme suggestions, and Hindi text-to-speech.
Features
-AI Health Assistant: Ask health or general questions in Hindi and get instant answers (text + voice).
-Medical Document Analysis: Upload prescriptions, lab reports, or medicine labels for instant analysis.
- Government Scheme Suggestions: Get personalized government scheme recommendations.
- Form Auto-fill: Automatically fill out health forms using AI.
- Secure & Scalable: Secrets are managed via environment variables and never committed to the repo.---
Prerequisites
-Node.js (v18+ recommended)
- npm (v9+ recommended)
- Firebase CLI (`npm install -g firebase-tools`)
- Google Cloud Service Account JSON (for TTS, in `functions/`)
- Gemini API Key (for AI)
- Firebase Project (for hosting and functions)
1. Clone the Repository
git clone https://github.com/Stuti-soni/asha-plus-meesho.git
cd asha-plus-meesho
2. Setup Environment Variables
Backend (`functions/.env`):
Create a file `functions/.env` with:
GEMINI_API_KEY=your_actual_gemini_api_key_here
Frontend (`frontend/.env`):
Create a file `frontend/.env` with:
VITE_FIREBASE_API_KEY=your_actual_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_actual_auth_domain
VITE_FIREBASE_PROJECT_ID=your_actual_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_actual_storage_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_actual_messaging_sender_id
VITE_FIREBASE_APP_ID=your_actual_app_id
Service Account JSON
Place your Google Cloud service account JSON (for TTS) in the `functions/` directory.  
Example: `functions/ai-health-assistant-7b5af-21dc9acf65a2.json`
3. Install Dependencies
Frontend
cd frontend
npm install
Backend
cd ../functions
npm install
4. Run Locally
Frontend (React)
cd frontend
npm run dev
Backend (Firebase Functions Emulator)
cd functions
npm run start
 This will start the Firebase Functions emulator (make sure your `.env` and service account JSON are present).
 5. Deploy to Firebase
Build frontend:
  cd frontend
  npm run build
-Deploy:
  cd ..
  firebase deploy
 6. Security
  Never commit your `.env` files or service account JSON.**  
  These are ignored by `.gitignore` and must be managed locally or in your deployment environment.
7. Project Links
-GitHub Repo: [https://github.com/Stuti-soni/asha-plus-meesho]
- Live App:(https://ai-health-assistant-7b5af.web.app/)
8. Contact:For questions , open an issue or contact [Stuti-soni on GitHub](https://github.com/Stuti-soni).

| Name                        | Version    | License    | Role/Usage                        | Source Link                                                                 |
|-----------------------------|------------|------------|------------------------------------|------------------------------------------------------------------------------|
| react                       | ^19.1.0    | MIT        | Main UI library (direct)           | https://github.com/facebook/react                                           |
| react-dom                   | ^19.1.0    | MIT        | DOM bindings for React (direct)    | https://github.com/facebook/react                                           |
| react-firebase-hooks        | ^5.1.1     | MIT        | React hooks for Firebase (direct)  | https://github.com/csfrequency/react-firebase-hooks                         |
| firebase                    | ^11.10.0   | Apache-2.0 | Firebase SDK (direct)              | https://github.com/firebase/firebase-js-sdk                                 |
| agora-rtc-sdk-ng            | ^4.23.4    | MIT        | Video call/RTC (direct)            | https://github.com/AgoraIO/AgoraRTC_NG                                      |
| html2canvas                 | ^1.4.1     | MIT        | HTML to canvas (direct)            | https://github.com/niklasvh/html2canvas                                     |
| pdfmake                     | ^0.2.20    | MIT        | PDF generation (direct)            | https://github.com/bpampuch/pdfmake                                         |
| vite                        | ^7.0.4     | MIT        | Frontend build tool (direct)       | https://github.com/vitejs/vite                                              |
| @vitejs/plugin-react        | ^4.6.0     | MIT        | Vite React plugin (direct)         | https://github.com/vitejs/vite-plugin-react                                 |
| eslint                      | ^9.30.1    | MIT        | Linting (direct)                   | https://github.com/eslint/eslint                                            |
| @eslint/js                  | ^9.30.1    | MIT        | ESLint config (direct)             | https://github.com/eslint/eslint                                            |
| eslint-plugin-react-hooks   | ^5.2.0     | MIT        | React hooks linting (direct)       | https://github.com/facebook/react                                           |
| eslint-plugin-react-refresh | ^0.4.20    | MIT        | React Fast Refresh linting         | https://github.com/vitejs/vite-plugin-react                                 |
| @types/react                | ^19.1.8    | MIT        | TypeScript types (direct)          | https://github.com/DefinitelyTyped/DefinitelyTyped                          |
| @types/react-dom            | ^19.1.6    | MIT        | TypeScript types (direct)          | https://github.com/DefinitelyTyped/DefinitelyTyped                          |
| globals                     | ^16.3.0    | MIT        | ESLint globals (direct)            | https://github.com/sindresorhus/globals                                     |
| firebase-admin              | ^12.6.0   | Apache-2.0 | Firebase Admin SDK (direct)        | https://github.com/firebase/firebase-admin-node                              |
| firebase-functions          | ^6.0.1    | Apache-2.0 | Firebase Cloud Functions SDK       | https://github.com/firebase/firebase-functions                               |
| @google-cloud/text-to-speech    | ^6.2.0    | Apache-2.0 | Google Cloud TTS API client        | https://github.com/googleapis/nodejs-text-to-speech                          |
| axios                           | ^1.10.0   | MIT        | HTTP client (direct)               | https://github.com/axios/axios                                               |
| firebase-functions-test         | ^3.1.0    | Apache-2.0 | Firebase Functions testing (dev)   | https://github.com/firebase/firebase-functions-test                          |
| @google-cloud/text-to-speech      | ^6.2.0      | Apache-2.0   | Google Cloud Text-to-Speech API client for Node.js      | npm                    |
| axios                             | ^1.10.0     | MIT          | Promise-based HTTP client for API calls                 | npm                    |
| firebase-admin                    | ^12.6.0     | Apache-2.0   | Firebase Admin SDK for backend (Firestore, Auth)        | npm                    |
| firebase-functions                | ^6.0.1      | Apache-2.0   | Firebase Cloud Functions SDK                            | npm                    |
| firebase/app, firestore, auth     | (frontend)  | Apache-2.0   | Firebase JS SDK for frontend (Firestore, Auth)          | npm                    |
| Hugging Face Inference API        | N/A (API)   | Varies (API) | OCR: Text extraction from images                        | Hugging Face API       |
| Google Gemini API                 | N/A (API)   | Google Terms | Generative AI for health advice, analysis, etc.         | Gemini API             |
| Google Translate (unofficial)     | N/A (API)   | Google Terms | Hindi translation (frontend)                            | Google Translate API   |
| Jitsi Meet (iframe API)           | N/A (API)   | Apache-2.0   | Video consultations (frontend)                          | Jitsi Meet             |


