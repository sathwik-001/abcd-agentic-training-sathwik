# 🧠 Article Summarizer (n8n + Gemini + Notion)

Automatically summarize any online article using **Google Gemini AI** and save the summary into a **Notion document** — all powered by **n8n workflow automation**.

---

## 🚀 Overview

The **Article Summarizer** is an automation workflow built using **n8n**, designed to:
- Fetch an article or text content
- Use **Gemini AI** to generate a concise, human-readable summary
- Store the summary automatically in a **Notion page** (or Google Docs)

This allows users to quickly generate clean summaries for research, newsletters, or knowledge bases — without copying and pasting text manually.

---

## 🧩 Workflow Components

| Step | Node | Description |
|------|------|--------------|
| 1️⃣ | **HTTP Request / Webhook** | Accepts article URL or raw text as input |
| 2️⃣ | **Gemini (Google AI)** | Processes the content and produces a summarized output |
| 3️⃣ | **Notion** | Creates or updates a Notion page with the article title and AI summary |
| 4️⃣ | *(Optional)* Google Docs / Drive | Can store summaries as `.docx` or `.pdf` files |

---

## 🧠 Example Setup in n8n

### 🧩 Notion Node Configuration
- **Parent Page:** Your Notion database or page link  
- **Title:**  
  ```js
  {{$json["title"] || "Article Summary"}}

## Flow:
  Step-1: Chat Trigger

  <img width="1488" height="399" alt="36E19A7E-80A2-413C-985C-36818638605C" src="https://github.com/user-attachments/assets/ae35b96c-c83d-4d48-ad69-923770cc233b" />

  step-2: Fetching

  ![A2E20647-6C7C-4C81-A96D-6939E6315CAB](https://github.com/user-attachments/assets/036d98f6-bf1f-4889-b9fd-f138af28a17b)

   Step-3: Summarizer

   <img width="2708" height="1229" alt="image" src="https://github.com/user-attachments/assets/2e48bba4-afb5-492f-bbaa-fc849ecc6f14" />

   Step-4: Notion

   ![171025D7-AF64-4C0B-8455-61654282B1EA](https://github.com/user-attachments/assets/503f7c29-ed18-401c-910a-8c1a54a4beb8)


   ## Future Insights:

Here are some powerful features you can add next:

📰 RSS Feed Integration
Automatically pull the latest news articles from BBC, Reuters, etc.

📧 Email Digest Delivery
Send summarized articles as daily or weekly newsletters.

🏷️ Topic Tagging
Use Gemini or OpenAI to generate tags like “Technology,” “Politics,” “Science.”

🔎 Auto Web Scraping
Fetch article text automatically using Cheerio or Mercury Parser node.

📄 Google Docs / Drive Sync
Export summaries to .docx or .pdf in your Drive.

📊 Analytics Dashboard
Track how many articles were summarized each week using Notion API or Google Sheets.

## 🧭 Workflow Diagram (Top-Down)


<img width="1024" height="1536" alt="ChatGPT Image Nov 1, 2025, 02_39_01 PM" src="https://github.com/user-attachments/assets/56d134d6-6d26-4fe2-a09f-6de4416c047d" />

## Conclusion:

This project successfully demonstrates how to automate article summarization using n8n integrated with Google Gemini and Notion.
By connecting these tools, we created a seamless workflow that:

Takes an article (via URL or text input)

Generates a concise summary using Gemini’s language model

Stores the output neatly in Notion for easy access and organization
