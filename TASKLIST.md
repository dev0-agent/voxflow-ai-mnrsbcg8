# Task List

This file shows the current progress of all tasks in this project.
It is automatically updated by dev0 as tasks are completed.

---

## Phase 1

- [ ] ⏳ **Project Scaffold and Layout Setup**
  Clean up the default Vite template. Create a responsive main layout with a sidebar for Agent Configuration and a main content area for the Conversation Interface. Include a header with the VoxFlow AI branding.

- [ ] ⏳ **Implement Local Storage State Management**
  Create a state management utility (using React Context or Zustand) to manage Agent Profiles (id, name, voiceURI, pitch, rate, systemPrompt) and Conversation History. Ensure state automatically syncs with `localStorage`.

## Phase 2

- [ ] ⏳ **Build Agent Configuration Form**
  Create a form in the sidebar to create and edit Agent Profiles. Include inputs for Name, a textarea for System Prompt (persona), a select dropdown for available system voices (`window.speechSynthesis.getVoices()`), and sliders for Pitch (0 to 2) and Rate (0.1 to 10).

- [ ] ⏳ **Implement Speech Recognition Hook**
  Create a `useSpeechRecognition` custom hook wrapping the Web Speech API. It should expose state for `isListening`, `transcript` (current spoken text), and functions to `startListening` and `stopListening`. Handle browser compatibility (`webkitSpeechRecognition`).

- [ ] ⏳ **Implement Speech Synthesis Hook**
  Create a `useSpeechSynthesis` custom hook. It should accept text, voiceURI, pitch, and rate, and use `window.speechSynthesis.speak()`. Expose an `isSpeaking` boolean state and a `cancel` function to stop current speech.

## Phase 3

- [ ] ⏳ **Build Conversation Transcript UI**
  Create a chat interface in the main content area displaying messages from the user and the agent. Differentiate them visually (e.g., user on right, agent on left). Include an empty state prompting the user to start talking.

- [ ] ⏳ **Integrate Speech Hooks and Mock Response Engine**
  Connect the UI to the speech hooks. When the user stops speaking, append their text to the chat, generate a mock response based on the agent's persona (e.g., simple keyword matching or echoing), append the agent's response to the chat, and trigger the `useSpeechSynthesis` hook to speak it out loud.

## Phase 4

- [ ] ⏳ **Implement Audio Visualizer Component**
  Create a CSS-animated audio visualizer component (e.g., pulsing bars or circles). It should take `isListening` and `isSpeaking` props to change its animation state (e.g., green pulsing when listening, blue waveforms when the agent is speaking, static when idle).

- [ ] ⏳ **Polish UI and Controls**
  Refine the application using shadcn/ui components. Add a prominent 'Push to Talk' or 'Toggle Mic' button with clear active/inactive states. Ensure the layout is responsive and looks good on smaller screens.

## Phase 5

- [ ] ⏳ **Add Error Handling and Browser Compatibility Checks**
  Implement an initialization check for Web Speech API support. If unsupported, display a clear warning banner to the user. Add error boundaries and toast notifications for microphone permission denials or synthesis errors.

---

_Last updated by dev0 automation_
