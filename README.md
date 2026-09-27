# okDriver AI CCTV Platform

A centralized CCTV monitoring, video analytics, and real-time intelligence platform built for the **okDriver Full Stack Developer Hiring Challenge** (aligned with the **Gujarat Police Innovation Hackathon 2026** specifications).

The platform unifies heterogeneous camera feeds, ingests AI inference events (ANPR/watchlist tracking), correlates detections against a central database, plots vehicle movement routes on interactive GIS maps, and pushes low-latency alerts to security operators.

---

## 🌟 Key Features & Functional Modules

### 1. Camera Registry & Health Monitoring
- Onboard and manage camera sources (RTSP, HLS, WebRTC adapters).
- Real-time camera status health tracking (**Online**, **Degraded**, **Offline**)[cite: 1, 3].
- Department and zone-level camera filtering and search[cite: 1, 3].

### 2. Live Video Grid & Analytics Overlays
- Multi-camera stream grid with live frame rates and protocol metadata[cite: 2].
- Real-time bounding box and ANPR confidence score visual overlays[cite: 2].
- Built-in analytics simulator for testing real-time event ingestion.

### 3. GIS Movement & Route Tracing
- Interactive map rendering spatial camera locations and alert markers[cite: 1, 3].
- Chronological route reconstruction for searched license plates (e.g., `GJ01XX0001`) across multiple camera nodes with exact timestamps[cite: 1, 3].

### 4. Real-Time Watchlist & Alert Operations
- Instant critical alert streaming via WebSockets (<5ms latency) without page refreshes[cite: 1, 2, 3].
- Automatic matching against a blacklisted/stolen vehicle watchlist database[cite: 1, 3].
- Complete operator alert lifecycle: **Acknowledge** and **Resolve** states with logged audit records[cite: 1, 3].

---

## 🛠️ System Architecture & Tech Stack

### Tech Stack
- **Backend Framework**: FastAPI (Python), REST APIs, WebSockets, Pydantic
- **Frontend Framework**: React.js, Tailwind CSS, Leaflet.js (GIS Mapping)[cite: 2, 3]
- **Real-Time Data Pipeline**: WebSockets, JSON Event Streaming[cite: 1, 2, 3]
- **Containerization**: Docker / Docker Compose

### System Architecture Diagram
