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
  
<img width="1379" height="180" alt="image" src="https://github.com/user-attachments/assets/69147a8a-4e69-4ab4-b984-541de32b5b65" />

