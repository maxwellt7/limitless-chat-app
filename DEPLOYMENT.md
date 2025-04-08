# Deployment Guide for Limitless Chat App

This guide will walk you through deploying the Limitless Chat App to Vercel.

## Prerequisites

1. A GitHub account
2. A Vercel account (you can sign up at [vercel.com](https://vercel.com) using your GitHub account)
3. Your API keys:
   - Limitless API Key: `sk-2a4a4d9e-23d2-4e5a-aba1-3e3809b4d287`
   - OpenAI API Key: `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`
   - Anthropic API Key: `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`

## Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and sign in to your account
2. Click on the "+" icon in the top right corner and select "New repository"
3. Name your repository (e.g., "limitless-chat-app")
4. Choose "Public" or "Private" visibility (your choice)
5. Click "Create repository"

## Step 2: Push the Code to GitHub

Once your repository is created, you'll need to push the code to GitHub. You can do this by running the following commands in your terminal:

```bash
# Navigate to the project directory
cd limitless-chat-app

# Initialize git repository
git init

# Add all files to git
git add .

# Commit the files
git commit -m "Initial commit"

# Add your GitHub repository as remote
git remote add origin https://github.com/YOUR_USERNAME/limitless-chat-app.git

# Push the code to GitHub
git push -u origin main
```

Replace `YOUR_USERNAME` with your GitHub username.

## Step 3: Deploy to Vercel

1. Go to [Vercel](https://vercel.com) and sign in with your GitHub account
2. Click on "Add New..." and select "Project"
3. Find and select your "limitless-chat-app" repository
4. Vercel will automatically detect that it's a Next.js project
5. Before deploying, you need to add your environment variables:
   - Click on "Environment Variables"
   - Add the following variables:
     - `LIMITLESS_API_KEY`: Your Limitless API key
     - `OPENAI_API_KEY`: Your OpenAI API key
     - `ANTHROPIC_API_KEY`: Your Anthropic API key
6. Click "Deploy"

Vercel will now build and deploy your application. Once the deployment is complete, you'll be given a URL where your application is hosted (e.g., `https://limitless-chat-app.vercel.app`).

## Step 4: Verify the Deployment

1. Visit the URL provided by Vercel
2. You should see the Limitless Chat App interface
3. The app should be fully functional with:
   - Chat interface with your Limitless data
   - Daily summaries of your Limitless data
   - Multiple LLM options (OpenAI and Anthropic)

## Updating Your Application

Whenever you make changes to your code and push them to GitHub, Vercel will automatically rebuild and redeploy your application.

## Custom Domain (Optional)

If you want to use a custom domain for your application:

1. Go to your project on Vercel
2. Click on "Settings" and then "Domains"
3. Add your custom domain and follow the instructions to configure DNS settings

## Troubleshooting

If you encounter any issues during deployment:

1. Check that all environment variables are correctly set
2. Verify that your API keys are valid
3. Check the build logs in Vercel for any errors
4. Make sure your repository contains all the necessary files

For more help, refer to the [Vercel documentation](https://vercel.com/docs) or [contact Vercel support](https://vercel.com/support).
