<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally and deploy to Render.com.

View your app in AI Studio: https://ai.studio/apps/drive/1jst3cjx3xunJavctRmHHgwFs1qfDfADZ

## Run Locally

**Prerequisites:** Node.js 18+

1. Install dependencies:
   ```bash
   npm install
   ```
2. Copy `.env.example` to `.env.local` and set your Gemini API key:
   ```bash
   cp .env.example .env.local
   ```
   Then edit `.env.local` and add your `GEMINI_API_KEY`

3. Run the app:
   ```bash
   npm run dev
   ```

## Deploy to Render.com

### Prerequisites:
- GitHub account with this repository
- Render.com account (https://render.com)
- Gemini API key

### Steps:

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Prepare for Render deployment"
   git push origin main
   ```

2. **Connect to Render:**
   - Go to [Render Dashboard](https://dashboard.render.com)
   - Click "New +" → "Web Service"
   - Connect your GitHub repository `phstatic1/phstatic2`
   - Choose the `main` branch

3. **Configure Environment:**
   - Runtime: Node
   - Build Command: `npm install && npm run build`
   - Start Command: `npm start`
   - Environment Variables:
     - Add `GEMINI_API_KEY` with your actual API key

4. **Deploy:**
   - Click "Create Web Service"
   - Render will automatically build and deploy your app

Your app will be available at `https://<your-service-name>.onrender.com`

## Files for Deployment

- `render.yaml` - Render deployment configuration
- `server.js` - Express server for production
- `.env.example` - Example environment variables
- `package.json` - Updated with start script and express dependency

