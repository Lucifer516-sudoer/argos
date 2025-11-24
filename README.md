# Argos

A local-first Mind Engine: CLI → API → persistence → simple ML → policy → actions → feedback loop.

## Overarching Goal

Build an end-to-end system that ingests user state, infers context, performs intelligent actions, and learns from feedback.

## Success Metrics

- [ ] E2E loop working (ingest → infer → action) by end of Sprint 1
- [ ] ≥1 stored session in Qdrant by Sprint 3
- [ ] Action follow-through rate > 40% within first month
- [ ] Automated test coverage ≥40% after Sprint 4

## Sprint Roadmap

### Sprint 0 — Prep (0.5 day)
**Goal:** Repo scaffold and environment setup
- [x] Initialize repo with `uv init`
- [x] Install dependencies: fastapi, uvicorn, rich, qdrant-client, pytest
- [x] Create directory structure
- [x] Write initial README (vibe coded this part)

**Duration:** 0.25 hours | **Status:** ✅️

---

### Sprint 1 — E2E Minimum Loop (1 week)
**Goal:** CLI input → rule-based inference → action (focus timer)
- [ ] Implement `infer_state()` with keyword rules
- [ ] Implement `perform_action()` mapping
- [ ] Build CLI with rich output
- [ ] Create action runner (timer)
- [ ] Add basic tests

**Deliverable:** `python -m mind_engine.cli` runs full loop

**Duration:** _____ days | **Status:** 👨‍💻 (🕝️ WIP)

---

### Sprint 2 — API + Persistence (1 week)
**Goal:** FastAPI exposure and SQLite sessions storage
- [ ] Create FastAPI `/ingest` endpoint
- [ ] Implement SQLite persistence layer
- [ ] Wire CLI to call API
- [ ] Add logging and Docker Compose setup

**Deliverable:** API stores and returns sessions

**Duration:** _____ days | **Status:** 👨‍💻 (🕝️ WIP)

---

### Sprint 3 — Embeddings & Vector Context (1 week)
**Goal:** Qdrant integration and semantic retrieval
- [ ] Add embedding with FastEmbed
- [ ] Set up Qdrant locally
- [ ] Implement session upsert to Qdrant
- [ ] Build retrieval endpoint
- [ ] Add vector store tests

**Deliverable:** Sessions stored and retrievable in Qdrant

**Duration:** _____ days | **Status:** 👨‍💻 (🕝️ WIP)

---

### Sprint 4 — Policy Engine & Feedback (1 week)
**Goal:** Deterministic policy and feedback loop
- [ ] Implement policy engine
- [ ] Add feedback endpoint
- [ ] Record follow-through and ratings
- [ ] Add action cooldown scheduler

**Deliverable:** Policy influenced by past feedback

**Duration:** _____ days | **Status:** 👨‍💻 (🕝️ WIP)

---

### Sprint 5 — Voice Input & ML Classifier (1 week)
**Goal:** Whisper transcription and hybrid inference
- [ ] Add voice recording and transcription
- [ ] Bootstrap scikit-learn classifier
- [ ] Collect labeled training data
- [ ] Add labeling endpoint

**Deliverable:** Voice ingestion and trainable classifier

**Duration:** _____ days | **Status:** 👨‍💻 (🕝️ WIP)

---

### Sprint 6 — Actions Library & Automations (1 week)
**Goal:** Diverse actions and real automations
- [ ] Implement 4+ action types (timer, journal, shell, note, walk reminder)
- [ ] Add async action runner
- [ ] Build rich terminal dashboard

**Deliverable:** Multiple actions working with dashboard

**Duration:** _____ days | **Status:** 👨‍💻 (🕝️ WIP)

---

### Sprint 7 — Personalization & Evaluation (1 week)
**Goal:** Improve metrics and personalization
- [ ] Implement bandit-style reward weighting
- [ ] Generate weekly summary reports
- [ ] Add integration tests
- [ ] Implement privacy encryption

**Deliverable:** Weekly reports and improved selection

**Duration:** _____ days | **Status:** 👨‍💻 (🕝️ WIP)

---

### Sprint 8+ — Polish & Optimization
**Goal:** Harden, iterate, and optimize
- [ ] Improve classifier (transformer-based if needed)
- [ ] Add calendar/terminal integrations
- [ ] Optional: Rust module for performance-critical paths

**Deliverable:** Production-ready system

**Duration:** _____ days | **Status:** 👨‍💻 (🕝️ WIP)

## Installation

```bash
uv init argos
cd argos
uv add fastapi uvicorn rich qdrant-client pytest
```

## License

MIT