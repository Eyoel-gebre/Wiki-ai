# Wiki AI Backend Server

This handles LLM requests and image fetching, acting as a proxy between the frontend and various external APIs.

## Hosting Setup

1. Install dependencies:
```bash
npm install
```

2. Create a `.env` file in `server/src` with the following variables:
```
GOOGLE_IMAGES_API_KEY=your_api_key
GOOGLE_IMAGES_CX=your_api_key
GEMINI_API_KEY=your_api_key
GROQ_API_KEY=your_api_key
OPENAI_CHAT_API_KEY=your_api_key
```

## Running the Server

Start the development server with:
```bash
npm run dev
```

Or start in production mode:
```bash
npm start
```

The server will be available at `http://localhost:1212`.

## API Endpoints

- POST `/api/generate-topic-overview` - Generate topic overview
- POST `/api/generate-detailed-content` - Generate detailed content for a topic
- POST `/api/fetch-images` - Fetch images using Google Custom Search API
- POST `/api/generate-subject-summary` - Generate introductory summary for a subject
- POST `/api/answer-question` - Answer questions about a topic
- POST `/api/expand-sentence` - Expand a sentence into a detailed paragraph