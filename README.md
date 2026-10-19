PacketVerse 🌐

PacketVerse is an interactive, browser-based educational platform designed to teach computer networking concepts. Serving as a patient networking tutor tailored for engineering students, the application operates entirely on the client side to simulate network protocols, packet behaviors, and data transfers.

No backend server, no build steps, and no databases are required. Just pure HTML, CSS, and JavaScript.

✨ Features

Interactive Curriculum: 17 detailed levels covering 4 main sections (Foundations, Link and Network, Transport, Application and Security).

Pure Simulation Engine: Step-by-step simulations of network state machines. Watch normal network flows or actively break connections by dropping, delaying, or corrupting packets (e.g., modifying ACK numbers or TCP flags).

Hands-on Widgets: Experimental mini-labs including:

CIDR subnet calculator.

Performance metric sliders (calculating latency, throughput, and bandwidth-delay product).

Bit-flipping tool to test error detection (Parity, Checksum, CRC).

Live URL request tracer.

Optional AI Tutor: An integrated, context-aware AI tutor powered by your own API key (supports OpenAI, Anthropic, and Gemini). The AI can answer questions based on the learner's current step and convert natural language "What if?" questions into broken-network scenarios.

Gamification & Progress Tracking: Pass dynamically shuffled 3-question quizzes to unlock levels. Progress, scores, and daily streaks are saved locally in the browser.

Personalized Appearance: Customizable UI themes with presets (Soft sage, Warm paper, Blue grey, Night) and granular color controls.

🚀 Getting Started

Since the project is a purely static frontend application, setting it up is incredibly simple.

Clone the repository:

git clone https://github.com/yourusername/packetverse.git



Open the application:
Navigate to the project folder and open index.html in any modern web browser.

cd packetverse
open index.html



📂 Project Structure

index.html: The application layout (level map, stage, AI chat panel, quizzes, dialogs).

app.js: Core UI logic, state management, progress tracking, and event delegation.

style.css: Design system, responsive layouts, animations, and CSS-variable-based theming.

engine.js: The simulation engine that calculates step snapshots for TCP handshakes, UDP flows, HTTP, and handles loss/delay scenarios.

levels.js: The curriculum database containing level goals, definitions, analogies, and quiz questions.

widgets.js: Logic for all interactive mini-labs (congestion window graphs, interactive server games, CIDR calculators).

ai.js: Optional AI integration layer handling API requests to LLMs and prompt management.

🤖 Configuring the AI Tutor (Optional)

The AI features are completely optional; the site works perfectly without them. If you want to enable the AI Tutor:

Open the application in your browser.

Click the Gear (⚙️) icon in the top right corner.

Enter your API Key, the Endpoint (e.g., https://api.openai.com/v1/chat/completions), and the Model you wish to use.

Click Save.

Note: Your API key is stored securely in your browser's localStorage and is never sent anywhere except directly to the AI provider.

🛠️ Built With

HTML5

CSS3

Vanilla JavaScript (ES6+)

📄 License

This project is open-source and available under the MIT License.
