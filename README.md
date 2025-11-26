MailGenius – Prompt-Driven Email Productivity Agent

MailGenius is a fully prompt-controlled email processing system built using Next.js, TypeScript, Tailwind CSS, shadcn/ui, and OpenAI.
It can ingest inbox emails, categorize them, extract action items, generate reply drafts, and offer an AI-powered chat interface — all powered by user-defined prompts.

🚀 Features

Load mock inbox (or Gmail integration if enabled)
Auto-categorize emails (Important / To-Do / Spam / Newsletter)
Extract action items using LLM
Auto-generate reply drafts
Full Prompt Brain — edit categorization, summary, extraction, and reply prompts
AI Email Agent Chat (summaries, replies, urgent filters, questions)
Safe Drafts — emails are never sent automatically
Clean UI with modular architecture
Clear API layer for backend operations

📦 mailgenius

 ┣ 📁 app
 
 ┃ ┣ 📁 api
 
 ┃ ┃ ┣ 📁 emails         → GET inbox data
 
 ┃ ┃ ┣ 📁 prompts        → GET/POST/PUT prompt configs
 
 ┃ ┃ ┣ 📁 process-email  → LLM categorization & extraction
 
 ┃ ┃ ┣ 📁 chat           → LLM-powered chat
 
 ┃ ┃ ┗ 📁 drafts         → Safe draft storage
 
 ┃ ┣ layout.tsx          → Global layout, theme, metadata
 
 ┃ ┗ page.tsx            → Main UI (Inbox + Prompts + Agent Chat)
 
 ┣ 📁 components
 
 ┃ ┣ inbox.tsx
 
 ┃ ┣ email-list.tsx
 
 ┃ ┣ email-detail.tsx
 
 ┃ ┣ prompt-configurator.tsx
 
 ┃ ┣ prompt-editor.tsx
 
 ┃ ┣ email-agent.tsx
 
 ┃ ┗ email-composer.tsx
 
 ┣ 📁 hooks
 
 ┃ ┗ use-init-data.ts    → Loads mock inbox + prompts
 
 ┣ 📄 SETUP_GUIDE.md
 
 ┣ 📄 PROJECT_SUMMARY.md
 
 ┣ 📄 COMPLETION_SUMMARY.md
 
 ┗ 📄 README.md


How the System Works
1. Inbox Ingestion

Loads mock inbox JSON with sample emails

Runs LLM to categorize and extract action items

Displays sender, subject, timestamp, tag, summary, actions, and draft

2. Prompt-Driven Architecture

All behaviors are controlled by prompts:

Categorization

Action item extraction

Summaries

Auto-draft replies

Users can edit prompts any time.

3. Email Agent Chat

Ask the system:

“Summarize this email”

“Draft a reply”

“What tasks do I need to do?”

“Is this email important?”

4. Safe Draft Workflow

Replies are stored as drafts

No email is ever sent automatically

🛠 Tech Stack

Frontend: Next.js (App Router), TypeScript, Tailwind CSS, shadcn/ui

Backend/API: Next.js API routes, OpenAI SDK, JSON storage

AI: OpenAI LLM for processing emails and chat responses
