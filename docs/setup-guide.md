# GitHub Profile Landing Page - Setup Guide

This document provides instructions on how to set up, customize, and maintain your GitHub profile landing page.

## Table of Contents
- [Initial Setup](#initial-setup)
- [Customizing Your Profile](#customizing-your-profile)
- [Updating Private Project References](#updating-private-project-references)
- [Setting Up GitHub Actions](#setting-up-github-actions)
- [Regular Maintenance](#regular-maintenance)

## Initial Setup

1. **Create a Special Repository**:
   - Create a new repository on GitHub with the exact same name as your GitHub username (`dtembe`)
   - This special repository will be displayed on your GitHub profile page

2. **Add the README.md**:
   - Copy the contents of `/home/em7admin/pyDev/_copilotDev/github-landing-page-dtembe/README.md` to your special repository
   - Commit and push the changes

3. **Set Up Assets**:
   - Create an `/assets` folder in your repository
   - Upload any custom images, icons, or logos you want to use

## Customizing Your Profile

### Personal Information
- Update your name, title, and social media links at the top of the README
- Customize the header image by modifying the Capsule Render URL parameters
- Update your social media badges with your actual profile links

### Tech Stack & Skills
- Modify the technology badges to reflect your actual expertise
- Adjust the progress bars in the "Highlighted Skills" section to match your skill levels
- Add or remove technologies as needed

### GitHub Stats
The GitHub stats section uses dynamic cards that automatically update:
- The cards use your GitHub username to fetch stats
- They update whenever someone views your profile
- No maintenance required beyond the initial setup

## Updating Private Project References

The "Private Project Portfolio" section is designed to showcase your work without exposing sensitive details:

1. **Update Project Table**:
   ```markdown
   | Project | Role | Technology Stack | Status |
   |---------|------|-----------------|--------|
   | **[Project Name]** | [Your Role] | ![Tech](https://img.shields.io/badge/Tech-Code-Color?logo=logo-name) | ![Status](https://img.shields.io/badge/Status-label?style=flat-square) |
   ```

2. **Projects by Category**:
   - Update the collapsible sections with your actual projects
   - Group similar projects together for better organization
   - Keep descriptions concise but informative

3. **What I'm Working On**:
   - Update the Mermaid mindmap to reflect your current focus areas
   - This gives visitors insight into your current interests without sharing confidential details

## Setting Up GitHub Actions

To enable dynamic content updates (like blog posts), set up GitHub Actions:

1. **Blog Posts Workflow**:
   Create a file at `.github/workflows/blog-post-workflow.yml`:

   ```yaml
   name: Latest blog posts workflow
   on:
     schedule:
       # Runs every day at 00:00
       - cron: '0 0 * * *'
     workflow_dispatch:
   
   jobs:
     update-readme-with-blog:
       name: Update README with latest blog posts
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v2
         - uses: gautamkrishnar/blog-post-workflow@master
           with:
             feed_list: "https://yourblog.com/feed"
             max_post_count: 5
   ```

2. **Profile Stats Update**:
   Your profile view counter and GitHub stats cards update automatically, but you can create a manual update workflow if needed.

## Regular Maintenance

To keep your profile fresh and engaging:

1. **Quarterly Review**:
   - Update project statuses and descriptions
   - Refresh your "What I'm Working On" section
   - Adjust skill levels as you grow

2. **Visual Refreshes**:
   - Periodically update your banner image or theme colors
   - Add new visualization types as they become available

3. **Content Updates**:
   - Add new accomplishments or certifications
   - Update blog post links manually if not using GitHub Actions

---

This setup provides a professional, visually appealing GitHub profile that effectively showcases your skills and projects while respecting the confidentiality of your private repositories.
