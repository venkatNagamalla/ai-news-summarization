# 🤖 AI News Summarizer & Daily Tech Newsletter

An automated **AI-powered news summarization and newsletter workflow** built with **n8n, Google Gemini, RSS feeds, SerpAPI, and Gmail**.

The workflow automatically collects the latest **AI and technology news**, retrieves relevant **AI events**, uses **Google Gemini** to summarize and organize the information, and delivers a concise daily newsletter through email.

---

## 🚀 Project Overview

Keeping up with the rapidly changing AI and technology landscape can be time-consuming.

This project automates the entire process:

**Collect → Aggregate → Summarize → Organize → Email**

Every day, the workflow collects information from multiple sources and uses Generative AI to transform the raw data into an easy-to-read **Tech Brief**.

---

## ✨ Features

* 📰 Automatically collects AI news from RSS feeds
* 💻 Collects broader technology updates
* 📅 Retrieves upcoming AI and technology events
* 🤖 Uses **Google Gemini** for AI-powered summarization
* 🔄 Aggregates information from multiple sources
* 📧 Automatically sends a daily newsletter through Gmail
* ⏰ Runs automatically using an n8n Schedule Trigger
* 🧠 Categorizes information into AI News, Technology Updates, and Upcoming AI Events
* 🔐 API credentials are configured separately using n8n credentials

---

## 🛠️ Technologies Used

| Technology        | Purpose                         |
| ----------------- | ------------------------------- |
| **n8n**           | Workflow automation             |
| **Google Gemini** | AI-powered summarization        |
| **RSS Feeds**     | AI & technology news collection |
| **SerpAPI**       | AI event information retrieval  |
| **Gmail**         | Automated newsletter delivery   |
| **REST APIs**     | Data retrieval and integration  |
| **JSON**          | Workflow configuration          |

---

## 🔄 Workflow Architecture

```text
                 ┌──────────────────┐
                 │  Schedule Trigger │
                 └─────────┬────────┘
                           │
              ┌────────────┼────────────┐
              │            │            │
              ▼            ▼            ▼
        ┌──────────┐ ┌──────────┐ ┌─────────────┐
        │ AI News  │ │   Tech   │ │ AI Events   │
        │ RSS Feed │ │ RSS Feed │ │  SerpAPI    │
        └────┬─────┘ └────┬─────┘ └──────┬──────┘
             │            │              │
             └────────────┼──────────────┘
                          ▼
                  ┌──────────────┐
                  │ Data Merger  │
                  └──────┬───────┘
                         ▼
                  ┌──────────────┐
                  │     Data     │
                  │  Aggregator  │
                  └──────┬───────┘
                         ▼
                  ┌──────────────┐
                  │    Google    │
                  │    Gemini    │
                  └──────┬───────┘
                         ▼
                  ┌──────────────┐
                  │ AI Summarized│
                  │  Tech Brief  │
                  └──────┬───────┘
                         ▼
                  ┌──────────────┐
                  │     Gmail    │
                  │   Newsletter │
                  └──────────────┘
```

---

## 📌 Workflow Steps

### 1. Schedule Trigger

The workflow starts automatically at a scheduled time using the **n8n Schedule Trigger**.

### 2. AI News Collection

An RSS feed is used to collect the latest AI-related news articles.

### 3. Technology News Collection

A technology-focused RSS feed collects broader technology updates.

### 4. AI Event Collection

SerpAPI is used to retrieve information about upcoming AI and technology events.

### 5. Data Merging

The information collected from different sources is merged into a single workflow.

### 6. Data Aggregation

All collected items are aggregated so that the AI model can process the information together.

### 7. AI Summarization

**Google Gemini** processes the collected information and generates a structured daily technology brief.

The AI is instructed to:

* Select important AI developments
* Summarize technology updates
* Identify upcoming AI events
* Include article/event links
* Keep the content concise and professional
* Avoid inventing information

### 8. Email Delivery

The generated Tech Brief is automatically sent through **Gmail**.

---

## 🧠 Sample Newsletter Structure

```text
Hi there,

Here's your Tech Brief:

AI NEWS HIGHLIGHTS
======================

HEADLINE IN ALL CAPS

Summary of the AI development...

Link: Article URL


TECHNOLOGY UPDATES
======================

HEADLINE IN ALL CAPS

Summary of the technology update...

Link: Article URL


UPCOMING AI EVENTS
======================

EVENT NAME

Summary of the event...

Link: Event URL


Your AI Intelligence Team
```

---

## 🔐 Security

**Important:** API keys, OAuth credentials, personal email addresses, and other sensitive information should **not** be committed to the public repository.

Before uploading the workflow to GitHub:

* Remove API keys
* Remove OAuth credentials
* Remove personal email addresses
* Remove n8n instance-specific information
* Use environment variables or n8n Credentials
* Use placeholder values in publicly shared workflow files

Example:

```json
{
  "api_key": "YOUR_SERPAPI_API_KEY"
}
```

---

## 📂 Project Structure

```text
AI-News-Summarizer/
│
├── workflow/
│   └── AI-News-Summarizer.json
│
├── screenshots/
│   └── workflow.png
│
├── .gitignore
│
└── README.md
```

---

## ⚙️ Setup

### Prerequisites

You need:

* [n8n](https://n8n.io/)
* Google Gemini API access
* SerpAPI account
* Gmail account connected to n8n
* RSS feed sources

### Import the Workflow

1. Open your n8n instance.
2. Create a new workflow.
3. Import `AI-News-Summarizer.json`.
4. Configure the required credentials.
5. Add your Gemini credentials.
6. Configure your Gmail credentials.
7. Configure your SerpAPI key securely.
8. Review the RSS feed URLs.
9. Test the workflow manually.
10. Activate the workflow.

---

## 🎯 What I Learned

This project helped me gain practical experience with:

* **Workflow Automation**
* **Generative AI**
* **Google Gemini API**
* **n8n**
* **REST API Integration**
* **RSS Feed Integration**
* **Data Aggregation**
* **Prompt Engineering**
* **AI-powered Content Generation**
* **Gmail Automation**
* **API Authentication & Credentials Management**

---

## 🔮 Future Improvements

Potential improvements include:

* [ ] Add more trusted news sources
* [ ] Add AI news filtering by topic
* [ ] Add duplicate article detection
* [ ] Add article relevance scoring
* [ ] Add a web dashboard
* [ ] Store summarized articles in MongoDB
* [ ] Add Telegram/WhatsApp notifications
* [ ] Generate a daily PDF newsletter
* [ ] Add multilingual summaries
* [ ] Add personalized news preferences
* [ ] Add error handling and workflow monitoring

---

## 💡 Use Case

This workflow can be adapted for:

* Personal AI news tracking
* Technology newsletters
* Company intelligence reports
* Research automation
* Industry trend monitoring
* Automated content curation
* AI-powered business reports

---

## 👨‍💻 Author

**Venkat Shiva Durga Nagamalla**

**Full Stack Developer | MERN | Generative AI | Python | SQL | AI Automation with n8n**

---

## ⭐ If You Find This Project Useful

Feel free to **star ⭐ the repository** and explore the workflow.

Feedback and suggestions are always welcome!
