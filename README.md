# Hello World Web App

A simple "Hello World" web page built with Node.js and Express, ready to deploy to Heroku.

## Local Development

### Prerequisites
- Node.js (v18 or higher)
- npm

### Setup

1. Install dependencies:
```bash
npm install
```

2. Run the server locally:
```bash
npm start
```

3. Open your browser and visit:
```
http://localhost:3000
```

## Deploy to Heroku

### Prerequisites
- A [Heroku account](https://signup.heroku.com/)
- [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli) installed
- Git installed

### Deployment Steps

#### Method 1: Deploy via Heroku CLI

1. Login to Heroku:
```bash
heroku login
```

2. Create a new Heroku app:
```bash
heroku create your-app-name
```
(Replace `your-app-name` with your desired app name, or omit it to get a random name)

3. Push your code to Heroku:
```bash
git add .
git commit -m "Initial commit"
git push heroku main
```

4. Open your deployed app:
```bash
heroku open
```

#### Method 2: Deploy via GitHub Integration

1. Push your code to GitHub:
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

2. Go to your [Heroku Dashboard](https://dashboard.heroku.com/)

3. Click "New" → "Create new app"

4. Give your app a name and choose a region

5. Under "Deployment method", select "GitHub"

6. Connect your GitHub account and search for your repository

7. Click "Connect" next to your repository

8. Enable "Automatic Deploys" (optional - deploys automatically when you push to GitHub)

9. Click "Deploy Branch" to deploy manually

10. Once deployed, click "View" to see your live app!

## Project Structure

```
.
├── server.js           # Express server with Hello World route
├── package.json        # Node.js dependencies and scripts
├── Procfile           # Tells Heroku how to run the app
├── .gitignore         # Files to exclude from Git
└── README.md          # This file
```

## How It Works

- **server.js**: Creates an Express server that listens on the PORT environment variable (Heroku sets this automatically)
- **Procfile**: Tells Heroku to run `node server.js` as a web process
- **package.json**: Defines the start script and Node.js version for Heroku

## Troubleshooting

### Local Issues
- **Port already in use**: Change the PORT in server.js or kill the process using port 3000
- **Dependencies not installed**: Run `npm install`

### Heroku Issues
- **Build failed**: Check that your `package.json` has the correct `start` script
- **App crashed**: Run `heroku logs --tail` to see error messages
- **Port issues**: Make sure your server uses `process.env.PORT`

## Next Steps

- Customize the HTML in [server.js](server.js)
- Add more routes
- Connect a database
- Add a custom domain

## License

MIT
