# Graphite Studio Podcast (GSP)

![React](https://img.shields.io/badge/React-19-20232a?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178c6?style=for-the-badge&logo=typescript)
![Vite](https://img.shields.io/badge/Vite-6.0-646cff?style=for-the-badge&logo=vite)
![Gemini](https://img.shields.io/badge/Google_Gemini-Pro_&_Flash-8e75b2?style=for-the-badge&logo=google)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-3.0-38bdf8?style=for-the-badge&logo=tailwindcss)

### Autonomous Multi-Modal Content Production Engine

**Graphite Studio** is a high-performance, proprietary Single Page Application (SPA) designed to solve the information density problem. It functions as an autonomous production studio that ingests raw unstructured data—text, web links, images, and audio—and transforms it into broadcast-quality audio narratives using a sophisticated multi-agent AI workflow.

Unlike standard text-to-speech wrappers, Graphite utilizes a client-side **Chain-of-Thought** pipeline to reason, plan, script, and direct audio content, effectively simulating a human production team within the browser.

---

### Project Status: Private Prototype

> **Notice:** This software is currently under active private development. This documentation serves as a technical overview of the application's capabilities and architecture. It is not open-source software.

---

### The Agentic Workflow

Graphite Studio distinguishes itself through `geminiService.ts`, which orchestrates a four-stage cognitive pipeline rather than a simple summarization task. The application uses specific AI agents to handle different stages of production:

1.  **The Researcher (Data Normalization):**
    Ingests raw multimodal content. It strips noise from web scrapes, OCRs uploaded images, and consolidates contradictory data into a structured "Research Dossier."

2.  **The Architect (Strategic Planning):**
    Analyzes the dossier against user-defined "Producer Guidelines." It constructs a narrative arc (Hook &rarr; Context &rarr; The Turn &rarr; Climax) to ensure the content flows logically rather than randomly.

3.  **The Writer (Script Synthesis):**
    Drafts the dialogue based on the Architect's blueprint. It enforces "Show, Don't Tell" principles and assigns distinct lexical personalities to the hosts (e.g., The Anchor vs. The Color Commentator).

4.  **The Director (Humanization):**
    A final pass that injects human nuance. This agent adds disfluencies, interruptions, and phonetic emphasis instructions to drive the Text-to-Speech engine, creating a natural, non-robotic listening experience.

---

### Technical Architecture

Graphite Studio pushes the boundaries of client-side processing, minimizing server dependencies for media manipulation.

#### Client-Side Audio Engineering
*   **Parallel Generation:** The application creates audio segments asynchronously to manage API rate limits and reduce time-to-first-byte.
*   **Binary Stitching:** Raw PCM data is decoded into `AudioBuffer` objects, stitched sequentially in memory using the Web Audio API, and re-encoded into WAV containers locally.
*   **Zero-Latency Visualization:** A dedicated `AudioContext` drives real-time canvas waveform rendering, providing immediate visual feedback during playback.

#### Hybrid Persistence Strategy
*   **IndexedDB:** Due to LocalStorage limits (5MB), Graphite utilizes `IndexedDB` to store heavy binary assets (generated WAV files) and synchronized transcript metadata.
*   **LocalStorage:** Used for lightweight configuration, maintaining user preferences for themes ("Graphite", "Midnight", "Porcelain") and UI styles ("Glass" vs "Simple").

#### Retrieval-Augmented Generation (RAG)
The **Discussion Panel** implements a RAG system grounded by Google Search. This allows users to interrogate their source material, fact-check generated scripts against the live web, and explore tangential topics without leaving the application context.

---

### Core Modules

*   **Unified Source Ingestion:** A centralized interface accepting direct text, URL scraping via proxy, image-to-text vision analysis, and microphone recording via the MediaStream Recording API.
*   **Interactive Learning Objects:** The application transforms static scripts into active learning tools, including `MindMapPanel` (SVG-based recursive tree visualization), `QuizPanel` (Gamified assessments), and `FlashcardsPanel` (Spaced repetition tools).
*   **Deep Customization:** Users have granular control over AI model selection (Gemini 3.0 Pro vs 2.5 Flash), host personas, and podcast length/format.

---

### Interface Gallery

<div align="center">
  <img src="https://github.com/user-attachments/assets/064ff45b-1682-40d5-9916-05145d70f6e4" width="48%" />
  <img src="https://github.com/user-attachments/assets/36cc9ffd-e871-4bd7-95a4-ce93476d3b3d" width="48%" />
  <img src="https://github.com/user-attachments/assets/4c9ff875-aff6-4e2c-b1ab-262cfced7796" width="48%" />
  <img src="https://github.com/user-attachments/assets/3326f90b-0c20-4638-a719-41125419f4a0" width="48%" />
  <img src="https://github.com/user-attachments/assets/10fc34fa-07d1-4456-a415-8c4ee878e95d" width="48%" />
  <img src="https://github.com/user-attachments/assets/99e75f0e-126d-44fa-b153-e1054a4f0ec3" width="48%" />
  <img src="https://github.com/user-attachments/assets/82158a8a-f6ec-4351-86e0-3b770110651f" width="48%" />
  <img src="https://github.com/user-attachments/assets/329ba793-70d3-407c-ad2b-29af8f57f1a3" width="48%" />
  <img src="https://github.com/user-attachments/assets/21e15856-b912-4efe-ad43-c9d024c364a7" width="48%" />
  <img src="https://github.com/user-attachments/assets/9dee9f95-984d-4030-b8e3-87bcf703102b" width="48%" />
  <img src="https://github.com/user-attachments/assets/1fe41c78-191d-45c0-a68c-66d52cc21ae3" width="48%" />
  <img src="https://github.com/user-attachments/assets/5eabd160-8a61-4908-b124-c20d7ea2e05b" width="48%" />
  <img src="https://github.com/user-attachments/assets/efed3434-c789-4f65-8ad3-6d2d0a8ccb1f" width="48%" />
  <img src="https://github.com/user-attachments/assets/acf36d56-8de0-47f0-b83e-f7437ccb75bc" width="48%" />
</div>

---

**Developed by Matthew Wesney**
*Full Stack Engineer & AI Systems Architect*
