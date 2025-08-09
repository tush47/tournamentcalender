# Sports Tournament Calendar 2025

## 📌 Overview
This project is a GenAI Intern Assignment solution: a simple, browser-based web app that displays an up-to-date calendar of real-world sports tournaments for 2025, covering 12 sports and all major levels (International, National, State, District, Corporate, University, Club, etc.).

- **UI:** Plain HTML + JavaScript (no frameworks)
- **Data:** JSON file (`tournaments.json`) acts as the in-memory database
- **Features:** Filter by Sport and Level, view tournament details, and visit official links

---

## 🏗️ System Design & Approach

### Data Collection
- Tournament data was manually curated from official sports federation websites, event organizers, and trusted sports news sources.
- Each entry was checked for accuracy and relevance (2025, real-world, upcoming events).
- Local and district-level tournaments were included for bonus points.
- Data is stored in a single JSON file for simplicity and portability.

### Architecture
- **Frontend:**
  - `index.html` loads and displays tournaments from `tournaments.json`.
  - Filtering is done in-memory using JavaScript.
  - No backend or database server required.
- **Data Storage:**
  - `tournaments.json` contains all tournament records in a flat array.
  - Each record now includes a `SportKey` field (a normalized, lowercase, no-space version of the sport name) to ensure robust and future-proof filtering logic in the UI.
  - Acts as a sample DB for the assignment.

### Output Format (JSON fields)
- Tournament Name
- Sport
- SportKey (for filtering)
- Level
- Start Date
- End Date
- Tournament Official URL
- Streaming Partners/Links
- Tournament Image
- Summary (max 50 words)

---

## 📂 Files
- `index.html` — Main UI (HTML + JS)
- `tournaments.json` — Full dataset (JSON)
- `README.md` — Documentation & reviewer guide

---

## 🚀 How to Run (Reviewer Instructions)
1. Download or clone this folder
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari)
3. Use the dropdowns to filter tournaments by Sport and Level
4. Click "Visit" to open the official tournament page

---

## 🗄️ Sample DB Schema (JSON)
```json
{
  "Tournament Name": "ICC Champions Trophy 2025",
  "Sport": "Cricket",
  "SportKey": "cricket",
  "Level": "International",
  "Start Date": "2025-02-19",
  "End Date": "2025-03-09",
  "URL": "https://www.icc-cricket.com/champions-trophy",
  "Streaming": "Disney+ Hotstar",
  "Image": "https://resources.pulse.icc-cricket.com/photo-resources/2025-champions-trophy.jpg",
  "Summary": "ODI tournament featuring top 8 cricket nations, held in Pakistan."
}
```

---

## 📊 Completeness, Clarity, and Relevance
- **Completeness:** All 12 sports and all required levels are covered, with real tournaments for 2025.
- **Clarity:** Data is structured, fields are self-explanatory, and the UI is intuitive.
- **Relevance:** Only real, upcoming tournaments are included; local and district events are present for bonus.

---

## 🔮 Future Improvements & GenAI Automation (Bonus)
- **Automated Data Collection:**
  - Use GenAI (e.g., GPT-4, Gemini) to scrape and summarize tournament data from official sites and news feeds.
  - Integrate sports APIs (e.g., SportRadar, RapidAPI) for live, auto-updating data.
  - Schedule regular updates via a backend script or cloud function.
- **API:**
  - Add a simple backend (Flask/Express) to serve `/tournaments` as a REST API.
- **UI:**
  - Add search by date, streaming info, and richer filters.
- **Scalability:**
  - Move data to SQLite/MySQL for larger datasets and multi-user access.

---

## ⚠ Limitations
- Data is static; updates require editing `tournaments.json`.
- No backend/API (can be added as a bonus).
- Images and URLs may change or expire over time.
- No authentication or user submissions.

---

## ✅ Bonus Points Covered
- Local tournaments included
- UI mockup with filtering
- API-ready JSON format
- Reviewer instructions provided

---

## 📞 Contact
For any questions, please contact [Your Name] or leave a comment in your submission.
