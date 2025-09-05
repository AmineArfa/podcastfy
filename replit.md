# Podcastfy.ai - Replit Setup

## Overview
Podcastfy.ai is an open-source Python package that transforms multimodal content (text, images, PDFs, YouTube videos, websites) into engaging, multilingual audio conversations using GenAI. This is an alternative to NotebookLM's podcast feature.

## Project Architecture
- **Backend**: FastAPI application serving REST endpoints
- **Main Components**:
  - Content parsers for various sources (PDF, website, YouTube)
  - Text-to-Speech providers (OpenAI, ElevenLabs, Google, Edge TTS)
  - Content generators using various LLM models
  - Audio processing and generation pipeline

## Current State
- ✅ Python 3.11 environment configured
- ✅ All dependencies installed from requirements.txt
- ✅ FastAPI server running on port 5000 with Replit-compatible configuration
- ✅ CORS enabled for web client access
- ✅ Deployment configured for autoscale mode
- ✅ Health check and API endpoints tested

## API Endpoints
- `GET /` - API information and available endpoints
- `GET /health` - Health check
- `POST /generate` - Generate podcast from URLs and configuration
- `GET /audio/{filename}` - Serve generated audio files

## Configuration
- Server runs on `0.0.0.0:5000` for Replit environment
- Supports multiple TTS providers (requires API keys)
- Configurable podcast generation parameters
- Audio files temporarily stored in `temp_audio/` directory

## Required API Keys
To use the podcast generation features, you'll need one or more of:
- `OPENAI_API_KEY` - For OpenAI TTS and LLM models
- `GEMINI_API_KEY` - For Google Gemini models
- `ELEVENLABS_API_KEY` - For ElevenLabs TTS

## Recent Changes
- Created main.py with proper Replit configuration
- Fixed type safety issues in API handlers
- Added CORS middleware for web client compatibility
- Configured deployment for production use
- Set up workflow for automatic server management

## User Preferences
- Project focused on API functionality over UI
- Requires external API keys for full functionality
- Designed for programmatic podcast generation