# CivicStack Frontend

React Native frontend for CivicStack - Civic Complaint Management System

## Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- npm or Yarn
- Expo CLI (`npm install -g expo-cli`)
- Expo Go app on your mobile device (for testing)

### Environment Variables

Create a `.env` file in the project root:

```
EXPO_PUBLIC_SUPABASE_URL=your_supabase_url
EXPO_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
EXPO_PUBLIC_API_URL=http://your_backend_ip:3001
```

Note: For local development with a physical device, use your computer's local IP address (e.g., 192.168.x.x) instead of localhost.

### Installation

Install dependencies:

```bash
npm install
# or
yarn install
```

### Running the App

Start the development server:

```bash
npm start
# or
yarn start
```

Then:
- Scan the QR code with Expo Go (Android) or Camera app (iOS)
- Press 'a' for Android emulator
- Press 'i' for iOS simulator

## Deployment

### Deploying to Vercel

1. Push your code to GitHub
2. Create a new project in Vercel linked to your GitHub repo
3. Add environment variables in Vercel project settings
4. Deploy the project

#### Environment Variables for Deployment

Make sure to add these environment variables in your Vercel project settings:

- `EXPO_PUBLIC_SUPABASE_URL`
- `EXPO_PUBLIC_SUPABASE_ANON_KEY`
- `EXPO_PUBLIC_API_URL` (pointing to your deployed backend)

### Building for Production

To create a production build:

```bash
expo build:android
# or
expo build:ios
```

## Security Notes

- Never commit `.env` files to version control
- Use environment variables for all sensitive information
- For production deployment, use secure environment variable storage (e.g., Vercel environment variables)
