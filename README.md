# Tusks - Build Roadmap (MVP → Full App)

---

## ⚙️ Setup
- [ ] Init GitHub repo
- [ ] Setup Netlify hosting + auto deploy
- [ ] Create Supabase project (Auth + DB + Storage)
- [ ] Define DB schema:
  - [ ] Users (id, type, name, email, phone, skills/job_needs, bio, location, rating)
  - [ ] Jobs (id, client_id, title, desc, budget, category, location, status, created_at)
  - [ ] Applications (id, job_id, seeker_id, status, applied_at)
  - [ ] Reviews (id, job_id, reviewer_id, rating, comment, created_at)
  - [ ] Wallet (id, user_id, balance, transactions)
  - [ ] Ads (id, type, content, status, client_id)
  - [ ] Flags (id, user_id, reason, status) – for scam reports
- [ ] Configure environment variables (Supabase keys, API keys)
- [ ] Add TailwindCSS for styling
- [ ] Setup CI/CD (Netlify deploy previews)

---

## 👤 User Accounts
- [ ] Auth: email + phone sign-up/login
- [ ] Add Google/Facebook OAuth
- [ ] Profile setup (skills for seekers, job needs for clients)
- [ ] Profile view page
- [ ] Optional ID verification system (store docs in Supabase Storage, manual verify)

---

## 💼 Job Posting & Discovery
- [ ] Job post form (title, description, budget, category, location, timeline)
- [ ] Job feed page (list all jobs)
- [ ] Filters: location (manual entry first), category
- [ ] Personalized feed (location + interactions + trending posts)
- [ ] Seekers can post availability
- [ ] Popular/active jobs sorting

---

## 🎯 Matching Algorithm
- [ ] Match by location + job category + reviews
- [ ] Push notifications (Supabase Functions or OneSignal integration)
- [ ] Nearby/relevant opportunities trigger

---

## 💬 Interaction
- [ ] Text posts free for all
- [ ] Contact sharing (optional phone/email field visible if allowed)
- [ ] Direct call link if contact is shared
- [ ] Premium unlock: image/video/audio uploads
- [ ] Media upload to Supabase Storage

---

## 💳 Payments
- [ ] Premium subscriptions (visibility boost, unlimited applications, media uploads)
- [ ] Commission model on job completion
- [ ] Escrow system (funds locked until job done → release minus commission)
- [ ] Wallet system (track deposits, withdrawals, job payments)
- [ ] Payment integrations:
  - [ ] Mpesa Daraja API
  - [ ] Stripe
  - [ ] PayPal
  - [ ] Crypto (Bitcoin, USDT, etc.)

---

## 📢 Ads & Monetization
- [ ] Phase 1: Google Ads / AdMob
- [ ] Phase 2: Direct Ads (Tusks team manually manages)
- [ ] Phase 3: Self-Serve Ads (dashboard for businesses to upload, pay, and run)
- [ ] Ad types:
  - [ ] Banners
  - [ ] Sponsored listings
  - [ ] Video ads

---

## 📜 Compliance & Data Protection
- [ ] Opt-in consent & privacy policy
- [ ] Right to delete account/data
- [ ] Encrypt passwords (Supabase handles)
- [ ] SSL/HTTPS everywhere
- [ ] Controlled data sharing (only with user approval)
- [ ] Audit logs (internal use only)
- [ ] Payments handled via providers (Tusks stores no card/bank info)
- [ ] Align with Kenya Data Protection Act

---

## 🚫 Cancellation & Anti-Scam
- [ ] Job cancellation rules (penalties for late/unfair cancels)
- [ ] Scam prevention:
  - [ ] Flag accounts posting fake jobs
  - [ ] Automatic suspension after repeated misuse
- [ ] Refund policy with mediation
- [ ] Commission refunds when valid

---

## ⭐ Ranking & Reviews
- [ ] Both seekers & clients rate each other (1–5 stars + comments)
- [ ] Reviews affect visibility/feed ranking
- [ ] Badges: Trusted Worker, Reliable Client, etc.
- [ ] Leaderboards:
  - [ ] Top workers
  - [ ] Best clients
  - [ ] Popular jobs
  - [ ] Most active areas

---

## 🗺 Navigation & Map System
- [ ] Use OpenStreetMap + Leaflet.js/Mapbox
- [ ] Custom job pins + seeker icons
- [ ] Route navigation via OSRM/GraphHopper
- [ ] Offline tiles for low-internet zones
- [ ] Seeker navigation to client location

---

## 🏆 Gamification & Engagement
- [ ] Badges for achievements (top-rated, most active, etc.)
- [ ] Weekly highlights (best clients, top jobs, top cities)

---

## 🌍 Translations
- [ ] Auto-translate posts, comments, bios
- [ ] Toggle between original and translated text
- [ ] Initial languages: English, Swahili, Sheng, French
- [ ] Implementation:
  - [ ] Free/open source (LibreTranslate, HuggingFace MarianMT)
  - [ ] Paid fallback: Google Translate API, DeepL
- [ ] Cache translations in DB (to save cost)
- [ ] UI: “Translate” button → show translation

---

## 📱 Tech Stack Migration (Later Phases)
- [ ] Web → SvelteKit frontend (instead of Alpine.js MVP)
- [ ] Mobile → React Native / Flutter app
- [ ] Backend → Node.js (Fastify) + PostgreSQL
- [ ] Hosting → DigitalOcean / Linode / AWS (scale-up)
- [ ] Add GraphQL or REST API layer

---

## 🤖 Long-Term AI & Advanced Features
- [ ] AI-based job matching (like TikTok FYP algorithm)
- [ ] Voice-enabled job search (English, Swahili, Sheng)
- [ ] Verified contracts with e-signatures
- [ ] Worker insurance integration
- [ ] Full self-serve ad platform
- [ ] Multi-currency payments
- [ ] Full offline-first support (low-data users)

