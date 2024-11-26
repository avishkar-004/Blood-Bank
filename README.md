# LifeLink - Blood Bank & Donor Matching Portal

A comprehensive blood bank management system built with React and TypeScript. Connects blood donors with recipients in real-time through an intuitive healthcare-focused interface.

## Features

### For Donors
- **Donor Dashboard** - View donation history, eligibility status, and upcoming camps
- **Donation Camps** - Browse and book slots at nearby donation events
- **Availability Toggle** - Set availability for emergency requests
- **Donation Tracking** - Track total donations and lives saved

### For Recipients
- **Blood Request** - Submit requests with urgency levels (Normal/Urgent/Emergency)
- **Donor Search** - Find compatible donors by blood type and location
- **Emergency Portal** - Fast-track urgent blood requirements
- **Request Tracking** - Monitor request status in real-time

### For Administrators
- **Admin Dashboard** - Overview of inventory, requests, and donor statistics
- **Inventory Management** - Track blood stock levels with alerts
- **Request Management** - Approve, match, and process blood requests
- **User Management** - Monitor donor and recipient accounts

### General
- **Role-Based Access** - Secure authentication with donor/recipient/admin roles
- **Notifications** - Real-time alerts for matches, reminders, and low stock
- **Blood Compatibility** - Automatic donor matching based on blood type compatibility
- **Responsive Design** - Works across desktop and mobile devices
- **Dark Mode** - Healthcare-optimized dark theme

## Tech Stack

- **React 18** with TypeScript
- **Vite** for development and builds
- **Tailwind CSS** with medical-themed design tokens
- **shadcn/ui** component library
- **React Router v6** for routing with protected routes
- **TanStack Query** for async state management
- **React Hook Form** + **Zod** for form validation
- **Recharts** for data visualization
- **date-fns** for date utilities
- **Lucide React** for icons

## Getting Started

### Prerequisites

- Node.js 18+
- npm or yarn

### Installation

```bash
git clone https://github.com/avishkar-004/Blood-Bank.git
cd Blood-Bank
npm install
```

### Development

```bash
npm run dev
```

The app runs at `http://localhost:8080`.

### Demo Accounts

| Role      | Email              | Password     |
|-----------|--------------------|--------------|
| Donor     | donor@test.com     | password123  |
| Recipient | recipient@test.com | password123  |
| Admin     | admin@test.com     | admin123     |

### Production Build

```bash
npm run build
npm run preview
```

## Project Structure

```
src/
├── components/
│   ├── ui/                  # Reusable UI primitives (shadcn)
│   ├── Header.tsx           # App header with navigation
│   ├── NavLink.tsx          # Active navigation link
│   └── ProtectedRoute.tsx   # Role-based route guard
├── contexts/
│   └── AuthContext.tsx       # Authentication provider
├── hooks/
│   ├── use-mobile.tsx       # Responsive breakpoint hook
│   └── use-toast.ts         # Toast notification hook
├── lib/
│   ├── mockData.ts          # Data models and mock dataset
│   ├── storage.ts           # LocalStorage CRUD layer
│   └── utils.ts             # Utility functions
├── pages/
│   ├── AdminDashboard.tsx   # Admin overview
│   ├── Auth.tsx             # Login/Register
│   ├── BloodRequest.tsx     # Submit blood requests
│   ├── DonationCamps.tsx    # Camp listings
│   ├── DonorDashboard.tsx   # Donor overview
│   ├── DonorSearch.tsx      # Find donors
│   ├── Emergency.tsx        # Emergency requests
│   ├── Help.tsx             # Help center
│   ├── Index.tsx            # Landing page
│   ├── NotFound.tsx         # 404 page
│   ├── Notifications.tsx    # Notification center
│   ├── Profile.tsx          # User profile
│   ├── RecipientDashboard.tsx # Recipient overview
│   └── Settings.tsx         # App settings
└── services/
    ├── auth.service.ts      # Authentication API
    ├── blood.service.ts     # Blood requests & inventory
    ├── donor.service.ts     # Donor management
    └── notification.service.ts # Notifications
```

## License

MIT
