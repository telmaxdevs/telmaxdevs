# Welcome 👋  

Hi there — and welcome

*IMPORTANT*: I recommend getting github copilot, or cursor to help you understand and finish/fix anything that needs fixing, there are ALOT of redundant stuff. 

This github account was created in order to contain all code I've created. 

I apologize as some repos may not be documented correctly. 

---

## 📂 Repository 1 — * Address Processing & Data Management Toolkit*  
**Purpose:** Comprehensive suite of Python tools for processing Canadian postal addresses, checking Bell Internet service availability, and managing geographic data with Canada Post API integration and competitive fiber analysis.  
**Tech stack:** Python, Selenium, Pandas, Requests, undetected-chromedriver, Canada Post API  
**Where to start:**  
- `python unified_canada_post_processor.py` - Main address processor (requires address_points.csv)
- `python postal_code_lookup.py` - Simple postal code lookup tool
- `pip install -r requirements.txt` then install additional deps: `pip install selenium undetected-chromedriver selenium-stealth fuzzywuzzy openpyxl`

**Tips & Gotchas:**  
- Rate limiting is crucial - scripts default to 0.1-0.2s delays between API calls to avoid getting blocked
- Progress auto-saves every 100 records to prevent data loss during long batch operations
- `stealth.py` uses advanced anti-detection for web scraping - may need Chrome driver updates
- Most scripts expect specific CSV column names (fulladdr, postal_code, town, status)
- Focus is Ontario addresses - Barrie, Richmond Hill, Aurora, Markham specifically
- Canada Post API key is hardcoded to the one on their website, please check the network tab to get one that works for you - replace "EA98-JC42-TF94-JK98" 

---

## 📂 Repository 2 — *TelMax Coords 2*  
**Purpose:** Interactive field survey tool for GPS coordinate tracking and data collection  
**Tech stack:** Next.js 15, React 19, TypeScript, Google Maps API, Supabase, Tailwind CSS  
**Where to start:**  
- Set up environment variables in `.env.local` (Google Maps API key, Supabase credentials)
- Run `npm install && npm run dev`
- Visit `http://localhost:3000` and click on the map to start tracking points

**Tips & Gotchas:**  
- Requires Google Maps API key with billing enabled for production use
- Database tables (maps, coordinates) must be created in Supabase before first use
- Mobile-optimized for field work - best used on touch devices with GPS
- Points are organized by map groups - create a new map for each survey project

---

## 📂 Repository 3 — *Engineering Project Management Suite (Notion Clone)*  
**Purpose:** A comprehensive Notion-like collaboration platform with specialized engineering project management capabilities for fiber network infrastructure. Features document management, real-time editing, and an advanced engineering tracking system for managing municipal projects, fiber hubs, milestones, and vendor relationships.

**Tech stack:** Next.js 15, TypeScript, Supabase (PostgreSQL), Tailwind CSS, Radix UI, BlockNote Editor, React Hooks, Zustand

**Where to start:**  
- Run `npm run dev` to start the development server
- Navigate to `/engineering` for the engineering database system
- Use the main document editor for Notion-like functionality

**Tips & Gotchas:**  
- Configure Supabase environment variables before running (`NEXT_PUBLIC_SUPABASE_URL`, `NEXT_PUBLIC_SUPABASE_ANON_KEY`)
- The engineering system supports 80+ dynamic milestone types and real-time collaboration
- Import CSV data using the Master Schedule import feature at `/api/engineering/import-master-schedule`
- Database migrations are managed via `npm run migrate` - run initial setup with `npm run dev:setup`
- Features dual-mode interface: standard Notion clone + specialized engineering tracking with municipal engagement, fiber hub management, and vendor tracking

---

## 🛠 General Advice  
- Keep dependencies updated, but **test thoroughly** before pushing changes.  
- Document changes in the repos’ own READMEs so future maintainers aren’t lost.  
- If something feels broken, check the commit history — you might find answers there.  

---

