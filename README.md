# OutageNet

**Resident Outage Detection and Communication System for Gated Residential Colonies**

When power or water fails in a large gated colony, residents can't tell whether the fault is their own, their block's, or colony-wide. Everyone phones the office at once, and a rumour reaches WhatsApp an hour or two later. OutageNet turns those calls into one verified signal: residents report with one tap, a density-based clustering engine classifies the scope, and only the affected blocks are notified.

## Features

**Incident detection (core)**
- One-tap outage and security reporting, with the block taken automatically from the resident's household
- DBSCAN-style clustering by block and time window, with no training data needed
- Scope classification: household fault, block-level outage, or colony-wide outage
- Block-targeted push notifications and a per-event comment thread
- Active-threat flag for security reports that pages the office immediately
- Predictive weather advisories from a daily forecast check
- Outage history, reliability dashboard, and restoration-time estimates
- RAG chatbot answering questions from the colony's own event log, with sources cited

**Colony administration**
- Verified onboarding: the office loads the household register, owners redeem single-use email invitations
- Resident profiles: family members, vehicles, emergency contacts, documents
- Monthly maintenance billing with slab-based tax and online payment
- Community events and facility booking
- Committee elections: one household, one vote per position
- Notifications centre with per-category mute, separate from incident alerts

## Tech Stack

| Layer | Technology |
|---|---|
| Mobile app | React Native (Android + iOS) |
| Admin panel | Next.js, Tailwind CSS |
| Backend | Python, FastAPI, SQLAlchemy, Pydantic |
| Database | PostgreSQL |
| Jobs | Redis, Celery |
| Notifications | Firebase Cloud Messaging (topic per block) |
| Detection | Spatiotemporal density clustering (DBSCAN-style) |
| Chatbot | Retrieval-augmented generation over the event log |
| Deployment | Docker, Nginx, Linux |

## Milestones

| # | Week | Focus |
|---|---|---|
| 1 | 6 | Foundation: schema, FastAPI, CI, onboarding |
| 2 | 12 | Detection engine and incident model |
| 3 | 18 | Notifications, comment threads, chatbot, admin panel |
| 4 | 24 | Mobile client |
| 5 | 30 | Pilot, evaluation, hardening |

## Team

University of Central Punjab (UCP), Lahore, Fall 2026

- Aqif Ahmed (Scrum Master)
- Danish Hamid
- Tayyab Sarwar
- Advisor / Product Owner: Miss Hafiza Maria Kiran

## Process

Scrum with 2-week sprints, tracked on this repo's GitHub Project. Each milestone ends with a tagged release.

## Status

Phase 1 (requirements and documentation) in progress.
