# LED Exposure Calculator

A web app that normalizes LED sponsorship schedule data with broadcast/streaming exposure to project media value, exposure, and impressions for any amount of scheduled inventory.

## What It Does

Upload two CSVs:
1. **LED Schedule Report** — in-game scheduled signage time by partner
2. **Broadcast Exposure Report** — actual on-screen time, value, and impressions

The app:
- Matches games by date + partner
- Filters to in-game only (excludes pregame/halftime/postgame)
- Normalizes everything to 30-second increments
- Calculates averages across all matched records
- Lets you toggle between Broadcast TV, Streaming, and Combined views
- Projects value/exposure/impressions for any number of 30-second units

## How to Deploy (Free)

### Step 1: Create a GitHub Account
Go to [github.com](https://github.com) and sign up if you don't have an account.

### Step 2: Create a New Repository
1. Click the **+** icon in the top right → **New repository**
2. Name it something like `led-calculator`
3. Set it to **Public** (required for free Vercel deployment)
4. Check **Add a README file**
5. Click **Create repository**

### Step 3: Upload the App
1. In your new repo, click **Add file** → **Upload files**
2. Drag in the `index.html` file
3. Scroll down, click **Commit changes**

### Step 4: Deploy to Vercel
1. Go to [vercel.com](https://vercel.com) and sign up with your GitHub account
2. Click **Add New...** → **Project**
3. Find your `led-calculator` repo and click **Import**
4. Leave all settings as default
5. Click **Deploy**

Within ~30 seconds, you'll get a live URL like `led-calculator-abc123.vercel.app`

### Step 5: Share It
That URL works for anyone, anywhere. Bookmark it, send it to coworkers, put it in your email signature.

## Updating the App
Any changes you make to `index.html` on GitHub (edit the file, commit) will automatically redeploy to Vercel within seconds. No manual deployment needed.

## CSV Format Requirements

### LED Schedule CSV needs columns:
- **Game Date** — format: MM/DD/YYYY
- **Partner** — brand name
- **Game Period** — "1st Half", "2nd Half", "Pregame", "Halftime", "Postgame"
- **Duration** — seconds scheduled

### Broadcast Exposure CSV needs columns:
- **Date** — format: MM/DD/YYYY (must match LED dates)
- **Partner** — brand name (must match LED partners)
- **View Duration** — seconds on screen
- **Total Value*** — media value in USD
- **Brand HH Impressions** — broadcast TV impressions
- **Brand Streaming Impressions** — streaming impressions

The app is flexible with column names (case-insensitive, partial matches work).
