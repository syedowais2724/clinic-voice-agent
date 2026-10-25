# ClinicVoice

A voice AI receptionist for clinics. Patients talk to it in the browser to check in, book, reschedule, or cancel doctor appointments.

- `backend/` – Python voice agent built with LiveKit Agents (patient check, doctor booking, rescheduling, billing).
- `frontend/` – Next.js web app where patients talk to the agent.

## Run locally

1. Create a free project at [LiveKit Cloud](https://cloud.livekit.io) and copy its URL, API key, and API secret.
2. Backend:
   ```bash
   cd backend
   cp .env.example .env               # fill LIVEKIT_URL, LIVEKIT_API_KEY, LIVEKIT_API_SECRET and your model API key
   uv sync
   uv run agent.py dev
   ```
3. Frontend (in a second terminal):
   ```bash
   cd frontend
   cp .env.example .env.local         # fill LIVEKIT_URL, LIVEKIT_API_KEY, LIVEKIT_API_SECRET
   pnpm install
   pnpm dev
   ```
4. Open http://localhost:3000 and start talking.

## Credits

Built on LiveKit's open-source healthcare example and Agent Starter for React. See [NOTICE](NOTICE).
