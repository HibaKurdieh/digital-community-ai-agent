# Digital Community AI Agent

## Overview
This project presents the initial architecture of an AI-based system designed to provide accurate and real-time information to community residents through a chat interface.

The system is built around a key principle:
separating language understanding from the data source to ensure reliability and prevent hallucinations.

## System Goals
- Provide fast and accurate responses to users
- Reduce administrative workload
- Improve accessibility to community information
- Ensure responses are based only on real data

## Architecture Overview
The system follows this flow:

User → Telegram Bot → Backend Server → LLM → Agent → Tools → Database → Response → User

## Key Components

### LLM Layer
- Used only for:
  - Intent detection
  - Entity extraction
- Does NOT generate factual answers

### Agent (LangGraph)
- Decision-based workflow
- Selects appropriate tools
- Handles missing or unclear inputs
- Manages system logic

### Tools Layer
- Responsible for retrieving real data
- Ensures accuracy of responses

### Database
- Google Sheets (MVP)
- Stores structured activity data

## Key Design Principles
- Separation of concerns (LLM vs Data)
- No direct answer generation without validation
- Reliable data-driven responses
- Minimal dependency on AI generation
- Modular and scalable architecture

## Technologies Used
- Python (FastAPI)
- LangGraph (Agent workflow)
- GPT-4o-mini (Intent & Entity extraction)
- Telegram Bot API
- Google Sheets (Database)

## Future Improvements
- Activity registration system
- Admin dashboard
- Notifications system
- Migration to scalable database (SQL)
- Enhanced agent capabilities

## Notes
This project focuses on system architecture and design rather than full implementation.

## Author
Hiba Kurdieh