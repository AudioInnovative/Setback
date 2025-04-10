# Product Requirements Document (PRD): Setback – Family Edition (Web Version)

## Overview
A 4-player, team-based card game (2v2) that allows family members to play Setback online from any browser. The game will follow custom family rules including the Widow, 6 and Out, custom draw phase, and scoring.

## 1. Goals
- Digitally recreate Setback with full rule fidelity.
- Allow remote players to connect and play from their own devices.
- Host the game on a custom website with a simple landing page.
- Provide a smooth, accessible user experience with minimal setup.

## 2. Users
- **Primary Users:** Family members familiar with Setback rules.
- **Secondary Users:** Guests invited to play.
- Users may be on desktop, tablet, or mobile.

## 3. Platforms
- Browser-based game built with HTML/CSS/JavaScript.
- Hosted on your custom website (e.g., setback.yourdomain.com).

## 4. Core Features

### Game Structure
- 4 players per game (2 teams of 2)
- 1 dealer per round (rotates left)
- 6 cards per player + 1 Widow hand
- Full 53-card deck (52 cards + 1 Joker)

### Game Phases
1. **Deal Phase** – Deal 6 cards to 4 players + 6 to Widow (last card face-up)
2. **Bidding Phase** – Clockwise, one bid per player (1–6 or 6 and Out)
3. **Trump Selection** – Bid winner merges with Widow and declares trump (must hold at least 1 trump card)
4. **Discard Phase** – Players discard all non-trumps (max 6 cards kept)
5. **Draw Phase** – Cards drawn from unshuffled deck (23 cards remaining) using zero-trump redraw logic
6. **Trick Play Phase** – 6 tricks per round, standard play rules
7. **Scoring Phase** – 6 points max per round (High, Low, Jack, Off-Jack, Joker, Game)
8. **Win Check** – First to 21 points or result of 6 and Out

## 5. Rules & Mechanics
- Widow rules
- Zero-Trump redraw rules with discard handling
- “6 and Out” bid with automatic win/loss logic
- Trick resolution including trump vs. non-trump behavior
- Scoring system with point-card tally and Game point value count

## 6. Multiplayer
- Realtime 4-player matches via WebSockets or Firebase
- Room creation with private join codes or usernames
- Turn synchronization and shared game state
- Host/dealer flow management

## 7. UI Components

### Landing Page
- Brief intro
- “Play Now” button
- Option to enter/join room

### Game Screen
- Player hands (cards face-up for local user only)
- Shared trick area (played cards)
- Bid interface
- Trump suit indicator
- Scoring area
- Notifications for turn, trick winner, round score

## 8. Stretch Features
- AI players (for testing or filling empty seats)
- In-game chat or emotes
- Game history or scoreboard
- Mobile UI optimizations
- Deck customization (e.g., card backs)

## 9. Technical Stack
- **Frontend:** HTML + CSS + JavaScript (Vanilla or React)
- **Game Framework (optional):** Phaser.js for card layout & animations
- **Networking:** Firebase (Firestore or Realtime DB) or WebSocket server
- **Hosting:** Your custom website (static site with backend for real-time logic)

## 10. Deliverables
- Landing Page with room creation/join
- Game Interface with full Setback logic
- Card Deck Logic and visualization
- Multiplayer Sync System
- Scoring System
- Final Deployment to live domain

## 11. Timeline (Example 4-Week Plan)
- **Week 1:** UI Layout, Card Rendering, Deck Logic
- **Week 2:** Bidding System, Widow Merge, Trump Declaration
- **Week 3:** Discard + Draw Phase, Trick Play Logic
- **Week 4:** Multiplayer integration, Scoring, Polish & Deploy
