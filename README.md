
# 🤖 AI LinkedIn Content Automation

An AI-powered LinkedIn content automation workflow built with **n8n**, **Google Sheets**, and **OpenAI**.

This project automates the process of creating and managing LinkedIn content. Instead of manually researching topics, writing posts, checking their status, and preparing visual content, the workflow connects these steps into an automated pipeline.

## 🚀 Overview

The workflow takes content topics and publishing information from Google Sheets, processes them through n8n, and uses AI to generate professional LinkedIn content.

The automation is designed to help individuals, creators, marketers, and businesses maintain a consistent LinkedIn presence with less manual effort.

## ✨ Features

* 📊 Google Sheets integration for content management
* 🤖 AI-powered LinkedIn post generation
* 📝 Automatically creates professional LinkedIn captions
* 🖼️ AI-based image generation for LinkedIn posts
* 🔄 Workflow-based automation using n8n
* ✅ Post status management
* 📅 Publishing date management
* 🔀 Conditional workflow logic using IF nodes
* ⚡ Automated content processing
* 📈 Scalable workflow for multiple posts

## 🛠️ Technologies Used

* **n8n** — Workflow automation
* **Google Sheets** — Content database and management
* **OpenAI** — AI content generation
* **JavaScript / n8n Expressions** — Dynamic data processing
* **LinkedIn** — Target publishing platform

## 🔄 Workflow

The basic automation flow is:

```text
Google Sheets
      ↓
Read Content Topic
      ↓
Check Post Status
      ↓
IF Condition
      ↓
AI Content Generation
      ↓
Generate Visual Content
      ↓
LinkedIn Publishing
      ↓
Update Status
```

## 📋 Google Sheets Structure

The Google Sheet can contain fields such as:

| Field         | Description                  |
| ------------- | ---------------------------- |
| Publish Date  | Scheduled publishing date    |
| Topic         | Topic for the LinkedIn post  |
| Status        | Current status of the post   |
| LinkedIn Post | Generated LinkedIn content   |
| Image         | Generated image or image URL |

Example:

```text
Publish Date: 2026-09-07
Topic: What is Elon Musk up to?
Status: Published
```

## 🧠 AI Content Generation

The AI receives the selected topic and generates a professional LinkedIn post.

The generated content can include:

* Strong opening hook
* Informative content
* Key insights
* Professional tone
* Call-to-action
* Relevant hashtags

Example topic:

```text
What is Elon Musk up to?
```

The AI converts the topic into a structured LinkedIn-ready post.

## 🖼️ AI Image Generation

After generating the LinkedIn content, the workflow can pass the generated post to an image-generation step.

Example prompt:

```text
Generate an image that perfectly represents the LinkedIn post.
```

This allows every LinkedIn post to have a relevant visual instead of relying only on text.

## 🔀 Conditional Logic

The workflow uses n8n's **IF node** to check the status of each post.

For example:

```text
Status = Published
```

The workflow can use this condition to determine whether a post should continue through the publishing workflow or be skipped.

## ⚙️ Setup

### 1. Install / Create n8n

Create an n8n Cloud account or run n8n locally.

### 2. Connect Google Sheets

Create a Google Sheet containing your content information and connect it to n8n using Google Sheets credentials.

### 3. Configure OpenAI

Add your OpenAI API credentials inside n8n and select the required model.

### 4. Create the Workflow

Connect the nodes according to the workflow structure:

```text
Google Sheets Trigger
        ↓
IF
        ↓
AI Content Generation
        ↓
Image Generation
        ↓
LinkedIn
```

### 5. Configure Expressions

n8n expressions can be used to dynamically pass Google Sheets data between nodes.

Example:

```javascript
{{ $json.Topic }}
```

For status:

```javascript
{{ $json.Status }}
```

## 🔐 Environment & Security

Never upload API keys, passwords, OAuth credentials, or other secrets to GitHub.

Use n8n credentials or environment variables to securely store sensitive information.

Do not commit files containing:

```text
API_KEY
OPENAI_API_KEY
CLIENT_SECRET
ACCESS_TOKEN
PASSWORD
```

## 📌 Use Cases

This automation can be used for:

* Personal LinkedIn content
* Business social media management
* Marketing agencies
* Startup content automation
* Personal branding
* AI-generated educational posts
* Tech news content
* Company thought leadership
* Social media scheduling

## 🎯 Future Improvements

Possible future enhancements include:

* Automatic LinkedIn publishing
* LinkedIn analytics tracking
* Multiple social media platforms
* Automatic hashtag generation
* Content calendar dashboard
* AI-generated content variations
* Automatic image generation
* Post performance analysis
* Automatic reposting
* Email notifications
* Approval workflow before publishing

## 📁 Project Structure

```text
AI-LinkedIn-Content-Automation/
│
├── README.md
├── workflow/
│   └── linkedin-automation.json
│
├── prompts/
│   └── content-generation.txt
│
└── docs/
    └── workflow-diagram.png
```

## ⚠️ Notes

This project requires valid credentials for the connected services. API usage may incur costs depending on the selected AI provider and account plan.

Always test the workflow before enabling automatic publishing.

## 👩‍💻 Author

**Eman Kanwal**

Built as an AI automation project focused on intelligent content creation and social media workflow automation.
