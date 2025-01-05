# RenderLoadingPage

A static site designed for the Render free tier to display a loading message while your web app starts up. Once the web app is ready, it automatically redirects users to your application.

## Features

- **Customizable Loading Message**: Easily update the loading message to match your app's theme or branding.
- **Automatic Redirection**: Seamlessly redirects to your web app as soon as it’s ready.
- **Lightweight and Fast**: Uses minimal HTML, CSS, and JavaScript for quick loading.
- **Open Source**: Free to use and adapt for your projects.

## Why Use RenderLoadingPage?

The Render free tier often experiences cold starts, which can delay the availability of your app. This project enhances user experience by displaying a friendly loading message instead of an empty screen or error.

---

## How It Works

1. **Dynamic App Loading**: Users are directed to a static loading page hosted separately.
2. **Periodic Status Checks**: The loading page pings your Render app to check its readiness.
3. **Automatic Redirection**: When the app responds successfully, users are redirected to your application.

---

## Installation and Setup

### Step 1: Update Your App's CORS Settings
To allow the loading page to check your app's status, you must add the following URL to your app's CORS settings:
```
https://renderloadingpage.onrender.com
```

For example, if you're using Express.js, update your CORS configuration:
```javascript
const cors = require('cors');
app.use(cors({
    origin: ['https://renderloadingpage.onrender.com'],
}));
```

### Step 2: Use the Loading Page
To use the loading page, construct the URL as follows:
```
https://renderloadingpage.onrender.com?site=[YOUR_RENDER_SITE_NAME]
```
- Replace `[YOUR_RENDER_SITE_NAME]` with the name of your Render app (omit `.onrender.com`).
- Example: If your Render app is `example.onrender.com`, the URL would be:
  ```
  https://renderloadingpage.onrender.com?site=example
  ```

### Step 3: Deploy Your Own (Optional)
If you prefer to host your own version of the loading page:
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/RenderLoadingPage.git
   ```
2. Customize the `index.html` file to suit your needs.
3. Deploy the page to any hosting provider (e.g., Render, Netlify, or Vercel).

---

## Example Usage

1. Deploy your app on Render with the appropriate CORS settings.
2. Share the loading page URL with users:
   ```
   https://renderloadingpage.onrender.com?site=example
   ```
3. Users will see a loading message while your app starts, and then they will be redirected once the app is ready.

---

## Contributing

Contributions are welcome! Feel free to:
- Submit issues for bugs or feature requests.
- Open pull requests to improve the project.

---

## License

This project is licensed under the Apache 2.0 License
