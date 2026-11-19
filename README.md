# VoxaOS — Hands-Free AI Personal & Professional Assistant

## 1. Project Vision & Core Concept
A cross-platform (Mobile & Desktop) **Voice-Controlled AI Operating Assistant** (inspired by Jarvis & Stonic AI). Built specifically for busy professionals (doctors, lawyers, freelancers, remote workers) and everyday users to operate their phones and computers completely hands-free using natural voice commands in Urdu, English, and global languages.

## 2. Monorepo Architecture (Enterprise Standard)
- `shared/` — Shared TypeScript types, voice intent schemas, prompt templates, i18n (EN/UR + RTL), and API client SDK.
- `backend/` — Node.js + **Express 5**, PostgreSQL, persistent vector/relational user memory engine, LLM orchestration, and subscription/token billing.
- `web-frontend/` — **Next.js (App Router)** + **Tailwind CSS** (User web dashboard, generated prescriptions/documents viewer, memory manager, and Admin panel).
- `mobile-app/` — **React Native (Expo) + Native Android Modules** (Wake-word detection, screen wake-up, phone calls, WhatsApp/app launching, and voice overlay).
- `desktop-agent/` — Lightweight **Electron / Tauri** background client for Windows & macOS system control (file organization, browser navigation, app execution).

## 3. Core Capabilities & Professional Modes
- **Hands-Free Device Control:** Custom wake-word ("Hey Voxa") wakes up locked phone screens, opens apps, navigates URLs, dials calls, and sends WhatsApp/email messages via voice.
- **Doctor / Telemedicine Mode:** Listens to doctor-patient online consultations (with consent), extracts symptoms, and auto-generates formatted digital prescriptions (PDF/WhatsApp ready) and patient history logs without manual typing.
- **Office & Freelancer Mode:** Drafts emails, summarizes long documents, manages calendars/reminders, and organizes messy desktop files into categorized folders on voice command.
- **Cross-Device Bridge:** Allows the user to speak into their mobile phone to control their office laptop/PC remotely.
- **Persistent Context & Memory:** Remembers user routines, frequent contacts, preferred templates, and past instructions.

## 4. What NOT to Include (Strict Guardrails)
- **No Unconfirmed Destructive Actions:** The AI must NEVER delete files, send financial transactions, or send external emails/messages without a quick voice or tap confirmation.
- **No Heavy Local LLM Bloat:** Keep client apps lightweight; run heavy AI reasoning and speech processing via low-latency cloud APIs so older phones and laptops do not lag.

## 5. Recommended Tools & Integrations
- **Backend & DB:** Node.js, Express 5, PostgreSQL + pgvector (for long-term AI memory).
- **Frontend & Mobile:** Next.js, Tailwind CSS, React Native (Expo) with Android Accessibility & Intent APIs.
- **Voice & AI Pipeline:** Deepgram / OpenAI Whisper (fast Urdu + English Speech-to-Text), Anthropic Claude API (Tool/Function Calling), ElevenLabs / OpenAI TTS (natural voice response).
- **Payments & Auth:** OAuth (Google/Apple), Stripe + Local Payment Gateways, End-to-End Encryption for medical/professional records.
