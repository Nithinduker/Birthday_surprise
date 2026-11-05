PRD — For My Pappuma 🤍 (Mathu's Birthday Experience)
Original Problem Statement
Personalize the existing birthday website for my girlfriend Mathu. My nickname for her is Pappuma🤍. We have been together for 2 and a half years. My name is Nithin. Birthday: November 17, 2026. Use elegant ivory white, champagne and rose gold colors. Make the experience romantic, premium, warm and emotional. Use the following exact sections: Welcome to Mathu's surprise, live birthday countdown, Our 2½ Years Journey, Our Memories, 10 Reasons I Love You, A Letter to My Pappuma, Open Your Little Gift, and the locked birthday reveal. Use the personalized copy I provide separately. Do not use generic placeholder names in visible text. Preserve existing working functionality.

Personas
Primary viewer: Mathu ("Pappuma") — opens the site on/around Nov 17, 2026; experiences the surprise on mobile.
Author: Nithin — owns the copy, the secret passcode, and the voucher promises.
Core Requirements (static)
Exact 8 sections, in order, with personalized names only (Mathu / Pappuma / Nithin).
Palette: ivory #FAF6F0, champagne #E8D3B9/#F4E6D4, rose gold #C87D87/#F2D6DC/#8C4A52, burgundy text #361622.
Romantic, premium, warm, emotional art direction.
Preserve existing working functionality (backend /api/ hello + status checks untouched and verified).
Architecture / Tasks Done (2026-11-03)
Rewrote frontend single-page experience (React + Tailwind + framer-motion + lenis + canvas-confetti).
Custom fonts: Cormorant Garamond (display), Great Vibes (script), Dancing Script (letter), Jost (body).
Custom favicon SVG (rose-gold heart monogram N♥M), branded index.html title/meta.
Signature on-load moment: burgundy intro curtain ("For my Pappuma — from Nithin, with love") sliding away into a masked line-by-line hero reveal.
Sections: Hero (parallax arch image, floating badges) → editorial marquee → live countdown (ticking digit animations to Nov 17 2026, celebratory state on the day) → Journey (dark burgundy alternating timeline, 5 chapters) → Memories (polaroid masonry + lightbox) → 10 Reasons (3D flip cards) → Letter (envelope opens to handwritten letter) → Gift (animated box opens to 4 love-voucher coupons) → Locked reveal (ticking lock card, secret passcode PAPPUMA2026/PAPPUMA/MATHU/LOVE, confetti + grand message, persisted in localStorage).
Lenis momentum scrolling; ErrorBoundary; grain overlay; data-testids on all interactive elements.
Backend untouched (FastAPI/Mongo template endpoints preserved, curl verified).
Verification
curl GET /api/ → {"message":"Hello World"} ✓; frontend 200 ✓
Desktop 1440 screenshot: hero correct, no overflow ✓
Mobile 390 screenshot + scripted flows: letter opens ✓, gift vouchers appear ✓, wrong passcode errors ✓, PAPPUMA2026 unlocks reveal + confetti ✓, memory lightbox ✓, no horizontal overflow ✓
Copy provenance / placeholders
Nithin provided no copy file; copy was drafted from his stated details (user approved best-judgment). Photos are romantic stock imagery — swap with real photos in /app/frontend/src/data/site.js (MEMORIES, IMAGES).
Updates (2026-11-04)
Real photos added (user uploaded 5 photos): hero arch now uses the couple's forehead-to-forehead photo (/photos/hero.webp), Our Memories gallery shows real polaroids with mood captions, and the Journey section uses the car photo as its faint backdrop. Remaining stock imagery (gift boxes, rose) is decorative only.
"Our Melody" music toggle (user uploaded Vazhithunaiye Song Bgm.mp3): hero now has a "Play Our Melody / Pause Our Melody" glass-pill toggle with a spinning rose-gold vinyl disc; audio loops at 55% volume, served from /audio/vazhithunaiye.mp3 (curl verified 200, audio/mpeg; play/pause state transitions verified).
Gallery expanded to 8 real frames: roadside hug ("the safest place on earth"), silly faces ("the sillies — a club of two"), pink floral café ("pretty in pink, just like her"), café coffee selfie ("coffee first, poses later"). All 8 verified loading (naturalWidth > 0), no horizontal overflow.
Backlog
P1: Real story milestones for the Journey timeline (dates/places).
P2: Hidden photo-scavenger-hunt easter egg via the passcode.