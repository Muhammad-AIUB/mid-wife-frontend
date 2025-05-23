# Midwife Frontend - Maternal Health Reporting System

A React-based web application designed to help pregnant women report health emergencies and provide healthcare professionals with tools for maternal care management. This system facilitates emergency reporting and administrative oversight for maternal health services.

## 🌟 Features

### Public Features
- **Emergency Reporting**: Anonymous reporting system for pregnant women in emergency situations
- **Real-time Statistics**: Display of recent reports and total report counts
- **Multilingual Support**: Bengali language support for local accessibility
- **Responsive Design**: Mobile-friendly interface for accessibility

### Healthcare Professional Features
- **User Registration**: Secure registration system for healthcare professionals
- **Email Verification**: Account verification process for security
- **Protected Dashboard**: Role-based access control for different user types
- **Profile Management**: User profile and account management

### Administrative Features
- **Admin Dashboard**: Comprehensive dashboard for report management
- **Interactive Maps**: Leaflet-based mapping for report visualization
- **Report Analytics**: Statistics and insights on maternal health reports
- **User Management**: Admin controls for user verification and management

## 🛠️ Tech Stack

- **Frontend Framework**: React 19 (RC) with TypeScript
- **Build Tool**: Vite 6.0
- **Styling**: Tailwind CSS 4.0
- **Routing**: React Router DOM 7.1
- **Maps**: React Leaflet 5.0 & Google Maps API
- **Forms**: React Hook Form with Zod validation
- **HTTP Client**: Axios
- **Notifications**: Sonner
- **Deployment**: Vercel

## 📋 Prerequisites

Before running this project, make sure you have:

- Node.js (version 18 or higher)
- npm or yarn package manager
- Git

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd midwife-frontend
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Setup

Create a `.env` file in the root directory and add necessary environment variables:

```env
# Add your environment variables here
# Example:
# VITE_API_BASE_URL=https://midwife-backend.vercel.app/api/v1
# VITE_GOOGLE_MAPS_API_KEY=your_google_maps_api_key
```

### 4. Start Development Server

```bash
npm run dev
```

The application will be available at `http://localhost:5173`

## 📁 Project Structure

```
src/
├── components/           # Reusable UI components
│   ├── ProtectedRoute.tsx   # Route protection component
│   ├── ReportForm.tsx       # Emergency report form
│   └── UserMap.tsx          # Interactive map component
├── pages/               # Application pages
│   ├── Dashboard.tsx        # Admin dashboard
│   ├── Login.tsx           # User login page
│   ├── Register.tsx        # User registration page
│   ├── Profile.tsx         # User profile page
│   └── NotVerified.tsx     # Account verification page
├── data/               # Static data and configurations
├── assets/             # Static assets (images, icons)
├── App.tsx             # Main application component
├── main.tsx            # Application entry point
└── index.css           # Global styles
```

## 🔐 Authentication & Authorization

The application implements role-based access control with the following user types:

- **Public Users**: Can submit emergency reports anonymously
- **Verified Users**: Healthcare professionals with verified accounts
- **Admins**: Full access to dashboard and user management

### Protected Routes

- `/dashboard` - Admin only
- `/profile` - Verified users only
- `/report` - Public access
- `/login`, `/register` - Public access

## 🗺️ Map Integration

The application uses two mapping solutions:

1. **React Leaflet**: For interactive map displays
2. **Google Maps API**: For enhanced mapping features

Maps are used to:
- Visualize report locations
- Display geographical distribution of cases
- Provide location-based insights

## 📱 API Integration

The frontend communicates with the backend API hosted at:
- **Production**: `https://midwife-backend.vercel.app/api/v1`

### Key API Endpoints Used

- `GET /reports` - Fetch reports and statistics
- `POST /auth/register` - User registration
- `POST /auth/login` - User authentication
- `POST /reports` - Submit new reports

## 🎨 UI/UX Features

- **Responsive Design**: Works seamlessly on desktop and mobile devices
- **Bengali Language Support**: Localized content for target audience
- **Accessible Interface**: Designed with accessibility best practices
- **Modern UI**: Clean, professional design using Tailwind CSS
- **Toast Notifications**: User feedback using Sonner

## 🚀 Deployment

### Vercel Deployment

The project is configured for Vercel deployment with:

1. **Build Command**: `npm run build`
2. **Output Directory**: `dist`
3. **SPA Routing**: Configured in `vercel.json` for client-side routing

### Manual Deployment

```bash
# Build the project
npm run build

# Preview the build
npm run preview
```

## 🧪 Development Scripts

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Run linting
npm run lint

# Preview production build
npm run preview
```

## 🔧 Configuration Files

- **TypeScript**: `tsconfig.json`, `tsconfig.app.json`, `tsconfig.node.json`
- **ESLint**: `eslint.config.js`
- **Vite**: `vite.config.ts`
- **Vercel**: `vercel.json`
- **Tailwind**: Configured via Vite plugin

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is developed under collaboration with eXhort and Projonmo Research Foundation Bangladesh to help pregnant women in emergency situations.

## 🆘 Support

For support and assistance:
- WhatsApp: [Contact for help]
- Email: [Contact information]

## 🏥 About

This application is specifically designed to support maternal healthcare in Bangladesh, providing:
- Emergency reporting capabilities for pregnant women
- Healthcare professional tools for case management
- Administrative oversight for maternal health services
- Real-time monitoring and analytics

The system aims to improve maternal health outcomes by facilitating quick emergency response and providing healthcare professionals with better tools for patient care and case management.