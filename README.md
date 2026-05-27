# Echolens

EchoLens 👁️

"What if the world could explain itself?"

EchoLens is an experimental, AI-powered environmental interpretation layer designed to help people interpret and understand unfamiliar or complex physical spaces. Rather than merely outputting raw, dry lists of objects (e.g., "chair, table, door"), EchoLens focuses on visual context, spatial cognition, and actionable navigation layouts.

It is specifically engineered to reduce cognitive load and spatial anxiety for first-time visitors, elderly individuals, people in high-stress situations, and users with accessibility needs navigating complex hubs like hospitals, railway stations, government offices, and campuses.

🌟 Key Features

1. Dynamic Cognitive Leveling (Persona Profiles)

Toggle between three modes that instantly change the user interface styling and response formatting to suit the user's emotional or physical state:

Standard Mode: Balanced, calm, and insightful overview of the surroundings.

Urgent Mode: Converts the interface to stark, ultra-high-contrast colors and condenses descriptions into short, blunt, single-clause action directives (max 8 words) to bypass panic.

Accessibility Mode: Emphasizes tactile paving, ramps, handrails, elevators, dynamic crowds, and overhead physical hazards.

2. Anchor-Point Orientation

Instead of telling users to "go north" or "turn left", the system identifies a massive, unmissable physical landmark in the frame (e.g., a giant statue, a central reception desk, or a massive pillar) and anchors all directions relative to it (e.g., "Keep the main desk on your left...").

3. Predictive Intent Pathway Mapping

The AI analyzes visible corridors, doors, stairs, and branching routes, creating stylized navigation cards that predict where those physical pathways logically lead.

4. Passive OCR Chronology & Filtering

The vision pipeline filters out irrelevant ambient text (such as outdated flyers, notices, or general posters) and prioritizes immediate, structural, and directional text (such as department names, room numbers, and directional arrows).

5. Pedestrian Crossing Safety Heuristics

When a thoroughfare or roadway separates the user from their destination (e.g., crossing MG Road to reach the Kerala Secretariat), the engine runs a dedicated safety evaluation to warn about high vehicular traffic, un-signaled curb drops, or the lack of audible pedestrian walk signals.

🔒 Zero-Retention Privacy Architecture

Because EchoLens is designed for sensitive, highly populated public spaces, privacy is embedded in its foundation:

Volatile In-Memory Streams: Camera frames are drawn to an internal, volatile memory buffer canvas for immediate API processing.

No local caching: Captured images are never permanently cached or stored on the user's device storage.

No database retention: Images are transmitted as a secure Base64 byte-stream directly to the Gemini API and are immediately discarded upon response delivery.

🛠️ Tech Stack & Files

The current MVP is built as a lightweight, single-file static web application designed for instant loading on mobile devices (via scan-to-view QR codes at building entrances):

Frontend Interface (index.html): Built with HTML5, Tailwind CSS, and vanilla ES6 JavaScript. Designed with a mobile-first premium minimalist aesthetic, tactile button feedbacks, and responsive high-contrast styling.

Hardware Controller: Integrates a seamless front-to-back camera flipping capability utilizing the browser's navigator.mediaDevices hardware API.

VLM Processing: Leverages the state-of-the-art gemini-2.5-flash model directly over secure HTTPS client-side calls.

🚀 Getting Started

Prerequisites

To use the live vision engine, you need a free Gemini API key from Google AI Studio.

Visit aistudio.google.com/apikey and generate a key.

Open the EchoLens app, expand the Gemini Vision API Access panel, paste your key, and click Save. Your key is securely stored only in your local browser sandbox (localStorage).

Running Locally

Since the frontend operates as a static file, you can run it using any simple local HTTP server:

Using Python:

python -m http.server 8000


Using Node.js:

npm install -g local-server
local-server


Or simply open the index.html file using Live Server in VS Code.
