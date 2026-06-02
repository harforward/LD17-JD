# JD17 Constituent Outreach Dashboard

**Assemblyman Joe Danielsen – 17th Legislative District**
Constituent Outreach Analytics Portal

---

## What This Is

A secure, password-protected analytics dashboard for the LD17 Constituent Outreach Program. It includes:
- 🔐 Password login screen (`district17`)
- 📊 Three stakeholder views: Executive, Oversight & Audit, Operations
- 📱 Fully mobile-responsive
- 📈 Real program data (Nov 2024 – Apr 2026)
- 🔮 Predictive forecast with adjustable sliders

---

## How to Deploy to GitHub Pages (Step-by-Step for Beginners)

### What You Need First
- A free GitHub account → [github.com](https://github.com)
- The `index.html` file from this folder

---

### Step 1 — Create a GitHub Account (skip if you have one)
1. Go to [github.com/signup](https://github.com/signup)
2. Enter your email, create a username and password
3. Verify your email address

---

### Step 2 — Create a New Repository
1. Click the **+** icon in the top-right corner of GitHub
2. Select **"New repository"**
3. Name it exactly: `jd17-dashboard`
   - ✅ Make it **Public** (required for free GitHub Pages hosting)
   - Leave everything else as default
4. Click **"Create repository"**

---

### Step 3 — Upload the Dashboard File
1. On your new repository page, click **"uploading an existing file"** (the link in the middle of the page)
2. Drag and drop the `index.html` file onto the upload area — OR click "choose your files" and select it
3. Scroll down. In the "Commit changes" box, type a message like: `Add JD17 dashboard`
4. Click the green **"Commit changes"** button

---

### Step 4 — Turn on GitHub Pages
1. Click the **"Settings"** tab at the top of your repository
2. In the left sidebar, scroll down and click **"Pages"**
3. Under **"Branch"**, click the dropdown that says "None" and select **main**
4. Leave the folder as `/ (root)`
5. Click **Save**

---

### Step 5 — Get Your Live URL
1. Wait 1–3 minutes
2. Refresh the Pages settings page
3. You will see a green box that says:
   **"Your site is live at: https://YOUR-USERNAME.github.io/jd17-dashboard/"**
4. Click that link — your dashboard is live!

---

### Step 6 — Share the Link
Send this URL to your authorized staff and stakeholders:
```
https://YOUR-USERNAME.github.io/jd17-dashboard/
```
Password: `district17`

---

## How to Update the Dashboard Later

1. Go to your repository on GitHub
2. Click on `index.html`
3. Click the **pencil icon** (Edit) in the top-right of the file view
4. Make your changes
5. Scroll down and click **"Commit changes"**
6. Your live site will update automatically within 1–2 minutes

---

## Changing the Password

The password is set in `index.html`. To change it:
1. Open `index.html` in the GitHub editor
2. Find this line (around line 380):
   ```
   if (pwd === 'district17') {
   ```
3. Replace `district17` with your new password
4. Save/commit the changes

> ⚠️ Note: Because this is a static site, the password is in the HTML source. This is appropriate for internal district use. For a higher-security deployment, consider Netlify with environment variables (ask your IT contact).

---

## Optional: Use a Custom Domain (e.g., dashboard.danielsen.nj.gov)

If the district has a custom domain:
1. Go to Settings → Pages in your GitHub repo
2. Under "Custom domain", enter your domain (e.g., `dashboard.yourdomain.com`)
3. Contact your domain registrar or IT team to add a CNAME record pointing to `YOUR-USERNAME.github.io`

---

## File Structure

```
jd17-dashboard/
└── index.html    ← The entire dashboard (single file, no dependencies needed)
```

Everything is self-contained in `index.html`. No server, no database, no build step required.

---

## Data Updates

All data is embedded in the `index.html` file in the `MONTHLY_DATA` and `AUDIT_DATA` objects (around line 350). To add a new month:

```javascript
const MONTHLY_DATA = {
  labels: [..., 'May\'26'],      // Add new label
  calls:  [..., 450],            // Add monthly total calls
  answered: [..., 75],           // Add answered calls
  engaged:  [..., 40],           // Add engaged conversations
  cases:    [..., 8],            // Add cases opened
  satisfaction: [..., 97],       // Add satisfaction % (number, not decimal)
  answerRate: [..., 16.7],       // Answered ÷ Calls × 100
};
```

And add a row to `AUDIT_DATA`:
```javascript
{period:'2026-05', muni:'NB + SBB + Franklin', calls:450, answered:75, engaged:40, cases:8},
```

---

## Support

For technical questions about updating or extending this dashboard, contact your data team or refer to the full Data Architecture Blueprint document.

Password: `district17`
Program: LD17 Constituent Outreach Analytics
Built: June 2026
