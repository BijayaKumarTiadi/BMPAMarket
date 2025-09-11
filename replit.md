# Stock Laabh Trading Platform

## Overview

This is a comprehensive B2B ecommerce marketplace for the trading industry branded as "Stock Laabh" with MySQL database backend. The platform provides a professional trading environment for business members to buy and sell stock, materials, and equipment. The system features user registration with email OTP verification, annual membership fees (₹2,499), admin approval workflow, and role-based access control.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **Routing**: Wouter for client-side routing with role-based page access
- **UI Components**: Shadcn/ui component library with Radix UI primitives for consistent design
- **Styling**: Tailwind CSS with custom CSS variables for theming
- **State Management**: TanStack React Query for server state management and caching
- **Forms**: React Hook Form with Zod validation for type-safe form handling

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **API Design**: RESTful API with route-based organization
- **Session Management**: Express sessions with PostgreSQL store for authentication persistence
- **Middleware**: Custom logging, error handling, and authentication middleware

### Authentication & Authorization
- **Strategy**: Replit OpenID Connect (OIDC) authentication
- **Session Storage**: PostgreSQL-backed sessions with configurable TTL
- **Role-Based Access**: Multi-role system (admin, buyer, seller, both) with route protection
- **User Management**: Complete user profile system with company information and membership status

### Database Architecture
- **Primary Database**: PostgreSQL with Neon serverless hosting
- **ORM**: Drizzle ORM for type-safe database operations
- **Schema Management**: Drizzle migrations with schema-first approach
- **Data Models**: Comprehensive schema including users, stock listings, orders, messages, categories, and payments

### Key Data Models
- **Users**: Profile information, roles, membership status, and Stripe integration
- **Stock Listings**: Product catalog with categories, pricing, and inventory management
- **Orders**: Complete order lifecycle management with status tracking
- **Messages**: Built-in messaging system for buyer-seller communication
- **Categories**: Hierarchical product categorization system

### File Structure
- **Shared**: Common TypeScript types and database schema shared between client and server
- **Client**: React frontend application with component-based architecture
- **Server**: Express backend with modular route organization
- **Monorepo**: Single repository with clear separation between frontend and backend code

## External Dependencies

### Payment Processing
- **Stripe**: Complete payment infrastructure for membership subscriptions and transaction processing
- **Integration**: React Stripe.js for frontend payment forms and server-side webhook handling

### Database & Hosting
- **Neon Database**: Serverless PostgreSQL hosting with connection pooling
- **Replit**: Development and deployment platform with integrated authentication

### Development Tools
- **TypeScript**: Full type safety across the entire stack
- **Vite**: Fast development server and optimized production builds
- **Drizzle Kit**: Database migration and introspection tools

### UI & Design System
- **Radix UI**: Headless component primitives for accessibility
- **Tailwind CSS**: Utility-first styling framework
- **Lucide Icons**: Consistent icon system throughout the application

### Additional Services
- **File Upload**: Uppy integration for handling product images and documents
- **Email/SMS**: OTP verification system for user registration
- **Search**: Built-in search functionality for stock listings and categories

## Recent Changes (September 2025)

### Admin Panel Improvements
- **Table Responsiveness**: Implemented comprehensive responsive design for all admin tables (Members, Approved Users, Payment History)
- **Mobile Optimization**: Added breakpoint-based column visibility (hidden on smaller screens)
- **Sticky Actions**: Actions column remains visible with proper z-index layering during horizontal scroll
- **Column Management**: Minimum width enforcement for proper text display with truncation

### Product Management Enhancements  
- **Streamlined Add Product Page**: Removed Back to Dashboard button for cleaner navigation flow
- **Form Simplification**: Removed Stock Type field requirement from product creation workflow
- **UI Polish**: Eliminated number input spinners from GSM field for cleaner appearance
- **Optimized Layout**: Removed redundant descriptive text and improved container spacing for better UX

### Technical Improvements
- **Schema Updates**: Cleaned up deprecated stockType references from form validation and data models
- **Type Safety**: Resolved all TypeScript errors and maintained strict type checking
- **Hot Reload**: All changes implemented with seamless Vite HMR integration

The application follows modern web development best practices with a focus on type safety, performance, and user experience while providing a comprehensive marketplace solution for the printing industry.