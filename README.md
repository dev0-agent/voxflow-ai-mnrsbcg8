# VoxFlow AI

> Build and interact with conversational voice agents directly in your browser.

## Overview

VoxFlow AI is a client-side web application that empowers users to design, configure, and interact with custom conversational voice agents. By leveraging modern browser APIs for speech recognition and synthesis, it provides a seamless, low-latency voice interaction experience without the need for complex backend infrastructure or API keys.

Whether you are a UX designer prototyping voice interfaces, a developer experimenting with the Web Speech API, or just someone looking to build fun voice personas, VoxFlow AI offers an immediate, zero-setup environment.

## Tech Stack

*   **Framework:** React 18 + Vite
*   **Styling:** Tailwind CSS
*   **UI Components:** shadcn/ui
*   **Icons:** Lucide React
*   **Speech Integration:** Native Web Speech API (`SpeechRecognition` & `SpeechSynthesis`)
*   **State & Persistence:** React Context / Zustand + `localStorage`

## Features

*   🎙️ **Real-time Speech-to-Text:** Speak naturally and see your words transcribed instantly.
*   🤖 **Native Text-to-Speech:** Agents respond audibly using built-in system voices.
*   ⚙️ **Agent Persona Builder:** Customize your agent's name, voice type, pitch, and speaking rate.
*   💬 **Conversation Transcript:** Keep track of the dialogue with a clean chat interface.
*   📊 **Audio Visualizer:** Visual feedback for listening and speaking states.
*   💾 **Local Persistence:** Your agents and chat history are saved securely in your browser.

## Getting Started

### Prerequisites

*   Node.js (v18 or higher recommended)
*   A modern browser with Web Speech API support (Google Chrome, Microsoft Edge, or Safari).

### Installation

1.  Clone the repository:
    ```bash
    git clone https://github.com/yourusername/voxflow-ai.git
    cd voxflow-ai
    ```

2.  Install dependencies:
    ```bash
    npm install
    ```

3.  Start the development server:
    ```bash
    npm run dev
    ```

4.  Open your browser and navigate to `http://localhost:5173`.

## Documentation

*   [TASKLIST.md](./TASKLIST.md) - Project tasks and progress tracking.
*   [LEARNINGS.md](./LEARNINGS.md) - Developer notes and architectural decisions.
*   [.dev0/RULES.md](./.dev0/RULES.md) - AI agent coding guidelines and project rules.

## Browser Support Note

This application relies heavily on the `window.SpeechRecognition` and `window.speechSynthesis` APIs. For the best experience, please use a Chromium-based browser (like Google Chrome or Microsoft Edge). Microphone permissions must be granted for the voice input features to function.