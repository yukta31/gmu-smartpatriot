# GMU SmartPatriot — AI-Powered University Knowledge Engine

An AI-powered chatbot for George Mason University students, built with a RAG (Retrieval-Augmented Generation) pipeline. Aggregates 200+ GMU web pages via web scraping and uses Groq's LLaMA 3.1 to answer campus questions with grounded, accurate responses.

🌐 **Live:** [gmu-smartpatriot-4ozcrv5ss-yukta-s-projects.vercel.app](https://gmu-smartpatriot-4ozcrv5ss-yukta-s-projects.vercel.app)

---

## 🤖 What It Does

Students ask questions about GMU — registration deadlines, housing, dining, financial aid, IT support — and get accurate answers grounded in real GMU web content, not hallucinated responses.

**Without RAG:** LLM guesses → wrong answers about specific GMU policies  
**With RAG:** LLM reads actual GMU pages → accurate, sourced answers

---

## 🏗️ Architecture

```
User Question
     ↓
Cheerio Web Scraper → 200+ GMU pages indexed
     ↓
Semantic Retrieval → find relevant content chunks
     ↓
Groq LLaMA 3.1 → generate grounded response
     ↓
Multi-turn Memory (5-7 turns) → context continuity
     ↓
Response < 2 seconds
```

---

## ✨ Features

- **RAG Pipeline** — answers grounded in real GMU web content
- **200+ pages indexed** — academic calendar, housing, dining, financial aid, IT support
- **Multi-turn conversation memory** — maintains context across 5–7 turns
- **< 2 second response latency** — serverless deployment on Vercel
- **Web scraping** — Cheerio parses and structures GMU page content

---

## 🔧 Tech Stack

| Category | Tools |
|----------|-------|
| Framework | Next.js + TypeScript |
| AI Model | Groq API (llama-3.1) |
| Web Scraping | Cheerio |
| Deployment | Vercel (serverless) |
| Runtime | Node.js |

---

## 🚀 How to Run

```bash
git clone https://github.com/yukta31/gmu-smartpatriot.git
cd gmu-smartpatriot
npm install
```

Add environment variables in `.env.local`:
```
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key  # optional, for web search
```

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000)

Get a free Groq API key at [console.groq.com](https://console.groq.com)

---

## 📖 Technical Deep Dive

Read the full technical writeup on how this was built:  
[How I Built an AI Knowledge Engine for My University Using RAG](https://dev.to/yukta31/how-i-built-an-ai-knowledge-engine-for-my-university-using-rag-5a74)

---

## 👩‍💻 Author

**Yukta Batra** — MS Computer Science, George Mason University

[Portfolio](https://yukta-batra.vercel.app) · [LinkedIn](https://linkedin.com/in/yuktabatra31) · [GitHub](https://github.com/yukta31)
