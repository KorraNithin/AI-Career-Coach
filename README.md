# 🚀 AI Career Coach

[![Next.js](https://img.shields.io/badge/built%20with-Next.js-black?logo=next.js)](https://nextjs.org/)
[![Tailwind CSS](https://img.shields.io/badge/styled%20with-TailwindCSS-blue?logo=tailwindcss)](https://tailwindcss.com/)
[![Prisma](https://img.shields.io/badge/database-Prisma%20%2B%20PostgreSQL-blueviolet?logo=prisma)](https://www.prisma.io/)
[![Gemini](https://img.shields.io/badge/powered%20by-Gemini%20AI-red?logo=google)](https://deepmind.google/technologies/gemini/)
[![License: MIT](https://img.shields.io/badge/license-MIT-yellow.svg)](LICENSE)

---

## 💡 Project Overview

**AI Career Coach** is a full-stack web app I built that empowers job seekers with AI-assisted tools for:
- ✍️ Resume building
- 📄 Cover letter generation
- 🎙 Mock interview practice

Built with **Next.js 15**, **React 19**, **Tailwind CSS**, and integrated with the **Gemini API**, this app helps users create professional documents and prep with confidence.

> 🔗 **Live Demo**: https://ai-career-coach-gamma-woad.vercel.app/

---

## ⚙️ Tech Stack

| Layer        | Tech Used                                                                 |
|--------------|---------------------------------------------------------------------------|
| Frontend     | React 19, Next.js App Router, Tailwind CSS, Shadcn UI                     |
| Backend      | Next.js Server Actions, Inngest (for async workflows)                     |
| Database     | Prisma ORM, PostgreSQL                                                    |
| Auth         | Clerk Authentication                                                      |
| AI Services  | Gemini API (for Resume, Cover Letter, Interview answers)                  |
| Deployment   | Vercel (CI/CD, environment management)                                    |

---

## ✨ Features

- 🔐 Clerk Auth + Protected Routes
- 📝 AI Resume & Cover Letter Builder (Gemini API)
- 🎯 Mock Interview Assistant with LLM-powered questions and answers
- 🧠 Role-based content (dashboard, onboarding)
- 💅 Fully responsive UI with Tailwind & Shadcn
- 📦 Scalable file structure using Next.js App Router
- 🔁 Background jobs via Inngest for async processing

---

## 🚀 Local Setup

> Make sure you have **Node.js ≥ 18**, **npm**, and a **PostgreSQL** database (e.g. via [Supabase](https://supabase.com)) ready.

### 1. Clone the repo

```bash
git clone https://github.com/<your-username>/ai-career-coach.git
cd ai-career-coach
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Copy `.env.example` to `.env` and fill in your own values:

```bash
cp .env.example .env
```

```ini
DATABASE_URL="postgresql://user:password@host:5432/dbname"
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="pk_test_xxxxxxxx"
CLERK_SECRET_KEY="sk_test_xxxxxxxx"
GEMINI_API_KEY="your_gemini_api_key"
```

Get your keys from [Supabase](https://supabase.com), [Clerk](https://clerk.com), and [Google AI Studio](https://aistudio.google.com/apikey).

### 4. Set up the database

```bash
npx prisma migrate dev
```

### 5. Start the development server

```bash
npm run dev
```

Visit `http://localhost:3000`.

---

## 📁 Folder Structure (Highlights)

```
/app                 → Next.js App Router structure
/actions             → Server actions (cover letter, resume, interview, dashboard)
/components          → UI and shared components
/prisma              → DB schema and migrations
/lib                 → Helpers, Prisma config, Inngest functions
/public              → Static assets
/hooks, /data        → Custom hooks and static data
```

---

## 🧠 AI-Powered Features

Powered by the Google Gemini API:
- Cover letters generated from role, company, and job description
- Custom resume content generation and improvement
- Mock interview questions with instant feedback and explanations
- Weekly industry insights (salary ranges, demand, trends) via a scheduled background job

---

## 📄 License

This project is licensed under the MIT License.