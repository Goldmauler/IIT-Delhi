# CivicStack Backend

Backend API for CivicStack - Civic Complaint Management System

## Setup Instructions

### Prerequisites
- Node.js (v14 or higher)
- npm

### Environment Variables

This project uses environment variables for configuration. Create a `.env` file in the project root based on the `.env.example` template:

```bash
cp .env.example .env
```

Then edit the `.env` file and fill in your specific credentials and configuration values:

- **Server Configuration**
  - `PORT`: The port the server will listen on (default: 3001)
  
- **Google Cloud Credentials**
  - `GOOGLE_PROJECT_ID`: Your Google Cloud project ID
  - `GOOGLE_CLIENT_EMAIL`: Service account email
  - `GOOGLE_PRIVATE_KEY`: Service account private key (with newlines preserved as `\n`)
  
- **Roboflow API Settings**
  - `ROBOFLOW_API_KEY`: Your Roboflow API key
  - `ROBOFLOW_WORKSPACE`: Workspace name
  - `ROBOFLOW_WORKFLOW`: Workflow ID
  
- **Cloudinary Configuration**
  - `CLOUDINARY_CLOUD_NAME`: Your Cloudinary cloud name
  - `CLOUDINARY_API_KEY`: Your Cloudinary API key
  - `CLOUDINARY_API_SECRET`: Your Cloudinary API secret
  
- **Wit.ai Configuration**
  - `WIT_AI_TOKEN`: Your Wit.ai token

### Installation

Install dependencies:

```bash
npm install
```

### Running the Server

Start the server:

```bash
npm start
```

For development with auto-restart:

```bash
npm run dev
```

## API Endpoints

- `GET /health`: Health check endpoint
- `POST /api/auth/login`: User login
- `POST /api/auth/signup`: User registration
- `GET /api/complaints/all`: Get all complaints
- `POST /api/complaints/create`: Create a new complaint
- `POST /api/transcribe/audio`: Transcribe audio to text

## Security Notes

- Never commit `.env` files to version control
- Use environment variables for all sensitive information
- For production deployment, use secure environment variable storage (e.g., Vercel/Netlify environment variables, Docker secrets, etc.)
