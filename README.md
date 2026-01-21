# 🏠 Rentify - Frontend

The frontend application for **LPRT (Landlord Property Rental Tool)** - a modern property management system built with React and Vite.

🌐 **Live Demo**: [https://rentifyyyy.netlify.app/](https://rentifyyyy.netlify.app/)

## ✨ Features

### 🔐 Authentication

- Role-based login (Property Owner / Tenant)
- Secure JWT-based authentication
- Persistent login sessions

### 🏢 Property Owner Dashboard

- **Property Management**: Add, edit, delete, and view properties
- **Tenant Management**: View and manage current tenants
- **Payments**: Track rent payments and financial records
- **Maintenance**: Handle maintenance requests from tenants
- **Settings**: Account preferences and profile management

### 👥 Tenant Dashboard

- **My Property**: View assigned rental property details
- **Pay Rent**: Make rent payments
- **Complaints**: Submit and track maintenance requests
- **Settings**: Account preferences and profile management

## 🚀 Tech Stack

| Technology       | Version | Purpose                 |
| ---------------- | ------- | ----------------------- |
| React            | 19.1.1  | UI Library              |
| Vite             | 5.4.20  | Build Tool & Dev Server |
| Tailwind CSS     | 4.1.13  | Styling                 |
| React Router DOM | 7.8.1   | Client-side Routing     |
| Axios            | 1.11.0  | HTTP Client             |
| Lucide React     | 0.540.0 | Icon Library            |
| React Icons      | 5.5.0   | Additional Icons        |

## 📁 Project Structure

```
frontend/
├── public/
│   └── _redirects           # Netlify redirect rules
├── src/
│   ├── assets/              # Static assets (images, fonts)
│   ├── components/
│   │   ├── Auth/            # Authentication components
│   │   │   ├── Layout.jsx   # Auth layout wrapper
│   │   │   ├── Login.jsx    # Login form
│   │   │   ├── RoleSelection.jsx  # Role selection UI
│   │   │   └── Signup.jsx   # Registration form
│   │   ├── owner/           # Property owner components
│   │   │   ├── AddPropertyModal.jsx
│   │   │   ├── AddTenantModal.jsx
│   │   │   ├── EditPropertyModal.jsx
│   │   │   ├── EditTenantModal.jsx
│   │   │   ├── Maintenance.jsx
│   │   │   ├── Payments.jsx
│   │   │   ├── PropertyDetailsModal.jsx
│   │   │   ├── PropertyManagement.jsx
│   │   │   ├── Settings.jsx
│   │   │   ├── TenantDetailsModal.jsx
│   │   │   └── Tenants.jsx
│   │   └── tenants/         # Tenant components
│   │       ├── Complaints.jsx
│   │       ├── MyProperty.jsx
│   │       ├── Payments.jsx
│   │       └── Settings.jsx
│   ├── api.js               # Axios API configuration
│   ├── App.jsx              # Main application component
│   ├── index.css            # Global styles
│   ├── index.js             # Legacy entry point
│   └── main.jsx             # Application entry point
├── index.html               # HTML template
├── package.json             # Dependencies & scripts
├── postcss.config.cjs       # PostCSS configuration
├── tailwind.config.cjs      # Tailwind CSS configuration
├── vite.config.js           # Vite configuration
└── vercel.json              # Vercel deployment config
```

## 🛠️ Getting Started

### Prerequisites

- **Node.js** >= 18.x
- **npm** or **yarn**

### Installation

1. **Navigate to the frontend directory**:

   ```bash
   cd frontend
   ```

2. **Install dependencies**:

   ```bash
   npm install
   ```

3. **Configure environment variables** (optional):

   Create a `.env` file in the frontend directory:

   ```env
   VITE_API_URL=http://localhost:5000/api
   ```

4. **Start the development server**:

   ```bash
   npm run dev
   ```

5. **Open your browser** and navigate to:
   ```
   http://localhost:5173
   ```

## 📜 Available Scripts

| Command           | Description                           |
| ----------------- | ------------------------------------- |
| `npm run dev`     | Start development server on port 5173 |
| `npm run build`   | Build for production                  |
| `npm run preview` | Preview production build locally      |
| `npm run lint`    | Run ESLint for code quality           |

## 🔧 Configuration

### Vite Configuration

The Vite config (`vite.config.js`) includes:

- React plugin for JSX support
- Development server on port 5173
- Production build output to `dist/`

### API Configuration

The API client (`src/api.js`) features:

- Axios instance with base URL configuration
- JWT token auto-injection via request interceptor
- Automatic logout on 401 responses
- 10-second request timeout

### Environment Variables

| Variable       | Description          | Default                     |
| -------------- | -------------------- | --------------------------- |
| `VITE_API_URL` | Backend API base URL | `http://localhost:5000/api` |

## 🚀 Deployment

### Netlify

The project is configured for Netlify deployment:

- `public/_redirects` handles SPA routing
- Build command: `npm run build`
- Publish directory: `dist`

### Vercel

Vercel configuration is available in `vercel.json`:

- Build command: `npm run build`
- Output directory: `dist`

## 🎨 Styling

This project uses **Tailwind CSS** for styling with:

- Utility-first CSS classes
- Custom yellow/gray color scheme
- Responsive design for all screen sizes
- PostCSS for processing

## 🔗 API Integration

The frontend connects to the backend API for:

- User authentication (`/auth/*`)
- Property management (`/properties/*`)
- Tenant operations (`/tenants/*`)
- Payment processing (`/payments/*`)
- Maintenance/Complaints (`/complaints/*`, `/maintenance/*`)

## 📱 Responsive Design

The application is fully responsive with:

- Collapsible sidebar navigation
- Mobile-friendly layouts
- Touch-friendly UI elements

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the terms specified in the root [LICENSE](../LICENSE) file.

---

**Built with ❤️ using React + Vite + Tailwind CSS**
