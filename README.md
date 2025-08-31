
# 🍳 AI-Powered Voice-Controlled Cooking Assistant

## 📌 Overview
The **Voice-Controlled Cooking Assistant** is a hands-free web/mobile application that helps users follow recipes step-by-step using **voice commands**.  
It eliminates the hassle of touching devices while cooking, providing an intuitive and interactive kitchen companion.

---

## 🚀 Features
- 🎙 **Voice Commands**: Navigate through recipes using commands like *"Next step"*, *"Repeat"*, *"Pause"*  
- 🔊 **Text-to-Speech**: Recipes read out loud with timers  
- ⏱ **Automatic Timers**: Set reminders for cooking steps  
- 🥗 **Personalization**: Choose preferences (Veg/Non-Veg, dietary needs)  
- 🌍 **Multi-language Support** (Future scope)  
- 🤖 **AI Integration** (Future scope): Ingredient substitution, nutrition info, Q&A  
- 📡 **Recipe Source**: TheMealDB API / Kaggle datasets  

---

## 🛠️ Tech Stack
- **Frontend:** HTML, CSS, JavaScript (React optional), Web Speech API  
- **Backend:** Node.js (Express) / Python Flask  
- **Database:** MongoDB Atlas (optional for preferences & history)  
- **API:** [TheMealDB](https://www.themealdb.com/)  
- **AI (Future):** OpenAI API / Hugging Face models  
- **Deployment:** Vercel / Netlify (Frontend), Render / Heroku (Backend)  

---

## 📂 Project Structure (Planned)
Voice-Cooking-Assistant/
│── frontend/           # React/HTML frontend with voice interface
│── backend/            # Node.js/Python backend APIs
│── database/           # MongoDB setup (optional)
│── docs/               # Documentation, reports, diagrams
│── README.md           # Project documentation

## PROJECT PLANNING
🗺️ Product Scope (Pages & Modules)

Frontend Pages (A leads)
	1.	Onboarding / Permissions (micro page)
	2.	Home (search bar, mic button, recent recipes)
	3.	Search Results (filters: cuisine, diet, time)
	4.	Recipe Details (ingredients, steps, nutrition, “Start Cooking”)
	5.	Cooking Mode (step-by-step, large controls, TTS, voice hints)
	6.	Timers Panel (active timers, add/cancel)
	7.	Substitutions Panel (AI suggestions)
	8.	Preferences (language, dietary, units, TTS speed/voice)
	9.	Saved/History (recently cooked, favorites)
	10.	Offline Downloads (toggle “make available offline”)

Backend (B leads)
	•	/recipes/search (q, filters) → cached from TheMealDB
	•	/recipes/{id} (normalized schema)
	•	/users (optional JWT later), /prefs
	•	/ai/substitutions (proxy to rule-based/LLM later)
	•	/nutrition/estimate (basic rule set or API)
	•	/telemetry (events: start_step, next, timer_set)

AI/Voice (C leads)
	•	Voice pipeline (Web Speech API) + fallback to server STT (future).
	•	Command parser (intent + slot extraction).
	•	i18n (English first; add Hindi later).
	•	AI: rule-based substitutions baseline; nutrition heuristics; LLM hook (future).

QA/DevOps (D leads)
	•	Test plan (unit, integration, E2E with Playwright/Cypress).
	•	Accessibility (WCAG AA checklist), Lighthouse budgets.
	•	Versioned docs: /docs/architecture.md, /docs/api.md, /docs/voice-grammar.md.
	•	Release process + demo script.
