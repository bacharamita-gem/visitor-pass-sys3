# Visitor Pass System - Gem Drytech Systems LLP

A comprehensive visitor management system with photo capture, PDF generation, and Google Sheets integration.

![Visitor Pass System](assets/screenshots/main-interface.png)

## 📋 Features

- ✅ **Visitor Registration** - Complete form with validation
- 📸 **Photo Capture** - Take photos via camera or upload
- 🆔 **Auto-generated IDs** - Format: GD + DDMMYY + 001
- 📄 **PDF Generation** - Professional visitor passes with photo
- ☁️ **Google Drive Integration** - Photos stored with shareable links
- 📊 **Google Sheets** - All data saved automatically
- 📱 **Responsive Design** - Works on mobile and desktop
- 🔍 **Real-time Stats** - Today's count, active passes, total entries

## 🚀 Live Demo

[Add your deployed web app URL here]

## 🛠️ Technologies Used

- **Google Apps Script** - Backend logic
- **Google Sheets** - Database
- **Google Drive** - Photo storage
- **HTML5/CSS3** - Frontend structure
- **JavaScript** - Client-side functionality
- **jsPDF** - PDF generation
- **Font Awesome** - Icons

## 📦 Installation

### Prerequisites
- Google Account
- Google Sheets
- Basic knowledge of Google Apps Script

### Step 1: Create Google Sheet
1. Create a new Google Sheet
2. Copy the Sheet ID from URL: `https://docs.google.com/spreadsheets/d/[SHEET_ID]/edit`
3. Sheet will auto-create with proper headers

### Step 2: Deploy Apps Script
1. Open Google Apps Script (script.google.com)
2. Create new project
3. Copy `Code.gs` content
4. Update `CONFIG.sheetId` with your Sheet ID
5. Save and deploy as Web App
6. Set access to "Anyone" or "Anyone with link"

### Step 3: Configure HTML
1. Update the deployment URL in your HTML if needed
2. Test the form submission

## ⚙️ Configuration

Edit the `CONFIG` object in `Code.gs`:

```javascript
const CONFIG = {
  sheetId: 'YOUR_SHEET_ID_HERE',
  mainSheet: 'VisitorData',
  idConfig: {
    prefix: 'GD',
    numberLength: 3
  },
  timeZone: 'Asia/Kolkata',
  photoFolderName: 'Visitor_Photos',
  companyName: 'Gem Drytech Systems LLP'
};
