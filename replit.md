# Employee Tracking Dashboard

## Overview

This is a full-stack web application built for BTN Services to track daily employee work activities. The system allows employees to log their daily missions, points earned, potential gains, and manage account information while providing comprehensive statistics and progress tracking.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for client-side routing
- **State Management**: TanStack React Query for server state
- **UI Framework**: Shadcn/ui components with Radix UI primitives
- **Styling**: TailwindCSS with custom business theme variables
- **Build Tool**: Vite for development and bundling

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **Authentication**: Replit Auth with OpenID Connect
- **Session Management**: Express sessions with PostgreSQL storage
- **File Uploads**: Multer for handling file attachments

### Database Architecture
- **Database**: PostgreSQL (Neon Database)
- **ORM**: Drizzle ORM with type-safe queries
- **Schema**: Shared schema between client and server
- **Migrations**: Drizzle Kit for schema migrations

## Key Components

### Authentication System
- Replit Auth integration with OIDC
- Session-based authentication with PostgreSQL storage
- User profile management with automatic user creation/updates
- Protected routes with authentication middleware

### Data Models
- **Users**: Profile information with Replit integration
- **Tracking Entries**: Daily work entries with missions, points, gains
- **Sessions**: Secure session storage for authentication

### File Management
- File upload system for screenshots and documents
- Support for JPEG, PNG, and PDF files (max 10MB)
- Local file storage in uploads directory
- File serving through Express static middleware

### Business Logic
- Daily tracking entry creation and management
- Statistics calculation (totals, averages, progress)
- Country-based work tracking
- Bonus points and managed accounts tracking
- Progress toward validation goals (30 accounts, 900k points)

## Data Flow

1. **Authentication Flow**: User logs in via Replit Auth → Session created → User data synced
2. **Dashboard Flow**: Stats aggregated from tracking entries → Progress calculated → Recent entries displayed
3. **Tracking Flow**: Form submission → Validation → File uploads → Database storage → Query invalidation
4. **History Flow**: Date/country filtering → Query execution → Table display with pagination

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: PostgreSQL database connection
- **drizzle-orm**: Type-safe database ORM
- **@tanstack/react-query**: Server state management
- **@radix-ui/**: UI component primitives
- **express**: Backend web framework
- **passport**: Authentication middleware

### Development Tools
- **vite**: Frontend build tool and dev server
- **tsx**: TypeScript execution for development
- **esbuild**: Production bundling for server
- **tailwindcss**: Utility-first CSS framework

### Third-party Services
- **Replit Auth**: Authentication provider
- **Neon Database**: Managed PostgreSQL hosting

## Deployment Strategy

### Development Environment
- Vite dev server for frontend hot reloading
- tsx for TypeScript execution with live reload
- Local file uploads to uploads directory
- Development session storage

### Production Environment
- Vite build process creates optimized static assets
- esbuild bundles server code for Node.js execution
- Static file serving through Express
- PostgreSQL session storage for scalability
- Autoscale deployment target on Replit

### Build Process
1. Frontend: `vite build` → Creates optimized static assets in dist/public
2. Backend: `esbuild` → Bundles server code with external packages
3. Production: `node dist/index.js` → Serves both API and static files

## Changelog
- June 25, 2025. Initial setup
- June 25, 2025. Completed BTN Services employee tracking dashboard with professional design, authentication, and all requested features

## Recent Changes
- Implemented beautiful gradient design with professional business theme
- Added comprehensive employee work tracking system
- Created multi-region country selection with flags
- Built progress tracking toward validation goals (30 accounts, 900k points)
- Added file upload system for proof documents
- Implemented real-time statistics and dashboard
- Fixed all TypeScript errors and database integration
- Application fully functional and ready for team use

## User Preferences

Preferred communication style: Simple, everyday language.