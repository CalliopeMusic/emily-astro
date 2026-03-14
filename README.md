# Emily · Astrology Reading

A personal astrology dashboard with natal chart, predictive transits, and an AI-powered Oracle (powered by OpenAI GPT-4o).

## Project Structure

```
emily-astro/
├── public/
│   └── index.html        # The full dashboard
├── api/
│   └── ask.js            # Vercel serverless function (proxies OpenAI API)
├── vercel.json           # Vercel routing config
└── package.json
```

---

## Step 1 — Create the GitHub Repository

1. Go to [github.com/new](https://github.com/new)
2. Sign in as **CalliopeMusic**
3. Repository name: `emily-astro`
4. Set to **Public** or **Private** (your choice)
5. ⚠️ Leave everything else **unchecked** — no README, no .gitignore, no license
6. Click **Create repository**

---

## Step 2 — Install Git (if you don't have it)

Check if you already have it:
```bash
git --version
```
If not installed, download it at [git-scm.com/downloads](https://git-scm.com/downloads) and run the installer.

---

## Step 3 — Push the Project to GitHub

1. Unzip `emily-astro.zip` on your computer
2. Open **Terminal** (Mac) or **Command Prompt / PowerShell** (Windows)
3. Navigate into the unzipped folder:
```bash
cd path/to/emily-astro
```
4. Run these commands one at a time:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/CalliopeMusic/emily-astro.git
git push -u origin main
```
5. GitHub may ask you to sign in — follow the prompts

✅ Your code is now on GitHub at `github.com/CalliopeMusic/emily-astro`

---

## Step 4 — Get Your OpenAI API Key

1. Go to [platform.openai.com/api-keys](https://platform.openai.com/api-keys)
2. Sign in (or create a free account)
3. Click **Create new secret key**
4. Give it a name like `emily-astro`
5. **Copy the key** — you won't be able to see it again (`sk-...`)

---

## Step 5 — Deploy to Vercel

1. Go to [vercel.com](https://vercel.com) and sign up / sign in (you can use your GitHub account)
2. Click **Add New Project**
3. Click **Import** next to `CalliopeMusic/emily-astro`
4. On the configuration screen, leave **all settings as default** — no framework, no build command
5. Scroll down to **Environment Variables** and add:
   - **Name:** `OPENAI_API_KEY`
   - **Value:** paste your key from Step 4
6. Click **Deploy**

⏱️ Vercel will build and deploy in about 30 seconds.

✅ Your live URL will be something like `emily-astro.vercel.app`

---

## Local Development (Optional)

To run the site locally with the Oracle working:

```bash
npm install -g vercel
```

Create a file called `.env` in the project root:
```
OPENAI_API_KEY=sk-...your key here...
```

Then run:
```bash
vercel dev
```

Visit `http://localhost:3000`

