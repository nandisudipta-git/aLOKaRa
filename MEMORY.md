# dotBro - Memory Handoff

This document summarizes the current state, deployment configuration, and recent activity for the `dotbro` project to ensure a smooth transition for subsequent sessions.

## 📌 Project Overview
- **Name:** dotBro
- **Tagline:** Some conversations deserve another chance.
- **Description:** A premium, highly interactive single-page landing website that gives missed conversations, questions, and collaborations another chance.
- **Tech Stack:** Vanilla HTML/CSS/JS (embedded scripts and styles), Vercel, Git.
- **Key Features:**
  - Premium Apple/Linear-style glassmorphic design system.
  - Interactive Custom Cursor & Cursor Ring.
  - Animated Particle 3D Background Canvas.
  - Interactive nodes/scenarios, scroll-linked animations, and slide system.
  - Smooth Keyboard and Slide dot navigation.

---

## 🛠️ Current State & Configuration

### 1. Git Repository
- **Remote URL:** `https://github.com/ronnandy56211-byte/dotbro.git`
- **Branch:** `main`
- **Status:** Clean. The working tree has no uncommitted changes for `index.html`.
- **Last Sync:** Successfully merged local edits with the remote.

### 2. Vercel Deployment
- **Project Name (on Vercel):** `dotbro`
- **Production URL:** [https://dobro.in](https://dobro.in) (Active & successfully aliased)
- **Fallback URL:** [https://dotbro.in](https://dotbro.in)
- **Deployment Flow:** Automatically triggers on git push to `main` via Vercel-GitHub integration, or manual push using `vercel --prod`.

---

## 🚀 Key Commands
- **Deploy manually to production:**
  ```bash
  vercel --prod
  ```
- **Force clean sync with Git (rebase and push):**
  ```bash
  git stash && git pull --rebase && git stash pop && git push
  ```

---

## 📋 Completed Tasks (Recent)
- [x] Initialized and connected repository to GitHub.
- [x] Refactored landing page design (Apple/Linear UI v2, graph nodes, camera momentum physics).
- [x] Resolved DNS/domain configuration issues to successfully link and alias `dobro.in`.
- [x] Verified builds and deployed clean state to production.
