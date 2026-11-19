# VoxaOS — Cross-Platform Hands-Free AI Personal & Professional Assistant

## 1. Project Vision & Product Form
A complete **Hybrid AI Operating Assistant** (Mobile App + Desktop Software + Web Portal) inspired by Jarvis & Stonic AI. Designed for busy professionals (doctors, lawyers, freelancers, remote workers) and everyday users to operate their phones and computers completely hands-free via natural Urdu and English voice commands.

## 2. Enterprise Monorepo Architecture (ChatDukan Standard)
- `shared/` — Shared Zod schemas, voice intent definitions, prompt templates, i18n (EN/UR + RTL support), and API client contracts.
- `backend/` — **Node.js + Express 5**, PostgreSQL + `pgvector` (long-term AI memory), `pg-boss` background workers, and token/subscription billing.
- `supabase/` — Database schema migrations, strict user data isolation policies, and audit logs.
- `web-frontend/` — **Next.js (App Router)** + **Tailwind CSS** (Web control center, generated medical prescriptions/documents viewer, memory manager, and Admin panel).
- `mobile/` — **React Native (Expo) + NativeWind + Native Android Modules** (Background voice listener, screen wake-up, phone calls, WhatsApp/app launching).
- `desktop-agent/` — Lightweight **Tauri / Electron** system software for Windows & macOS (file organization, browser control, desktop app execution).

## 3. Specialized Tools & Capabilities to Include
- **Wake-Word & Screen Wake Engine:** Porcupine (Picovoice) wake-word detection ("Hey Voxa") + Android Accessibility & Intent APIs to wake locked screens and navigate apps hands-free.
- **Ultra-Fast Voice Pipeline:** Deepgram Nova-2 / OpenAI Whisper (multilingual Urdu + English Speech-to-Text) -> Anthropic Claude API (Tool/Function Calling) -> ElevenLabs / OpenAI Realtime TTS.
- **Doctor / Telemedicine Mode:** Listens to patient consultations (with consent), extracts symptoms, and auto-generates formatted PDF/WhatsApp prescriptions and patient records.
- **Office & File Automation Mode:** Drafts emails, summarizes documents, and organizes desktop folders automatically via voice commands.
- **Cross-Device Remote Bridge:** Secure WebSocket bridge allowing users to speak into their mobile phone to control their office laptop/PC remotely.
- **Enterprise Security & Compliance:** End-to-end Envelope Encryption for medical/professional records, HIPAA-ready privacy retention rules, Gitleaks, and CodeQL CI checks.

## 4. What NOT to Include (Strict Guardrails)
- **No Unconfirmed Destructive Actions:** The AI must NEVER delete files, send payments, or dispatch external messages/emails without a quick voice or tap confirmation.
- **No Heavy Local AI Models on Client Devices:** Keep mobile and desktop apps lightweight by running heavy AI inference in the cloud so devices do not overheat or lag.
