![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js\&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4ea94b?logo=mongodb\&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis\&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-Deployed-black?logo=vercel)

# 🧠 Mini CRM

A full-stack CRM platform designed to empower marketing teams with smart campaign management, team collaboration, customer insights, and AI-powered business intelligence.

---

## ✨ Key Features

* Customer & order management with automatic stats
* Campaign builder with real-time audience preview
* AI-powered segmentation and messaging
* Team roles using **Role-Based Access (RBA)**
* Business owner can invite **managers, analysts, viewers**
* Message delivery via **SMTP** & **WhatsApp**
* Business growth **insight generator** using **Google Gemini AI**
* Secure, scalable authentication using **HTTP-only cookies + Redis session store**
* Fully responsive, modern UI with Tailwind CSS

---

## 📸 Screenshots

![image](https://github.com/user-attachments/assets/f0335666-55d8-45ec-ad39-97aa57293e5a)
![image](https://github.com/user-attachments/assets/1d5fa81b-f312-4131-b788-ddb15a5a45e9)
![image](https://github.com/user-attachments/assets/71710727-a45b-4690-be5e-9a436d2cbb7a)

---

## 🚀 Core Modules

### 👥 Customer Management

* Add, update, and view customer profiles
* Tracks `totalSpend`, `totalOrders`, `lastOrderDate` automatically

### 🛒 Order Management

* Orders linked to customers
* Auto-updates related customer stats instantly

### 📣 Campaign Builder

* Input campaign name, message, and segmentation rules
* Uses **Google Gemini AI** to:

  * Convert natural language → MongoDB query
  * Suggest short, engaging messaging

### 👁️ Audience Preview

* Real-time filtered list of customers matching rules

### ✉️ Messaging Delivery

* Supports:

  * **📧 Email** (SMTP)
  * **📱 WhatsApp API**
* Logs everything:

  * Message status (SENT/FAILED)
  * Vendor response
  * Timestamp

### 📊 Campaign History & Logs

* Full log history for each campaign
* Transparency for debugging and delivery monitoring

### 📈 Business Insights

* Route: `/reports`
* AI-powered business improvement tips via:

  * `/api/dashboard/insights`
* Helps improve conversions and retention

### 🔐 Authentication

* **Google OAuth 2.0** (Passport.js)
* **HTTP-only cookies**

  * Safer against XSS
  * Fully managed server-side
* **Redis session store**

  * Faster
  * Scalable
* Role-based access protection
* Frontend route protection using Context API

---

## 🧑‍🤝‍🧑 Role-Based Access (RBA)

Now includes team roles:

* 👑 **Owner** — full control, invites members
* 🔧 **Manager** — can manage customers, orders, and campaigns
* 👁️ **Viewer** — read-only dashboard and analytics

### Access is controlled at:

* Backend middleware
* Session validation
* Frontend routing
* UI visibility rules

---

## 💡 AI-Powered Tools (Google Gemini)

| Feature                   | Description                          |
| ------------------------- | ------------------------------------ |
| Prompt → Mongo filter     | Converts natural rules to DB queries |
| Segment goal → Message    | Suggests strong marketing messages   |
| Dashboard Tips & Insights | Personalized business intelligence   |

---

## ✅ Feature Checklist

| Feature                              | Status |
| ------------------------------------ | ------ |
| Customer ingestion                   | ✅      |
| Order ingestion + stats update       | ✅      |
| Campaign creation + audience preview | ✅      |
| SMTP email delivery                  | ✅      |
| WhatsApp message integration         | ✅      |
| Per-campaign delivery logs           | ✅      |
| AI prompt → MongoDB query            | ✅      |
| AI message generator                 | ✅      |
| AI-powered growth tips               | ✅      |
| Google OAuth 2.0 login               | ✅      |
| Redis-based session storage          | ✅      |
| HTTP-only cookie authentication      | ✅      |
| Role-Based Access (RBA)              | ✅      |
| Team member invitations              | ✅      |
| Responsive Tailwind UI               | ✅      |
| Dashboard overview with stats        | ✅      |

---

## 🧪 Technologies Used

| Layer       | Stack                                    |
| ----------- | ---------------------------------------- |
| Frontend    | React (Vite), Tailwind CSS, React Router |
| Backend     | Node.js, Express, Mongoose (MongoDB)     |
| AI Services | Google Gemini AI                         |
| Messaging   | Nodemailer (SMTP), WhatsApp API          |
| Auth        | Google OAuth 2.0, Passport.js, JWT       |
| State Mgmt  | React Context API                        |
| Session     | Redis + connect-redis                    |
| UX Tools    | Toastify, Lucide Icons                   |

---

## 🗂️ Folder Structure

```
/backend
├── config/        
├── controllers/
├── models/
├── routes/
├── middleware/
├── services/      
└── server.js

/frontend
├── pages/
├── components/
├── routes/
├── context/
├── api/
└── App.jsx / main.jsx
```

---

## 🧑‍💻 Local Setup

### 🔧 Backend

```bash
cd backend
npm install
npm run dev
```

`.env` configuration:

```env
PORT=5000
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
CLIENT_URL=http://localhost:5173

# Redis
REDIS_URL=redis://localhost:6379

# Google AI
GOOGLE_GEMINI_API_KEY=your_gemini_key

# Google OAuth
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_secret

# SMTP
SMTP_HOST=smtp.example.com
SMTP_PORT=587
SMTP_USER=email@example.com
SMTP_PASS=your_password

# WhatsApp API
WHATSAPP_API_URL=https://api.example.com/send
WHATSAPP_API_KEY=your_key
```

---

### 💻 Frontend

```bash
cd frontend
npm install
npm run dev
```

Access frontend at:
➡️ [http://localhost:5173](http://localhost:5173)

---

## 👨‍💻 Author

**Ayush Rajput**


---

## 📝 License

Open-source project for learning and portfolio demonstration.


