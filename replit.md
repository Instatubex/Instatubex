# Instatubex - Replit Architecture Overview

## Overview

Instatubex is a premium full-stack TypeScript application that provides a luxury media downloading service for multiple social media platforms with auto-fetching capabilities and grid-based format selection. The application is built with React on the frontend and Express.js on the backend, with PostgreSQL as the database using Drizzle ORM. The website features a modern, luxury design with gradient backgrounds and glass-morphism effects, complete Google AdSense integration, and advanced download functionality.

## User Preferences

Preferred communication style: Simple, everyday language.
Brand Name: Instatubex
Design Theme: Luxury/Premium design with gradient backgrounds and glass-morphism effects
Target Platforms: Instagram, YouTube, TikTok, Facebook, Twitch

## System Architecture

The application follows a modern full-stack architecture with the following key components:

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for fast development and optimized builds
- **UI Framework**: Shadcn/UI components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom design tokens
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for client-side routing
- **Forms**: React Hook Form with Zod validation

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **Session Management**: Built-in session handling
- **API Design**: RESTful endpoints with proper error handling
- **Development**: Hot reloading with Vite integration

### Database Architecture
- **ORM**: Drizzle ORM with TypeScript-first approach
- **Database**: PostgreSQL (configured for Neon Database)
- **Schema**: Structured with users and downloads tables
- **Migrations**: Automated with Drizzle Kit

## Key Components

### Core Features
1. **Multi-Platform Support**: Instagram (videos, photos, stories), YouTube, TikTok, Facebook, Twitch
2. **Auto-Fetch Technology**: Automatically analyzes URLs and displays media information without waiting
3. **Grid-Based Download System**: Visual format selection with thumbnails, quality options, and file sizes
4. **Multiple Format Support**: MP4, MP3, JPG, PNG downloads based on content type
5. **Quality Selection**: 1080p, 720p, 480p, 360p, and audio-only options for YouTube
6. **Real-Time Progress**: Individual progress tracking for each download format
7. **Google AdSense Integration**: Complete monetization with auto ads and strategic placement
8. **Analytics Integration**: Google Analytics for user behavior tracking
9. **Luxury Design**: Premium UI with gradient backgrounds and glass-morphism effects

### Database Schema
- **Users Table**: Basic user management with username/password
- **Downloads Table**: Track download requests with metadata (URL, platform, format, status, etc.)

### API Endpoints
- `POST /api/download`: Process video download requests
- Additional endpoints for user management and download tracking

### UI Components
- **Download Form**: Main interface for URL input and format selection
- **Platform Selection**: Visual platform picker with icons
- **Progress Tracking**: Real-time download status updates
- **Legal Pages**: Terms, Privacy Policy, DMCA, Disclaimer

## Data Flow

1. **User Input**: User pastes video URL and selects format
2. **URL Validation**: Client-side validation using Zod schemas
3. **Platform Detection**: Automatic platform identification from URL
4. **Download Request**: API call to backend with validated data
5. **Processing**: Backend processes video using mock ytdl-core functionality
6. **Status Updates**: Real-time progress updates to frontend
7. **File Delivery**: Completed download delivered to user

## External Dependencies

### Frontend Dependencies
- **UI Components**: Radix UI primitives for accessibility
- **Analytics**: Google Analytics for user tracking
- **Form Handling**: React Hook Form with Zod validation
- **HTTP Client**: Native fetch with TanStack Query wrapper

### Backend Dependencies
- **Database**: Neon Database (PostgreSQL) with connection pooling
- **Session Storage**: connect-pg-simple for PostgreSQL session storage
- **Video Processing**: Mock ytdl-core implementation (placeholder for actual video processing)

### Development Tools
- **Build System**: Vite with TypeScript support
- **Code Quality**: ESLint and TypeScript compiler
- **Database Tools**: Drizzle Kit for migrations and schema management
- **Replit Integration**: Custom Vite plugins for Replit environment

## Deployment Strategy

### Development Environment
- **Local Development**: Vite dev server with Express backend
- **Hot Reloading**: Full-stack hot reloading support
- **Environment Variables**: Separate config for development/production

### Production Build
- **Frontend**: Vite production build with optimized assets
- **Backend**: ESBuild compilation for Node.js deployment
- **Database**: Automated migrations on deployment
- **Static Assets**: Served from Express in production

### Environment Configuration
- **Database URL**: PostgreSQL connection string
- **Google Analytics**: Measurement ID for tracking
- **Session Configuration**: Secure session management
- **CORS**: Configured for cross-origin requests

The application is designed to be easily deployable on Replit with minimal configuration, using environment variables for sensitive data and providing a seamless development experience.