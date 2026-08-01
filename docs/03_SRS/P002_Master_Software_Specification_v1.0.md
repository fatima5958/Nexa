# P002 – Master Software Specification (MSS)
## Project NEXA

**Document ID**: NEXA-DOC-P002-v1.0
**Baseline Reference**: P001 – Project Constitution v1.0 (Approved)
**Company**: TheCodeWhiz
**Primary AI Embodied Robot**: Aura
**Status**: Baseline Approved (Implementation Ready)

---

## 1. Introduction
The Master Software Specification (MSS) provides an absolute, unambiguous, and complete engineering baseline for building Project NEXA. Every system component, API contract, database schema, state machine transition, and UI flow is defined herein.

## 2. Product Overview
NEXA shifts online education from passive consumption to an immersive, interactive, human-centric apprenticeship model powered by Aura, an embodied AI mentor that sees, hears, analyzes, and guides users in real time.

**Key Value Propositions:**
1. Embodied Mentorship
2. Real-Time Code Evaluation
3. Audio & Pitch Coaching
4. Adaptive Interview Engine
5. Long-Term Epistemic Memory

## 3. System Architecture
Distributed microservices pattern fronted by an edge-accelerated Next.js Application Layer.
- **Frontend**: Next.js 14, React 18+, TypeScript, Tailwind CSS, Zustand, Monaco Editor.
- **3D Graphics**: Three.js, React Three Fiber (WebGL 2.0).
- **Backend Runtimes**: Node.js 20 LTS (Fastify), Python 3.11+ (FastAPI), Go 1.22+ (Code Runner).
- **Databases**: PostgreSQL 16 (Primary), Redis Enterprise (Cache), Qdrant Cloud (Vector DB).
- **AI Stack**: Anthropic Claude 3.5 Sonnet, OpenAI GPT-4o, Deepgram Nova-2 (STT), ElevenLabs (TTS).

## 4. Feature List
- **REQ-NEXA-001**: Embodied Aura Canvas (3D/2D viewport rendering Aura with real-time lip sync).
- **REQ-NEXA-002**: Multi-Modal Voice Loop (Bi-directional streaming).
- **REQ-NEXA-004**: Interactive Code Workspace (Monaco Editor, live AST markers).
- **REQ-NEXA-006**: Adaptive Technical Interviewer.
- **REQ-NEXA-008**: Epistemic Memory System.

## 5. UI & Avatar Specification
- **Design Philosophy**: Robot-First Spatial Integration, Obsidian Glassmorphism (Dark mode), Zero-Latency Sensory Feedback.
- **Aura Robot Engine**: Finite State Machine (IDLE, LISTENING, THINKING, SPEAKING, CELEBRATING, ERROR_HANDLING).
- **Layout Zones**: Top Nav, Left Sidebar, Main Workspace Canvas, Aura Robot Panel (380px default width), Bottom Status Bar.

## 6. Core Learning Engines
- **Programming Learning Engine (PLE)**: Real-time IDE environment. Monaco editor, isolated container runner (Docker), AST diagnostics. Socratic Hinting logic.
- **Communication Coaching Engine (CCE)**: Real-time pitch & cadence engine. Calculates WPM, tracks filler words, and maps structural concept coverage.
- **Interview Engine (ITE)**: Multi-stage technical interviews. Automated rubric scoring (Problem Solving, Code Quality, System Design, Communication).

## 7. AI Memory Engine & Database
- **RAG Architecture**: Short-Term (Redis Token Window), Working Memory (Redis Hash), Long-Term (Qdrant Vector DB).
- **PostgreSQL Tables**: `users`, `profiles`, `learning_progress`, `coding_sessions`, `communication_sessions`, `interview_sessions`, `gamification`.

## 8. API Specification
REST APIs follow standard JSON structure with JWT auth.
- **Auth**: `POST /api/v1/auth/login`
- **Code Execution**: `POST /api/v1/ple/execute`
- **Speech Analysis**: `POST /api/v1/cce/analyze-session`

## 9. Deployment Strategy
- **Environments**: Local (Docker Compose), Staging (AWS EKS), Production (AWS EKS Aurora + Vercel).
- **CI/CD**: GitHub Actions for lint, build, test, and deploy.
- **Security**: OWASP Top 10 compliance, strict RBAC, AES-256 at rest, TLS 1.3 in transit.

*(Note: Refer to P002 PDF for the complete extensive architectural schemas, flow diagrams, UI CSS tokens, and exhaustive feature indices.)*
