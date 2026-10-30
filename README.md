# Curbwire Agent — Ambient Civic Intelligence Prototype

A pixel-perfect, interactive WhatsApp Web/Mobile chat interface demonstrating the **Curbwire Agent** in action as an ambient civic intelligence bot for neighborhood group chats.

![WhatsApp Civic Agent Demo](https://images.unsplash.com/photo-1519331379826-f10be5486c6f?auto=format&fit=crop&w=600&q=80)

## 🌟 Overview & Topic

This prototype simulates a lively neighborhood WhatsApp group chat in **Monta Vista (Cupertino, CA)**. When neighbors discuss local fencing and construction at Stevens Creek and Vista, they summon **@Curbwire** to query verified municipal open data in real time. 

The bot delivers instant permit clarity, environmental review milestones, upcoming public hearing details, and proactive public works road resurfacing alerts.

---

## 🎨 Visual Design & Features

- **WhatsApp Design System**:
  - Classic dark green header (`#075E54` / `#128C7E`)
  - Subtle doodle patterned wallpaper (`#EFEAE2`)
  - Rounded speech bubbles with speech bubble tails (white for received, `#DCF8C6` for user messages)
  - Color-coded member names (Sarah, Dave, Priya)
  - Group avatar with Cupertino park photography and active status indicator
  - Standard action icons (video call, voice call, search, menu)
- **Curbwire Civic Bot Representation**:
  - **Verified Civic Agent** badge with animated pulse
  - Structured municipal records (Permit #, Scope, CEQA status, hearing dates)
  - Interactive **"View City Staff Report"** modal with official document layout
  - Interactive **"Track This Project"** toggle with toast notifications
  - Proactive **Civic Alerts** for DPW street resurfacing and parking restrictions
- **Device Frame & Responsive View**:
  - Realistic iPhone mobile bezel with dynamic island / notch
  - Desktop / Full-screen toggle button to preview in standard web view
  - Real-time mobile status bar clock
  - Native Web Audio API sound effects (WhatsApp message send & receive chimes)
- **Live Interactivity**:
  - Working text input with dynamic Mic ⇄ Send button state
  - Instant pre-scripted quick prompt chips:
    - `🔍 Permit on 10450 Stevens Creek`
    - `🚧 Road closures this week`
    - `🌳 Saturday park cleanup`
    - `🧹 Street sweeping schedule`
  - Dynamic simulation engine: types `@curbwire` or civic keywords to get real-time responses with realistic typing indicator (`"Curbwire Bot is typing..."`)
  - In-chat message search filter
  - Group info modal detailing group participants and bot permissions
  - Zero build steps: 100% self-contained in `index.html` via Tailwind CSS CDN.

---

## 💬 The Conversation Flow

1. **Sarah (Member)**: *"Hey neighbors, does anyone know what’s going on at the corner of Stevens Creek and Vista? They put up temporary fencing around the old bank branch this morning."*
2. **Dave (Member)**: *"Probably another bank or empty retail space 🙄 Anyone else tired of construction on that strip?"*
3. **Priya (Member)**: *"@Curbwire what's the active permit on 10450 Stevens Creek?"*
4. **Curbwire Bot (Verified Civic Agent)**:
   - 📍 **Permit Record**: City of Cupertino Planning & Building
   - **Permit #2026-PLN-0388** (Filed Oct 14, 2026)
   - **Scope**: Commercial alteration converting 4,200 sq ft retail branch to a community bakery & market with 16 outdoor patio seats.
   - **Status**: Environmental review approved. Final architectural review before Planning Commission on Nov 12.
   - *[Link: View City Staff Report]* &nbsp; *[Button: Track This Project]*
5. **Dave**: *"Wait, an actual bakery with patio seating? That's huge."*
6. **Sarah**: *"Thanks @Curbwire! Way better than guessing on Nextdoor."*
7. **Curbwire Bot (Proactive Civic Alert)**:
   - ⚠️ **Heads-up**: Public works street resurfacing is scheduled for McClellan Rd between Vista and Bubb from 8 AM - 3 PM this Thursday. Street parking will be restricted.

---

## 🚀 How to Run Locally

Because this project is self-contained with no build steps, you can run it immediately:

### Option 1: Direct File Open
Double-click `index.html` or open it directly in any modern browser (Chrome, Safari, Edge, Firefox).

### Option 2: Local Server
```bash
# Using Python 3
python -m http.server 8080

# Using Node.js (npx)
npx serve .
```
Navigate to `http://localhost:8080`.

---

## ☁️ Deploying to Netlify

### Fast Deploy via Netlify CLI:
```bash
# If Netlify CLI is installed
npx netlify deploy --prod --dir=.
```

### Git-Connected Deploy via Netlify Dashboard:
1. Initialize and push your repository to GitHub / GitLab:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Curbwire WhatsApp Civic Agent interface"
   git remote add origin <your-github-repo-url>
   git branch -M main
   git push -u origin main
   ```
2. Go to [Netlify](https://app.netlify.com).
3. Click **"Add new site"** → **"Import an existing project"**.
4. Select your Git repository.
5. Set:
   - **Build command**: *(leave blank)*
   - **Publish directory**: `.` (or current directory, configured automatically in `netlify.toml`)
6. Click **Deploy Site**. Your site will be live instantly with global CDN and SSL!
