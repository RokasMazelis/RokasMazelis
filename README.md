### Hi, I'm Rokas 👋

I build production AI systems for businesses: voice agents, SMS automation,
pricing intelligence, RAG and agentic workflows. If a process is repetitive,
there's usually a better way. Based in Vilnius 🇱🇹.

Most of my work is client code, so most repositories are private (🔒).
**Source code and walkthroughs are available on request.**

---

## ⭐ Featured

### 📞 Telefonauzeris: AI voice calling agent · 🔒
Platform for outbound AI phone campaigns. Users set up a voice agent, upload a CSV
of contacts and launch batch calls. Each call returns a transcript, sentiment and a
structured summary.

- Real-time call audio streamed over WebSockets: telephony → speech-to-text → LLM → text-to-speech
- Pluggable providers: 4 TTS engines (ElevenLabs, Azure, Gemini, Sinteze) and
  5 STT engines (Google Chirp, Deepgram, Whisper, OpenAI Realtime), Silero VAD for turn-taking
- Lithuanian first, English second; 2–3 s end-to-end response time; built-in latency tracking
- **Stack:** FastAPI · Telnyx · ElevenLabs Conversational AI · OpenAI · Next.js 15 · Supabase · Render

### 💬 SMS AI: appointment confirmation assistant · 🔒
Watches a client's Outlook calendar, texts customers before their appointment and
understands their replies (confirm, cancel or reschedule) to keep the calendar up to date.
In production with a paying client. **No-shows fell by 40%.**

- LLM intent parsing of free-text replies, with follow-up and reschedule flows, plus an intent eval script
- **Microsoft Graph** calendar access, restricted to one user-selected calendar
- Client portal: magic-link login, conversation history, pause or resume automation, admin impersonation
- **Stack:** Python · OpenAI · TextMagic · Microsoft Graph · Next.js 15 · Supabase (RLS) · Render · pytest / Vitest

### 🎸 Pricing and catalogue automation for a music-instrument store · 🔒
Production system behind a Lithuanian WooCommerce store with **6,000+ products**.

- Competitor price monitoring: scrapes Thomann for 20 brands, pre-filters
  candidates by token similarity, then **Claude** confirms exact product matches
  and price proposals respect a margin floor
- Ingests stock and price feeds from several distributors (FTP, XML, CSV, JSON) on nightly and weekly schedules
- Custom WordPress plugins: real-time product sync to a pricing database, a stock-source /
  delivery-time card on product pages, checkout improvements
- SEO pipeline: crawls competitor product pages and generates Lithuanian product
  titles, with a review step before anything is published
- **Stack:** Python · Claude API · Oxylabs · WooCommerce REST · PHP · MariaDB · cron

### 🏦 Senatoriai: invoice and payment reconciliation · 🔒
Production system that matches incoming bank payments to open invoices across
departments, replacing manual reconciliation. I led a team of 3, working between
the business owners and the developers on requirements, priorities and new features.

- Pulls bank statements from Luminor through a signed SOAP / ISO 20022 (camt.054) integration
  with XML signature handling, polled every 15 minutes
- Ingests invoices from two source systems (an r_keeper POS and RASO) and normalises invoice numbers
- Automatic matching from payment remittance text, with a manual "match" flow for the rest;
  debt overview by department and customer, Excel export
- **Stack:** Go · MySQL · Next.js 16 · React 19 · Docker · VPS · Swagger

### 🏗️ IN ARCH: AI-coordinated workspace for interior design projects · 🔒
One shared workspace for architects, clients, contractors and suppliers. People can
chat or send Lithuanian voice notes, or edit records directly, and both routes update
the same project. An AI coordinator tracks stages, dependencies and decisions,
and asks for confirmation where the project's rules require it.

- Web app: dashboard, projects, task board and list, timeline, files and team chat;
  51 unit tests plus Playwright smoke tests, mobile-first
- Architecture: event-sourced project history, one backend plus a background worker,
  and agents that act through the same operations people use
- **Stack:** Next.js 16 · React 19 · Tailwind 4 · Vitest · Playwright · PostgreSQL

### 📊 DIVA: business data analysis agent · 🔒
Upload sales, expense or customer data (CSV, Excel, SQL, PDF). An agent profiles it
and returns an interactive dashboard with plain-language findings and recommendations.
Built for small businesses that have the data but no analyst.

- Built on the **Claude Agent SDK**; answers in the user's language
- Magic-link auth, trial credits, per-session uploads with cleanup
- **Stack:** Claude Agent SDK · Next.js 16 · ApexCharts · Postgres · Docker · Caddy

### 🏠 Facade Visualizer: AI renders for building-material sellers · 🔒
A homeowner uploads a photo of their house, picks a facade material and gets an
AI-generated render of the house in that material in about 30 seconds. Sold as a
monthly subscription to building-material businesses, with branded pages per brand
and WooCommerce integration.

- **Stack:** FastAPI · Gemini image generation · Pillow · WooCommerce

---

## ✈️ Travel

### Bičiulių Kelionės: adventure-travel booking site · 🔒
Live client site. Visitors browse trips, register, and pay a deposit or the full
price online. Trip content is managed in a CMS admin.

- **Stack:** Next.js 15 · React 19 · Payload CMS · MongoDB · Cloudflare R2 · Paysera + Stripe · Resend

### AI travel agent (kelioniuPY) · 🔒
Multi-agent travel planner. Specialised agents for flights, bookings, places and
road trips coordinate through OpenAI tool calling, pulling TripAdvisor content.

- **Stack:** FastAPI · OpenAI function calling · MongoDB · Render

### Holiday planner MVP (holidaymvp) · 🔒
Streamlit journey planner that combines flight, hotel and weather lookups with a
**RAG** guide built from Italy travel content, to suggest trips within a budget.

- **Stack:** Streamlit · LangChain · OpenAI embeddings · vector store

---

## 🧪 Experiments and smaller builds

| Project | What it is | Stack |
|---|---|---|
| [streamlit-rag](https://github.com/RokasMazelis/streamlit-rag) | **RAG** chat over web pages: load, chunk, embed into Chroma, answer questions | LangChain · Chroma · OpenAI · Streamlit |
| docscan / skaitytuvas 🔒 | Document scanner: camera or upload → GPT vision extraction → CSV / Google Sheets | OpenAI Vision · OpenCV · Streamlit |
| [config](https://github.com/RokasMazelis/config) | WordPress plugin connecting a 3D product configurator to WooCommerce, with rule-based pricing | PHP · WooCommerce REST |
| task-board 🔒 | Local Trello-style board that Claude Code drives through a skill and CLI | Next.js · SQLite · Vitest |
| [bober](https://github.com/RokasMazelis/bober) | Always-on conversion-rate-optimisation agent for websites (early stage) | Claude Agent SDK |
| WeeatherCalling 🔒 | First experiment with LLM tool calling: weather lookups | Python · OpenAI |

---

## Tools I use most

`Python` `TypeScript` `Next.js` `FastAPI` `Claude API / Agent SDK` `Claude Code` `OpenAI`
`LangChain` `Supabase` `Postgres / MariaDB / MongoDB` `WooCommerce / WordPress`
`Docker` `Render` `Vercel`
