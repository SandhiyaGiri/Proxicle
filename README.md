## 🚀 What is Proxicle?

Proxicle is a proximity-based networking app designed for tech events, conferences, meetups, and hackathons.
It solves a common real-world problem:

“At events, you don’t know who’s around you. You end up talking to random people, and introverts often struggle to break the ice.”

Proxicle fixes this by giving attendees a live demographic overview of the people around them (roles, domains, tech stack), along with auto-generated domain groups where they can observe or participate in discussions.

It acts as a real-time, location-bounded knowledge network that disappears once the event ends.

## 🎯 Core Features (MVP)
### ✅ Live Event Demographics

See a vertical bar graph showing counts of:
- AI Engineers
- Full Stack Developers
- Product Managers
- CXOs
- Data Scientists
- Founders
… dynamically generated based on nearby attendees.

### ✅ Auto-Generated Domain Groups

Proxicle automatically creates groups such as:
- AI Engineers
- Full Stack Developers
- Product Managers
- CXOs

Write Access: Only attendees from that domain
Read-Only Access: Everyone else (e.g., a CXO can view AI discussion)

### ✅ Lightweight Attendee Profiles

Attendees can share:
- Name
- Role
- Tech stack
- Domain
- Problem they are working on
- Years of experience
- LinkedIn, GitHub, X (optional)

### ✅ Event-Scoped, Temporary Network

- Active only when attendees are near the event venue
- Designed to be an ice-breaker
- Encourages in-person networking after digital interaction
- No long-term social graph, no follower system

### 🧱 Tech Stack
### Frontend (PWA)
  - Next.js
  - TypeScript
  - TailwindCSS
  - Zustand (state management)
  - Next-PWA
  - React Query

### Backend
  - Supabase
  - Auth
  - Database
  - Realtime (group chat)
  - Deployment
  - Vercel (frontend)
  - Supabase Cloud (backend + DB)

### 📦 Project Structure (planned)
proxicle/
 ├── app/                 # Next.js app router
 │    ├── login/
 │    ├── profile/
 │    ├── event/
 │    ├── groups/
 │    └── api/
 ├── components/          # UI components
 ├── hooks/               # Custom React hooks (Zustand, queries)
 ├── lib/                 # Supabase client, helpers
 ├── public/              # Icons, manifest.json
 ├── supabase/            # SQL schemas, migrations
 └── README.md

### 🗄️ Database Schema (MVP)
profiles
field	type
id	uuid
name	text
role	text
domain	text
tech_stack	text[] / json
experience	int
linkedin	text
github	text
twitter	text
created_at	timestamp
groups
field	type
id	uuid
name	text
domain	text
created_at	timestamp
group_messages
field	type
id	uuid
group_id	uuid
sender_id	uuid
content	text
created_at	timestamp
📅 Development Plan (Week 1)

###  Goal: Build a working prototype that allows:

Login

Profile creation

Joining default domain groups

Group chat (read/write rules)

Simple attendee list

Static demographics graph

Day-by-day:

Day 1: Set up repo, Next.js, Tailwind, Supabase client

Day 2: Auth + Profile screen

Day 3: Create default groups + Supabase schema

Day 4: Group chat UI + Realtime

Day 5: Attendee list page

Day 6: Demographics graph (mocked)

Day 7: PWA support + polish

🌍 Vision (Future Work)

Real 500m radius proximity using geolocation

Event QR join flow

Role-based permissions for groups

Push notifications

Anonymous “ice breaker” questions

Recruiter-specific features

Sponsor booths discovery

Hall-wise attendee density heatmaps

🤝 Contributing

PRs, feedback, and ideas are welcome!
This project is in early R&D mode — experimentation is encouraged.

📄 License

MIT License.

🧑‍💻 Author

Proxicle — built by developers who believe knowledge should be democratized at events.
