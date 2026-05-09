# TrustLocal: AI-Powered Hyperlocal Commerce Platform 🏪

![TrustLocal Header](https://images.unsplash.com/photo-1542838132-92c53300491e?auto=format&fit=crop&w=1200&h=400&q=80)

TrustLocal is a modern, AI-powered hyperlocal marketplace designed to connect consumers directly with trusted nearby businesses. By leveraging real-time geolocation, AI trust scoring, and direct shop-to-customer interactions, TrustLocal aims to empower neighborhood economies and eliminate the dependency on centralized warehouse delivery apps.

---

## 🛑 The Problem
Modern quick-commerce platforms rely heavily on centralized "dark stores" and warehouse delivery models. This system:
- Destroys local neighborhood economies by bypassing local shopkeepers.
- Suffers from fake reviews and artificially inflated ratings.
- Increases delivery times and costs for goods that are often available just streets away.
- Deprives customers of direct, trustworthy relationships with local merchants.

## 💡 The Solution
TrustLocal flips the model by empowering existing neighborhood stores:
- **Direct Hyperlocal Connection**: Order directly from shops within a small radius (e.g., your neighborhood) ensuring ultra-fast delivery.
- **AI Trust Engine**: Uses AI to analyze shop behavior, order fulfillment rates, and community feedback to assign a real-time, tamper-proof "Trust Score".
- **TrustBot AI**: An integrated AI assistant (powered by Google Gemini) that helps users find the best, most trusted shops for specific needs nearby.
- **Keep Wealth Local**: Every transaction helps local neighborhood entrepreneurs thrive against corporate monopolies.

---

## ✨ Features

### 🛒 For Customers
- **Real-Time Geolocation**: Automatically detects your location and shows verified shops nearby on an interactive map.
- **TrustBot AI Assistant**: Chat with an AI to find the best pharmacies, groceries, or repair shops in your vicinity based on real-time data and trust scores.
- **Live Marketplace Dashboard**: Browse categories, view live inventory, and simulate secure checkouts.
- **Verified Trust Scores**: See exactly how reliable a shop is before purchasing.

### 🏪 For Sellers (Shopkeepers)
- **Instant Digital Storefront**: Create a shop profile, capture exact GPS coordinates, and go live instantly.
- **Seller Dashboard**: Manage inventory, track live orders, and monitor your shop's performance via a beautiful, responsive UI.
- **AI Business Insights**: Receive automated AI suggestions on peak hours, low stock alerts, and revenue trends.
- **Real-Time Map Visibility**: View your shop's exact location on the map to ensure customers can find you.

---

## 🛠️ Tech Stack

### Frontend (Client)
- **Framework**: React 18 with Vite
- **Styling**: Tailwind CSS & Vanilla CSS (for custom utility classes)
- **Animations**: Framer Motion
- **Routing**: React Router DOM
- **State Management**: Zustand
- **Maps & Geolocation**: React Leaflet & Browser Geolocation API
- **Icons**: Lucide React

### Backend (Server)
- **Runtime**: Node.js & Express.js
- **Database**: MongoDB Atlas (with Mongoose ODM)
- **Authentication**: JWT (JSON Web Tokens) & bcrypt.js
- **AI Integration**: Google GenAI SDK (Gemini Flash Models)
- **Real-Time**: Socket.io (Configured for future live order tracking)

---

## 📂 Project Structure

```text
Hyperlocal-1-main/
│
├── client/                     # React Frontend
│   ├── public/                 # Static assets
│   ├── src/
│   │   ├── components/         # Reusable UI components (TrustBot, ui/, etc.)
│   │   ├── lib/                # API configurations (Axios)
│   │   ├── pages/              # Main application views (Auth, Dashboards, Landing)
│   │   ├── store/              # Zustand state management
│   │   ├── App.tsx             # Main React component & Routing
│   │   └── index.css           # Global styles and Tailwind configuration
│   ├── package.json
│   └── vite.config.ts
│
└── server/                     # Node.js Backend
    ├── src/
    │   ├── controllers/        # Business logic (Auth, Chat/AI)
    │   ├── models/             # Mongoose database schemas (User, Shop, Order)
    │   ├── routes/             # Express API routes
    │   ├── middleware/         # Custom middleware (Auth guarding)
    │   └── index.ts            # Entry point for the Express server
    ├── .env                    # Environment variables (ignored in Git)
    └── package.json
```

---

## 🚀 Getting Started (Local Development)

### Prerequisites
- Node.js (v18+)
- MongoDB Atlas Account (or local MongoDB instance)
- Google Gemini API Key

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/hyperlocal-platform.git
cd hyperlocal-platform
```

### 2. Backend Setup (`/server`)
```bash
cd server
npm install
```
Create a `.env` file in the `/server` directory:
```env
PORT=5000
MONGO_URI=mongodb+srv://<your_db_user>:<your_password>@cluster0...
JWT_SECRET=your_super_secret_jwt_key
GEMINI_API_KEY=your_google_gemini_api_key
CLIENT_URL=http://localhost:5173
NODE_ENV=development
```
Run the backend server:
```bash
npm run dev
```

### 3. Frontend Setup (`/client`)
```bash
cd ../client
npm install
```
Create a `.env` file in the `/client` directory:
```env
VITE_API_URL=http://localhost:5000/api
```
Run the frontend development server:
```bash
npm run dev
```

The application will now be running on `http://localhost:5173`.

---

## 🌐 Deployment Guidelines

The project is structured to be deployed independently to modern cloud providers:

- **Frontend (Vercel)**: Simply connect your GitHub repository to Vercel, set the root directory to `client`, and add the `VITE_API_URL` environment variable pointing to your live backend.
- **Backend (Render / Railway)**: Connect the repository, set the root directory to `server`, configure your Start Command (`npm start`), and add all necessary environment variables (`MONGO_URI`, `GEMINI_API_KEY`, etc.). Ensure `CLIENT_URL` is set to your live Vercel domain to prevent CORS issues.

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## 📝 License
This project is built for the Future. Copyright © 2026 TrustLocal Technologies.
