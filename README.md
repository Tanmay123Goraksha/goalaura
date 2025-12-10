# GoalAura 🌟
### *GenAI-Powered Financial Dream Architect*

**GoalAura** is a cross-platform financial wellness application that bridges the gap between abstract life dreams and financial reality. Unlike traditional budgeting apps, it uses a **Multi-Agent GenAI System** to "reverse-engineer" user goals (e.g., "buy a cafe in Mumbai") into brutally honest, actionable financial roadmaps.

---

## 🚀 Key Features

* **🧠 Dream Mapping Studio**: Users describe dreams in natural language. The AI acts as a "Financial Architect," breaking them down into 10-step execution plans with real-time market cost estimation.
* **⚖️ Reality Check Engine**: A logic-driven "Feasibility Score" analyzes user income vs. goal costs. It provides "brutally honest" feedback—telling users if a goal is unrealistic and suggesting concrete "Income Growth" strategies or alternatives.
* **💸 Opportunity Cost Visualizer**: An AI agent that contextualizes impulse purchases (e.g., "This ₹5,000 purchase costs you 40 hours of work or ₹12,000 in future investment value").
* **📱 Cross-Platform Ecosystem**: A unified experience across **Web (React)** and **Mobile (Flutter)**, allowing users to track goals and milestones on any device.

---

## 🛠️ Tech Stack

### **Frontend**
* **Web**: React.js + Vite, Tailwind CSS (Responsive Dream Map visualization)
* **Mobile**: Flutter (Dart) for Android/iOS

### **Backend & AI**
* **Primary Backend**: Node.js + Express (User Auth, Goal Management)
* **AI Microservice**: Python + FastAPI (Agent Orchestration)
* **Models**: Google Gemini 2.0 Flash / Pro (via `google-genai` SDK)
* **Database**: MongoDB (Complex Schemas for User Goals & Milestones)

---

## 📂 Project Architecture

The system uses a **Dual-Backend Architecture**:
1.  **Node.js Server**: Handles traditional CRUD operations (Users, Transactions, Saved Goals).
2.  **Python AI Agent**: Stateless microservice that performs heavy-lifting logic (Cost Estimation, Feasibility Analysis) using Gemini.

```text
GoalAura/
├── agents/            # Python/FastAPI AI Microservices
│   └── dreammap_test/ # Core Logic for Dream Mapping & Opportunity Cost
├── client/            # React + Vite Web Dashboard
├── mobile_application/# Flutter Mobile App
└── server/            # Node.js + Express REST API
```

⚡ Getting Started
Prerequisites
Node.js (v18+) & npm

Python (v3.10+) & pip

Flutter SDK

MongoDB Instance

Google Gemini API Key

1. Setup AI Microservice (Python)
The intelligence engine must be running for roadmap generation.

Bash

cd agents/dreammap_test
pip install -r requirements.txt
# Create a .env file with: GEMINI_API_KEY=your_key_here
uvicorn app.main:app --reload --port 8000
2. Setup Primary Backend (Node.js)
Handles user data and persistence.

Bash

cd server
npm install
# Create a .env file with: MONGO_URI=your_db_url, PORT=3000
npm start
3. Run Web Client (React)
Bash

cd client
npm install
npm run dev
4. Run Mobile App (Flutter)
Bash

cd mobile_application/goalaura
flutter pub get
flutter run
🛡️ License
This project was developed for Mumbai Hacks. Code is available for educational purposes.
