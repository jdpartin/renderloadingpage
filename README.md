# RenderLoadingPage

A static site designed for the Render free tier to display a loading message while your web app starts up. Once the web app is ready, it automatically redirects to your application.

## Features

- **Customizable Loading Message:** Easily update the loading message to fit your app's theme or branding.
- **Automatic Redirection:** Redirects to your web app as soon as it's ready.
- **Lightweight and Fast:** Minimal static HTML, CSS, and JavaScript for quick loading.
- **Open Source:** Free to use and modify for your projects.

## Why Use RenderLoadingPage?

The Render free tier often experiences cold starts, causing delays before the app becomes accessible. This project provides a better user experience by showing a friendly loading message instead of an empty screen or error.

## How It Works

1. Deploy the static loading page to Render or any other hosting platform.
2. Configure the static page to periodically ping your web app to check its status.
3. Automatically redirect users to the web app once it’s ready.

## Installation and Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/RenderLoadingPage.git
