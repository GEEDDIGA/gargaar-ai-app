# gargaar-ai-app

A Technology AI Tutor application powered by Google Gemini API and Firebase Authentication.

## Features
- AI-powered technology lesson generation
- Firebase Authentication (Email/Password and Google)
- Modern, responsive UI with Tailwind CSS
- Focuses on practical, market-oriented technology education

## Configuration

This app requires API credentials to run. Copy `.env.example` to create your configuration:

1. **Firebase Configuration** - Get from Firebase Console:
   - apiKey
   - authDomain
   - projectId
   - storageBucket
   - messagingSenderId
   - appId

2. **Google Gemini API Key** - Get from Google AI Studio:
   - GEMINI_API_KEY

## Deployment to Vercel

### Prerequisites
- GitHub account with this repository
- Vercel account (free tier available at https://vercel.com)
- Firebase project with credentials
- Google Gemini API key

### Steps to Deploy:

1. **Import to Vercel:**
   - Go to https://vercel.com/new
   - Click "Import Git Repository"
   - Select this repository (GEEDDIGA/gargaar-ai-app)
   - Click "Import"

2. **Configure Environment Variables:**
   - In the Vercel import screen, scroll to "Environment Variables"
   - Add each variable from your `.env` file:
     - `FIREBASE_API_KEY`
     - `FIREBASE_AUTH_DOMAIN`
     - `FIREBASE_PROJECT_ID`
     - `FIREBASE_STORAGE_BUCKET`
     - `FIREBASE_MESSAGING_SENDER_ID`
     - `FIREBASE_APP_ID`
     - `GEMINI_API_KEY`

3. **Deploy:**
   - Click "Deploy"
   - Wait for build to complete (usually 1-2 minutes)
   - Your app will be live at `https://your-project-name.vercel.app`

4. **Update Firebase Configuration:**
   - Go to Firebase Console > Authentication > Settings
   - Add your Vercel domain to "Authorized domains"
   - Format: `your-project-name.vercel.app`

### Continuous Deployment

Vercel automatically redeploys when you push to the `main` branch:
- Any commit to main triggers a new deployment
- Preview deployments are created for pull requests
- View deployment history in Vercel dashboard

## Local Development

1. Clone the repository
2. Copy `.env.example` to `.env` and fill in your credentials
3. Open `index.html` in a web browser
4. Or use a local server: `python -m http.server 8000`

## Technologies Used

- **Frontend:** HTML5, Tailwind CSS, Vanilla JavaScript
- **AI:** Google Gemini API (gemini-1.5-flash-002)
- **Authentication:** Firebase Auth
- **Deployment:** Vercel (or any static hosting)

## Security Notes

- Never commit `.env` file with actual credentials
- Use environment variables for all sensitive data
- Firebase security rules should be configured properly
- API keys should have appropriate restrictions in Google Cloud Console

## License

MIT License - feel free to use for educational purposes.
