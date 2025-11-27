
# Graphite Studio

<div align="center">
  <h3>The AI-Powered Audio Production & Knowledge Engine</h3>
  <p><em>Transform raw chaos into high-fidelity podcasts and structured learning tools.</em></p>
</div>

---

> **Note:** This is a proprietary technical showcase. This repository does NOT contain the source code for the commercial-grade application demonstrating advanced React 19 patterns and Agentic AI workflows.

## Overview

**Graphite Studio** is a sophisticated Single Page Application (SPA) that acts as an autonomous production studio. It ingests unstructured data—articles, white papers, images, or messy voice notes—and orchestrates a team of AI agents to produce a broadcast-quality podcast with two distinct AI hosts.

Beyond audio, Graphite Studio serves as a "Knowledge Engine," instantly converting the source material into interactive Mind Maps, gamified Quizzes, and spaced-repetition Flashcards.

## ✨ Key Features

### Agentic Podcast Production
Graphite doesn't just "summarize." It uses a **multi-step Chain-of-Thought workflow** to emulate a real production team:
1.  **The Researcher:** Sanitizes input and builds a "Dossier."
2.  **The Architect:** Plans the episode structure (Hook, Turn, Climax).
3.  **The Writer:** Drafts natural dialogue with distinct host personas.
4.  **The Director:** Injects speech disfluencies (um, uh), interruptions, and pacing instructions for the TTS engine.

### Knowledge Tools
*   **Infinite Mind Maps:** An interactive, zoomable SVG canvas that visualizes concepts. Nodes can be recursively expanded by AI.
*   **RAG Discussion Panel:** A chat interface grounded in Google Search to verify facts from the source text.
*   **Gamified Quizzes:** Generates MCQs and True/False questions with streak tracking and explanations.

### Advanced Audio Engineering
*   **Client-Side Mixing:** Stitches multiple PCM audio buffers into a single `.wav` file within the browser.
*   **Waveform Visualization:** Real-time frequency analysis using the Web Audio API.
*   **Deep Customization:** Control host personalities, voices, script complexity, and output language (EN, ES, FR, DE, JA).

## Technical Architecture

### Core Stack
*   **Frontend:** React 19, TypeScript, Vite.
*   **Styling:** TailwindCSS with a custom CSS Variable theming engine (Glassmorphism support).
*   **AI Layer:** Google GenAI SDK (Gemini 2.5 Pro / 2.5 Flash).
*   **Persistence:** IndexedDB (via native wrappers) for storing large binary audio blobs.

### The "Magic" Under the Hood
Graphite Studio bypasses traditional backend requirements by handling heavy lifting on the client:
*   **Vision Analysis:** Images are encoded to Base64 and processed by Gemini Vision for description ingestion.
*   **Audio Transcription:** Browser `MediaRecorder` captures mic input, which is sent to Gemini Flash for instant transcription.
*   **Binary Manipulation:** Custom utilities generate RIFF WAVE headers manually to allow local downloading of generated content without server processing.

## Interface

| **The Studio** | **Knowledge Engine** |
|:---:|:---:|
| *Multi-agent script generation & waveform analysis* | *Interactive Mind Maps & Quizzes* |


## License & Usage

**Proprietary / Closed Source.**
This repo is provided for portfolio and technical demonstration purposes only. Redistribution, modification, or commercial use without explicit permission is strictly prohibited.

---

<div align="center">
  <small>Built with ❤️ by Matthew Rotert Wesney</small>
</div>

