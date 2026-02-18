# FINAL-YEAR-PROJECT

AI-Enabled Intelligent Teacher Robot for Automated Attendance, Personalized Learning Assistance, and Real-Time Knowledge Retrieval

Project Overview

The proposed project aims to develop an AI-enabled intelligent teacher robot that assists in classroom management and student learning. The system is designed to automate attendance marking, provide interactive learning support, and retrieve educational information in real time.
The robot functions as a teaching assistant rather than a replacement for teachers. It helps reduce manual workload and improves classroom efficiency through automation and intelligent interaction.

Working Principle
The system uses computer vision and artificial intelligence techniques to recognize students and mark attendance automatically. It also supports voice-based interaction, allowing students to ask questions. The system processes the query using natural language processing and retrieves relevant information from a knowledge base.
The overall system combines:
Face recognition for attendance
Speech recognition for interaction
Natural language processing for understanding queries
Knowledge retrieval for answering questions

Main Components
Camera Module – Captures student images for attendance.
Face Recognition Module – Identifies students and updates attendance records.
Microphone Module – Captures student voice input.
Speech-to-Text Module – Converts voice queries into text.
NLP Module – Analyzes and understands student questions.
Knowledge Retrieval Module – Fetches relevant answers from the database.
Output Module – Provides response via speaker or display.
Database – Stores attendance and interaction data securely.

 (cd "$(git rev-parse --show-toplevel)" && git apply --3way <<'EOF' 
diff --git a/README.md b/README.md
index 568b7437aac8ae55d2136e9817016ccf9ccec8f5..111d6c1706885dd338125e50bbba74fad1c2cba4 100644
--- a/README.md
+++ b/README.md
@@ -1,32 +1,52 @@
 # FINAL-YEAR-PROJECT
 
-AI-Enabled Intelligent Teacher Robot for Automated Attendance, Personalized Learning Assistance, and Real-Time Knowledge Retrieval
+AI-Enabled Intelligent Teacher Robot for Automated Attendance, Personalized Learning Assistance, and Real-Time Knowledge Retrieval.
 
-Project Overview
+## Project Overview
 The proposed project aims to develop an AI-enabled intelligent teacher robot that assists in classroom management and student learning. The system is designed to automate attendance marking, provide interactive learning support, and retrieve educational information in real time.
 The robot functions as a teaching assistant rather than a replacement for teachers. It helps reduce manual workload and improves classroom efficiency through automation and intelligent interaction.
 
-Working Principle
+## Working Principle
 The system uses computer vision and artificial intelligence techniques to recognize students and mark attendance automatically. It also supports voice-based interaction, allowing students to ask questions. The system processes the query using natural language processing and retrieves relevant information from a knowledge base.
+
 The overall system combines:

+- Face recognition for attendance
+- Speech recognition for interaction
+- Natural language processing for understanding queries
+- Knowledge retrieval for answering questions
+
+## Layered System Architecture
+

+flowchart TB
+    A[Frontend Layer<br/>React UI (Chatbot + Instructor Panel)] --> B[NodeJS Layer<br/>API Gateway<br/>Authentication (JWT)<br/>Role-Based Access Control<br/>Request Routing]
+    B --> C[Caching Layer<br/>Redis (Session Cache + Frequently Asked Queries)]
+    C --> D[Backend AI Services (Python Microservices)<br/>RAG Engine<br/>Attendance Engine<br/>Quiz Generator<br/>Auto-Evaluator<br/>Whisper API (Flask)<br/>Personalization Engine<br/>Model Manager<br/>AI Validation Guard]
+    D --> E[Async Task Queue<br/>Background Processing<br/>(Embedding Generation, LMS Sync, Transcription)]
+    E --> F[Database Layer<br/>Oracle SQL (Structured Data)<br/>LLM Vector Database (Embeddings)]
+```
+
+### Layer Responsibilities
+- **Frontend Layer**: Provides student and instructor user interfaces for chatbot interaction and panel-based management.
+- **NodeJS Layer**: Handles authentication, role enforcement, API gateway concerns, and request routing to internal services.
+- **Caching Layer**: Uses Redis to speed up session access and serve frequently asked queries with low latency.
+- **Backend AI Services**: Runs specialized Python microservices for retrieval, attendance, quiz generation, evaluation, speech, personalization, model lifecycle, and validation.
+- **Async Task Queue**: Processes long-running tasks outside the synchronous request cycle.
+- **Database Layer**: Persists structured relational data and semantic vectors for retrieval-augmented generation workflows.
+
+## Main Components
+- **Camera Module** – Captures student images for attendance.
+- **Face Recognition Module** – Identifies students and updates attendance records.
+- **Microphone Module** – Captures student voice input.
+- **Speech-to-Text Module** – Converts voice queries into text.
+- **NLP Module** – Analyzes and understands student questions.
+- **Knowledge Retrieval Module** – Fetches relevant answers from the database.
+- **Output Module** – Provides response via speaker or display.
+- **Database** – Stores attendance and interaction data securely.
+
+## Expected Outcome
+- Automated and accurate attendance marking
+- Reduced teacher workload
+- Improved student engagement
+- Faster access to learning materials
+- Smart classroom assistance system
 

m
