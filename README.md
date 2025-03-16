# TRON Enhanced

A cutting-edge note-taking application with AI-powered features.

## Features

- Create and manage notes with rich text formatting
- Voice transcription using Deepgram
- AI-powered search and note connections
- Built with React, TypeScript, and modern web technologies

## Setup

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory with the following variables:
   ```
   OPENAI_API_KEY=your_openai_api_key
   DEEPGRAM_API_KEY=your_deepgram_api_key
   PROXY_URL=http://localhost:3002/api/deepgram (optional, defaults to this value)
   PROXY_PORT=3002 (optional, defaults to 3002)
   ```

4. Start the application:
   ```bash
   npm run start:all
   ```
   
   This will start both the proxy server and the development server concurrently.

   Alternatively, you can start each server individually:
   ```bash
   # In one terminal
   npm run proxy
   
   # In another terminal
   npm run dev
   ```

## Browser CORS Issues

Deepgram does not allow direct API calls from browsers due to CORS restrictions. The application uses a proxy server to handle these API calls. Make sure to start the proxy server before using voice transcription features.

## Environment Variables

- `OPENAI_API_KEY`: Required for AI features like processing voice commands and generating connections between notes
- `DEEPGRAM_API_KEY`: Required for voice transcription (used by the proxy server)
- `PROXY_URL`: URL to the proxy server (defaults to http://localhost:3002/api/deepgram)
- `PROXY_PORT`: Port for the proxy server (defaults to 3002)

## Automated Development

You can use the automation script to set up the project:

```bash
node automate.js
```

## Voice Transcription

The application uses Deepgram for high-quality voice transcription. Voice commands can be used to create notes, search for content, and perform various actions within the application.

## Testing

Run tests with:

```bash
npm test
```

## License

MIT 