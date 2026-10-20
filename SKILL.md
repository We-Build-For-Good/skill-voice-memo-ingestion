---
name: voice-memo-ingestion
description: "Operational protocol for ingesting rapid, spoken founder voice notes and stream-of-consciousness dictation (Wispr Flow, voice memos, transcriptions). Parses raw speech into atomic intent: cleanly separating exploratory brainstorming, strategic pivots, and immediate execution tickets without flattening the founder's authentic voice."
license: MIT
metadata:
  author: We Build for Good
  version: "1.1.0"
---

# Voice Memo Ingestion: Stream-of-Consciousness Parsing Protocol

Founders often move faster by speaking than by typing. 

Using voice-to-text tools (like Wispr Flow, Apple Dictation, or audio recordings), a founder will dictate a five-minute audio memo that mixes strategic frustration, creative ideas, minor UI tweaks, and direct technical orders in a single breath.

Standard AI assistants mishandle spoken input in two opposite ways:
1. **The Over-Eager Assistant**: It treats every speculative brainstorm as an immediate engineering ticket, creating chaos in the backlog.
2. **The Passive Summarizer**: It turns a dense, urgent voice memo into a dry bulleted summary, losing the actionable instructions entirely.

The `voice-memo-ingestion` protocol cleanly separates spoken stream-of-consciousness input into structured, actionable intent.

---

## The Prime Philosophy

**Preserve the authentic voice, but categorize the intent into four distinct buckets.**

The AI must never invent certainty where the speaker was deliberately exploring an ambiguity. If the founder says "Maybe we should kill the waitlist, or maybe we just make it free?", the AI must log it as an open question, not execute a database deletion.

---

## The Four Intent Buckets

When ingesting a voice memo transcript, parse every thought into one of four buckets:

### Bucket 1: Strategic Mindset & Context
* How the founder is feeling, the emotional texture, the high-level perspective.
* *Example*: "Feeling frustrated that our mobile checkout feels clunky compared to Apple Pay."
* *Action*: Preserved in session memory to calibrate the AI's tone and priorities.

### Bucket 2: Exploratory Brainstorming (Not Tickets)
* Ideas, hypotheses, creative possibilities, and future concepts.
* *Example*: "What if we added a pastel isometric map for the studio?"
* *Action*: Recorded in a strategic backlog or ideas register. Never dispatched as code changes without explicit confirmation.

### Bucket 3: Immediate Execution Tickets (Grounded Action)
* Concrete, unambiguous instructions that can be executed immediately.
* *Example*: "Fix the z-index so the rings sit in front of the artwork on mobile."
* *Action*: Converted into bounded git tickets or executed immediately, unless it spends money, sends something to real people, touches credentials, or deletes data: those are prepared and confirmed first, however clearly they were spoken.

### Bucket 4: Decisions & Rulings
* Definite choices that close an open debate.
* *Example*: "I decided we are parking the simulation idea for now."
* *Action*: Codified into project memory so the question is never re-opened.

---

## The Response Contract

When processing a voice memo, the AI must reply with a structured three-part response:

1. **What I Heard (The Reality Check)**:
   A 2 to 3 sentence confirmation capturing the essence of the memo to verify comprehension before acting.
2. **Immediate Actions Dispatching Now**:
   The concrete tasks from Bucket 3, with branch names and files targeted.
3. **Decisions Logged & Ideas Captured**:
   The items from Buckets 2 and 4 logged for posterity without cluttering today's sprint.
