# Ecom360_Project_FYP-Showcase
A complete visual showcase of the ecom360 platform, featuring a live demo link and application screenshots. https://ecom360-official.vercel.app/

# Ecom360 - AI-Powered E-Commerce Intelligence Suite 🚀

**1-Line Description:** Ecom360 is a comprehensive, multi-platform, AI-driven e-commerce assistance tool tailored for Pakistani sellers (Shopify, Daraz) to optimize operations through real-time data scraping, machine learning-based sales forecasting, SEO content generation, and strategic marketing intelligence.

---

## 📖 Project Overview
The e-commerce landscape in Pakistan is growing rapidly, but many local sellers lack access to localized, data-driven intelligence. Ecom360 solves this problem by centralizing critical business tools into a single, intuitive web application. Built with a robust decoupled architecture, it uses React (TypeScript/TSX) for a dynamic frontend and Python FastAPI for a high-performance backend. 

## ✨ Features

* **Sales & Revenue Predictor:** Analyzes live product metrics (price, ratings, reviews) scraped via BeautifulSoup and feeds them into a custom Scikit-Learn Linear Regression model to forecast monthly sales units and estimated revenue.

* **SEO Content Generator:** Integrates directly with the Google Gemini API to instantly generate high-converting, SEO-optimized product titles and descriptions based on user-provided features.

* **Global Supplier Finder:** Allows sellers to search for suppliers dynamically (e.g., via Alibaba links) or submit direct Concierge Sourcing Requests to the platform's administrative team.

* **AI Marketing Strategist:** Users input their budget, target audience, and goals, and the Gemini API generates a comprehensive, markdown-formatted, budget-aware marketing strategy tailored to the local landscape.

* **Profit Calculator:** A real-time client-side financial simulation engine that calculates net profit margins, ROI, and break-even points by factoring in COGS, shipping, marketing CPA, and miscellaneous taxes.

* **Role-Based Admin Portal:** A highly secure backend portal restricted via JWT authentication. Admins can manage the global product catalog, review user sourcing requests, and reply directly to user support tickets.

* **User Workspace:** Users can manage their profiles, save favorite products for quick access, view their historical search analysis, and receive direct replies from admins regarding support queries.

---

##  Technology Stack

**Frontend (Client-Side):**
* **Framework:** React.js
* **Language:** TypeScript (TSX)
* **Build Tool:** Vite
* **Styling:** Tailwind CSS (for responsive UI)

**Backend (Server-Side):**
* **Language:** Python 3.x
* **Framework:** FastAPI
* **Database:** PostgreSQL
* **ORM:** SQLAlchemy & SQLModel
* **Authentication:** Passlib & Python-Jose (JWT)

**AI & Data Acquisition:**
* **Machine Learning:** Scikit-Learn, Pandas (Linear Regression)
* **Web Scraping:** BeautifulSoup4
* **Generative AI:** Google Gemini API

---

##  Installation & Setup Guide (A to Z)

This project uses a decoupled architecture. You must configure and run both the backend server and the frontend development server simultaneously.

### Prerequisites
* Node.js (v16+ recommended)
* Python (v3.9+ recommended)
* PostgreSQL (Running locally or via a cloud provider)
* Git

### Clone the Repository & Run commands
Open your terminal and clone the project:
```bash
Step 1:

git clone [https://github.com/your-username/Ecom360_FYP.git](https://github.com/your-username/Ecom360_FYP.git)
cd Ecom360_FYP

Step 2: Backend Setup & Execution

cd backend

In Wondow:
python -m venv venv
venv\Scripts\activate
Mac/Linux:
python3 -m venv venv
source venv/bin/activate

pip install -r requirements.txt
# Database Connection String
DATABASE_URL=postgresql://postgres:your_db_password@localhost:5432/ecom360db
# Security & Authentication
SECRET_KEY=generate_a_strong_random_string_here
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=1440
# Third-Party APIs
GEMINI_API_KEY=your_actual_gemini_api_key_here
uvicorn main:app --reload
http://localhost:8000
You can access the automatic API documentation (Swagger UI) at: http://localhost:8000/docs

Step 3: Frontend Setup & Execution

cd frontend
npm install
VITE_API_URL=http://localhost:8000
npm run dev
