# Aditya Jain Professional Portfolio

## Overview

A professional portfolio website for Aditya Jain, a DevOps Engineer specializing in cloud-native platforms. The application is a full-stack TypeScript project with a React frontend and Express backend, designed to showcase professional experience, skills, education, and contact information in a modern, polished interface.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack React Query for server state and caching
- **Styling**: Tailwind CSS with CSS variables for theming (dark mode default)
- **Component Library**: shadcn/ui with Radix UI primitives for accessible, customizable components
- **Animations**: Framer Motion for smooth transitions and interactions
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Runtime**: Node.js with Express
- **Language**: TypeScript with ES modules
- **API Pattern**: RESTful endpoints prefixed with `/api`
- **Static Serving**: Express serves the built React app in production, with Vite middleware in development

### Data Storage
- **ORM**: Drizzle ORM configured for PostgreSQL
- **Schema Location**: `shared/schema.ts` contains database table definitions
- **Migrations**: Managed via `drizzle-kit push` command
- **Current Storage**: In-memory storage implementation (`MemStorage` class) with interface ready for database migration

### Design System
- **Typography**: Inter/DM Sans for headings, JetBrains Mono for technical elements
- **Color Scheme**: HSL-based CSS variables with dark mode as default
- **Spacing**: Consistent Tailwind spacing units (4, 6, 8, 12, 16, 24)
- **Components**: Hero section, experience timeline, skills grid, education cards, navigation with smooth scrolling

### Project Structure
```
├── client/               # React frontend
│   ├── src/
│   │   ├── components/   # UI components (shadcn/ui + custom)
│   │   ├── hooks/        # Custom React hooks
│   │   ├── lib/          # Utilities and query client
│   │   └── pages/        # Page components
├── server/               # Express backend
│   ├── index.ts          # Server entry point
│   ├── routes.ts         # API route registration
│   ├── storage.ts        # Data storage interface
│   └── vite.ts           # Vite dev server integration
├── shared/               # Shared types and schemas
│   └── schema.ts         # Drizzle ORM schema definitions
└── attached_assets/      # Static assets (resume, images)
```

## External Dependencies

### Database
- **PostgreSQL**: Primary database (requires `DATABASE_URL` environment variable)
- **Drizzle ORM**: Type-safe database queries and schema management
- **connect-pg-simple**: Session storage for PostgreSQL (available but not currently active)

### UI Libraries
- **Radix UI**: Comprehensive set of accessible component primitives
- **Lucide React**: Icon library
- **React Icons**: Additional icon sets (including Simple Icons for tech logos)
- **Embla Carousel**: Carousel component
- **Vaul**: Drawer component
- **cmdk**: Command menu component

### Build & Development
- **Vite**: Development server and production bundler
- **esbuild**: Server-side bundling for production
- **TypeScript**: Type checking across the entire codebase
- **PostCSS/Autoprefixer**: CSS processing pipeline

### Form & Validation
- **React Hook Form**: Form state management
- **Zod**: Schema validation
- **drizzle-zod**: Zod schema generation from Drizzle schemas