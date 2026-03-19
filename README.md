# Course Ranking System — Product Design Case Study

**Nastka Dąbrowska · Product Manager · March 2026**  
[LinkedIn](https://www.linkedin.com/in/anastazjadabrowska/) · [Interactive Prototype →](https://anastazjadabrowska.github.io/course-ranking-system-design/course-ranking-prototype.html)

---

## Overview

A self-contained product design case study: how should course ranking work on a multi-category learning platform?

The brief was open-ended — define the principles, identify the contributing factors, design the sorting and filtering UX. I treated it as a full product exercise: competitor research, algorithm design, key decision documentation, and an interactive prototype.

**Completed independently in ~2 days.**

---

## Deliverables

| | |
|---|---|
| 📄 [Product Design Document](https://anastazjadabrowska.github.io/course-ranking-system-design/course-ranking-document.html) | Algorithm design, competitive audit, three key decisions explained |
| 🖥️ [Interactive Prototype](https://anastazjadabrowska.github.io/course-ranking-system-design/course-ranking-prototype.html) | Lo-fi desktop UI — working filters, sort modes, quality labels |
| 🎥 [Loom Walkthrough](https://www.loom.com/share/8b05401c1f384407957f323b0916bc0b) | ~2 min video walkthrough |

---

## The Problem

Most learning platforms treat ranking as a black box.

- **Coursera** had no user-controlled sort in search results — the button was missing entirely
- **Skillshare** hid ratings on listing cards — no way to evaluate a course without clicking in
- Both platforms made filter state invisible — filters activated silently with no confirmation

Users paid the price: wasted time on low-quality content, good courses staying buried.

---

## The Algorithm

A composite Ranking Score combining five signals:

| Signal | Weight | Why |
|---|---|---|
| User Rating | 40% | Weighted by review volume — prevents gaming by small review sets |
| Completion Rate | 25% | Hardest signal to fake — users vote with their time |
| Popularity | 20% | Scaled enrollment — older courses don't permanently dominate |
| Content Freshness | 10% | Critical in fast-moving fields like AI and cloud |
| Community Activity | 5% | Q&A responsiveness, instructor engagement |

Each course receives a **quality label** — ★ Top Rated, ✦ Highly Rated, or · Well Rated — rather than a raw numeric score. The label is more actionable at a glance and avoids false precision (73.4 vs 71.2 is meaningless to a learner).

---

## Three Key Decisions

**1. Label over number**  
An earlier version showed a raw score on every card. Scrapped it — a label communicates what the user actually needs to act on without requiring interpretation.

**2. Completion rate visible and sortable**  
Neither Coursera nor Skillshare surfaces this. Making it visible changes the incentive structure: instructors are rewarded for building courses people finish, not just enroll in.

**3. Instructor dashboard: hints, not weights**  
The roadmap includes a dashboard for course creators — but deliberately without exposing the exact weight of each factor. If instructors know rating = 40%, they optimise for rating, not for learners. And every rebalancing of weights feels like a rule change.

The better version: actionable hints. *"63% of learners drop off before lesson 4 — review pacing in that section."* Actionable, not algorithmic.

---

