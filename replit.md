# replit.md

## Overview

This is an AI-powered mathematical calculation application that allows users to draw mathematical expressions on a canvas and get automated solutions. The system consists of a React frontend for drawing mathematical expressions and a FastAPI backend that uses Google's Gemini AI to analyze and solve the mathematical problems from drawn images.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript and Vite for fast development and hot module replacement
- **UI Libraries**: 
  - Mantine Core for UI components and drawing canvas functionality
  - Tailwind CSS for styling with custom design system
  - Shadcn/ui components for consistent UI elements
- **Drawing System**: HTML5 Canvas with custom drawing logic for mathematical expression input
- **Math Rendering**: MathJax integration for rendering LaTeX mathematical expressions
- **State Management**: React hooks (useState, useEffect) for local component state
- **HTTP Client**: Axios for API communication with the backend
- **Build Tool**: Vite with TypeScript support and ESLint integration

### Backend Architecture
- **Framework**: FastAPI for high-performance async API development
- **AI Integration**: Google Gemini 1.5 Flash model for mathematical expression analysis
- **Image Processing**: PIL (Python Imaging Library) for handling base64 image data
- **API Design**: RESTful API with structured endpoints for calculation processing
- **Data Validation**: Pydantic models for request/response validation
- **CORS**: Configured to allow cross-origin requests from frontend

### Core Features
- **Canvas Drawing**: Users can draw mathematical expressions with different colors
- **Image Analysis**: Converts canvas drawings to base64 images for AI processing
- **Mathematical Solving**: Supports multiple types of mathematical problems:
  - Simple arithmetic expressions
  - Algebraic equations
  - System of equations
  - Variable assignments
  - Graphical problems
- **Real-time Results**: Displays solved expressions with LaTeX formatting
- **Interactive UI**: Draggable result display and color palette for drawing

### Data Flow
1. User draws mathematical expression on HTML5 canvas
2. Canvas content is converted to base64 image format
3. Image data is sent to FastAPI backend with variable context
4. Gemini AI analyzes the image and solves mathematical expressions
5. Results are returned in structured format with LaTeX expressions
6. Frontend renders results using MathJax for proper mathematical notation

## External Dependencies

### AI Services
- **Google Gemini API**: Core AI service for mathematical expression recognition and solving
  - Model: gemini-1.5-flash for image analysis and mathematical computation
  - Requires GEMINI_API_KEY environment variable

### Frontend Dependencies
- **React Ecosystem**: React 18, React DOM, React Router for navigation
- **UI/UX Libraries**: 
  - Mantine Core and Hooks for drawing components
  - Tailwind CSS for styling
  - Lucide React for icons
- **Mathematical Rendering**: MathJax for LaTeX expression display
- **Canvas Tools**: html2canvas for image capture, lazy-brush for smooth drawing
- **Utilities**: Axios for HTTP requests, clsx for class management

### Backend Dependencies
- **Web Framework**: FastAPI with uvicorn for ASGI server
- **AI/ML**: google-generativeai for Gemini API integration
- **Image Processing**: Pillow for image manipulation
- **Utilities**: python-dotenv for environment management, pydantic for data validation

### Development Tools
- **Frontend**: Vite, TypeScript, ESLint for code quality
- **Backend**: Python 3.x runtime environment
- **Package Management**: npm/yarn for frontend, pip for backend dependencies