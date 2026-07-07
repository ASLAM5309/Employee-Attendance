# Employee Attendance & Management System

A highly professional, full-stack enterprise web application designed for tracking employee attendance, managing employee profiles, and visualizing organizational analytics. Built with **React 19**, **Express**, **TypeScript**, **PostgreSQL**, and **Drizzle ORM**, this system provides a secure, intuitive experience for administrators and employees.

---
# 📸 Application Screenshots

## 🏠 Dashboard

<p align="center">
  <img src="https://plain-apac-prod-public.komododecks.com/202607/07/G7xJx2BszGJFOUcYtiJP/image.png" alt="Dashboard" width="100%">
</p>

---

## 👥 Employee Management

<p align="center">
  <img src="https://plain-apac-prod-public.komododecks.com/202607/07/sWXgZfntOC7Zo7TZtvw3/image.png" alt="Employee Management" width="100%">
</p>

---

## 📅 Attendance Management

<p align="center">
  <img src="https://plain-apac-prod-public.komododecks.com/202607/07/hOBWYzWoatsGBEoQM7Q7/image.png" alt="Attendance Management" width="100%">
</p>

---

## 📊 Reports

<p align="center">
  <img src="https://plain-apac-prod-public.komododecks.com/202607/07/5BhFhjSCtG1FnUfZVtif/image.png" alt="Reports" width="100%">
</p>

---

## ⚙️ Settings

<p align="center">
  <img src="https://plain-apac-prod-public.komododecks.com/202607/07/8bbMvgOAH3cOz2LItmqx/image.png" alt="Settings" width="100%">
</p>

## 🚀 Key Features

*   **Executive Dashboard & Analytics**: High-fidelity, real-time reporting showing daily attendance status, departmental ratios, monthly active averages, and custom charts using `recharts`.
*   **Employee Profiles Directory**: Comprehensive employee directory featuring structured profile management, department assignments, quick contact data, search filters, and profile editing.
*   **Real-time Attendance Tracking**: Immediate manual check-in/check-out controls for employees, supporting statuses such as *Present*, *Absent*, *Late*, and *Leave*.
*   **Bulk Attendance Submission**: Rapid-fire daily roster sheet allowing admins to mark attendance for the entire workforce on any selected calendar date with a single click.
*   **Admin Authentication**: Secure JWT-based admin access featuring password hashing (`bcrypt`) and protected middleware route guards.
*   **Interactive Visualizations**: Smooth, responsive graphics paired with elegant entrance transitions powered by `motion/react`.
*   **Modern Visual Identity**: Polished user interface utilizing Tailwind CSS, spacious negative space, and premium visual components.

---

## 🛠️ Tech Stack

### Frontend
*   **React 19** & **TypeScript**
*   **Vite** (Next-generation, ultra-fast frontend tooling)
*   **Tailwind CSS** (Utility-first styling framework)
*   **Lucide React** (Consistent, modern icon system)
*   **Recharts** (Interactive visual charts)
*   **Motion** (`motion/react` for fluid UI animations)

### Backend
*   **Express** (Robust HTTP server framework)
*   **Drizzle ORM** (TypeScript-first ORM)
*   **PostgreSQL** (Durable SQL database client)
*   **JSON Web Tokens (JWT)** (Secure authentication sessions)
*   **Bcrypt** (Secure password hashing)
*   **Esbuild** (Compiling and bundling the production server)

---

## 📂 Project Structure

```text
├── drizzle/                  # Auto-generated database migrations
├── src/
│   ├── components/           # Modular visual components
│   │   ├── AttendanceView.tsx   # Manual and bulk attendance managers
│   │   ├── DashboardView.tsx    # Graphical charts and analytics dashboard
│   │   ├── EmployeesView.tsx    # Employee profile lists and edit forms
│   │   ├── Login.tsx            # Secure JWT login panel
│   │   ├── ReportsView.tsx      # Comprehensive CSV/tabular reports exporter
│   │   ├── SettingsView.tsx     # Admin controls and system updates
│   │   └── Sidebar.tsx          # Responsive navigation sidebar
│   ├── context/
│   │   └── ToastContext.tsx     # Application-wide push notifications
│   ├── db/
│   │   ├── drizzle.config.ts    # Drizzle ORM configuration and dialect settings
│   │   ├── index.ts             # PostgreSQL client and pool initializer
│   │   └── schema.ts            # Drizzle relational SQL schema definition
│   ├── lib/
│   │   ├── firebase.ts          # Client-side Firebase configurations (if used)
│   │   └── firebase-admin.ts    # Server-side Firebase admin configurations (if used)
│   ├── middleware/
│   │   └── auth.ts              # Express HTTP route guards and token validation
│   ├── utils/
│   │   └── api.ts               # Custom Axios-like REST client wrapper
│   ├── App.tsx               # Main application visual wrapper
│   ├── index.css             # Global Tailwind directives & font imports
│   ├── main.tsx              # React mounting entry point
│   └── types.ts              # Global TypeScript interfaces and enums
├── .env.example              # Template for environment configuration
├── .gitignore                # Complete list of ignored paths
├── LICENSE                   # MIT License
├── package.json              # Project dependencies and script declarations
├── server.ts                 # Full-stack Express server and API gateway
├── tsconfig.json             # TypeScript compiler settings
└── vite.config.ts            # Vite compiler configurations
```

---

## ⚙️ Environment Variables

Copy the template file `.env.example` to `.env` to configure your environment variables:

```bash
cp .env.example .env
```

| Variable | Description | Example |
| :--- | :--- | :--- |
| `PORT` | Node server listening port | `3000` |
| `NODE_ENV` | Application environment state | `development` |
| `APP_URL` | Accessible URL of the system | `http://localhost:3000` |
| `JWT_SECRET` | Secret key used to sign session cookies/tokens | `my_secure_jwt_secret_token` |
| `SQL_HOST` | Host address of PostgreSQL server | `127.0.0.1` |
| `SQL_USER` | Username for database client runtime | `postgres` |
| `SQL_PASSWORD` | Password for database client runtime | `my_postgres_password` |
| `SQL_DB_NAME` | Target PostgreSQL database name | `employee_attendance_db` |
| `SQL_ADMIN_USER` | Admin username for migrations | `postgres` |
| `SQL_ADMIN_PASSWORD` | Admin password for migrations | `my_postgres_password` |
| `GEMINI_API_KEY` | (Optional) Gemini AI API Token | `your_gemini_api_key` |

---

## 🚀 Quick Start & Local Setup

### Prerequisite Checklist
*   **Node.js**: `v18.x` or higher
*   **PostgreSQL**: `v14.x` or higher

### Step 1: Clone the Repository
```bash
git clone https://github.com/ASLAM5309/Employee-Attendance.git
cd Employee-Attendance
```

### Step 2: Install Dependencies
```bash
npm install
```

### Step 3: Configure Environment Variables
Create a local `.env` file using `.env.example` as a starting point, then customize the connection values to point to your local PostgreSQL server:
```bash
cp .env.example .env
```

### Step 4: Run Database Migrations
Generate and apply database tables to your PostgreSQL instance using Drizzle Kit:
```bash
# Generate SQL migration script
npx drizzle-kit generate

# Run migration against database
npx drizzle-kit migrate
```

### Step 5: Start the Development Server
This boots the unified Express application server and mounts Vite's dev server middleware on port `3000`:
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your web browser.

---

## 📦 Production Build & Local Launch

To compile assets and start the application in optimized production mode:

```bash
# 1. Compile frontend client and bundle server
npm run build

# 2. Run the compiled self-contained bundle
npm start
```

This compiles static SPA bundles into `dist/` and compiles `server.ts` into a self-contained CommonJS executable (`dist/server.cjs`) using `esbuild`.

---

## ☁️ Deployment Instructions

This application is built as a **full-stack unified system** (Express serves compiled SPA assets in production), making deployment simple and cost-efficient.

### 1. Database Provisioning (PostgreSQL)
Set up a hosted PostgreSQL database using any modern cloud database provider:
*   **Neon**, **Supabase**, or **Render PostgreSQL**.
*   Once provisioned, note the host, user, password, and database name.
*   Set `SQL_HOST`, `SQL_USER`, `SQL_PASSWORD`, `SQL_DB_NAME`, `SQL_ADMIN_USER`, and `SQL_ADMIN_PASSWORD` to point to this remote database in your production settings.
*   Apply schema migrations against the live production database using:
    ```bash
    SQL_HOST=your_prod_host SQL_USER=your_prod_user SQL_PASSWORD=your_prod_pw SQL_DB_NAME=your_prod_db npx drizzle-kit migrate
    ```

### 2. Hosting the Full-Stack App (Render / Heroku / Koyeb / Railway)
Since the production build bundles the frontend assets inside the compiled Express container, you can deploy the entire app to a container platform like Render or Railway.

#### On Render:
1.  Create a new **Web Service**.
2.  Connect your GitHub Repository.
3.  Choose **Node** environment.
4.  Specify the build and start configuration:
    *   **Build Command**: `npm install && npm run build`
    *   **Start Command**: `node dist/server.cjs`
5.  Add all required production environment variables under the **Environment** tab:
    *   Set `NODE_ENV=production`
    *   Set `PORT=3000` (or leave empty to let Render bind default)
    *   Set your live database credentials (`SQL_HOST`, `SQL_USER`, etc.)
    *   Set a secure, custom `JWT_SECRET` key.

### 3. Separation of Concerns (Optional: Static Frontend on Vercel)
If you prefer to host the frontend static files on a serverless CDN like **Vercel** and the backend API separately on **Render**:

#### Frontend (Vercel)
1.  Configure Vercel to read `package.json`.
2.  Set **Build Command** to `vite build`.
3.  Set **Output Directory** to `dist`.
4.  Configure `VITE_API_BASE_URL` (in your API helper) to point to your deployed backend API URL.

#### Backend (Render Web Service)
1.  Host as a Node web service.
2.  Configure server to accept CORS requests from your Vercel URL.
3.  Deploy with `node dist/server.cjs` or adjust the entry point to target API endpoints exclusively.

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👥 Authors & Contributors

*   **ASLAM5309** - *Lead Creator & Maintainer* - [ASLAM5309](https://github.com/ASLAM5309)
