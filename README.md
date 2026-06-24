# gh-deployment-workflow

A portfolio website automatically deployed to **GitHub Pages** using **GitHub Actions**.

## 🚀 Live Site

Visit: [Clickable Text](`https://vishwasvarma.github.io/gh-deployment-workflow/`)

---

## 📋 Project Overview

This project demonstrates a CI/CD pipeline using GitHub Actions to automatically deploy a static portfolio website to GitHub Pages whenever `index.html` is updated on the `main` branch and I am doing this for [Clickable Text](`https://roadmap.sh/projects/github-actions-deployment-workflow`).

---

## ⚙️ How It Works

The workflow in `.github/workflows/deploy.yml` is triggered **only** when a push to `main` includes changes to `index.html`. This keeps unnecessary deployments from running on unrelated file changes.

### Workflow Steps:

1. **Checkout** – Pulls the latest code from the repo
2. **Configure Pages** – Sets up the GitHub Pages environment
3. **Upload Artifact** – Packages the site files for deployment
4. **Deploy** – Publishes the site to GitHub Pages

---

## 📁 Project Structure

```
gh-deployment-workflow/
├── index.html                  # Main portfolio page
├── README.md                   # Project documentation
└── .github/
    └── workflows/
        └── deploy.yml          # GitHub Actions CI/CD workflow
```

---

## 🛠️ Setup Instructions

### 1. Enable GitHub Pages

- Go to your repo → **Settings** → **Pages**
- Under **Source**, select **GitHub Actions**
- Save the settings

### 2. Push a Change to Trigger Deployment

Any push to `main` that modifies `index.html` will automatically trigger the workflow and deploy your updated portfolio.

### 3. Monitor the Workflow

- Go to the **Actions** tab in your repository
- Watch the `Deploy Portfolio to GitHub Pages` workflow run in real time

---

## 🔒 Permissions

The workflow uses the following GitHub token permissions:

- `pages: write` – to deploy to GitHub Pages
- `id-token: write` – for OIDC authentication
- `contents: read` – to read repository files

---

## 🌱 What I Learned

- Setting up GitHub Actions workflows
- Using path filters to trigger jobs only on relevant file changes
- Deploying static sites using the official `actions/deploy-pages` action
- Understanding GitHub Pages environments and deployment URLs

---

## 🔧 Tech Stack

- **HTML/CSS** – Static portfolio site
- **GitHub Actions** – CI/CD pipeline
- **GitHub Pages** – Hosting
