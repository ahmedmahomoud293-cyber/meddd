# رابعة طب — Premium Medical Study Planner

A luxurious, high-performance medical study management platform purpose-built for fourth-year medical students. Designed to streamline curriculum tracking, lecture mastery, dynamic countdowns, dual Gregorian/Hijri calendar scheduling, daily clinical tasks, and real-data topic progression analytics.

---

## 🌟 Key Highlights & Features

- **Exclusive 4th-Year Medical Curriculum Preloaded:**
  - **Pediatrics:** 16 branches (Neonatology, Nutritional Disorders, Respiratory, Hematology, Gastroenterology, Cardiology, Nephrology, Neurology, Endocrine & Adolescent Medicine, Infectious Diseases, Allergy, Rheumatology, Immunology, Oncology, Genetics, Hepatology) spanning 45 high-yield lectures.
  - **Anesthesia:** General Anesthesia & Perioperative Care (11 lectures).
  - **Psychiatry:** Comprehensive Psychiatry Topics (10 lectures).
  - **Tropical Medicine:** Infectious & Tropical Medicine Topics (17 lectures).
  - **Rheumatology:** Autoimmune & Connective Tissue Diseases (6 lectures).
- **Interactive Multi-View Calendar:**
  - Month, Week, and Day interactive views.
  - **Gregorian Primary & Umm al-Qura Hijri Secondary:** Standardized via `Intl.DateTimeFormat` with `islamic-umalqura` calendar.
  - Side panel for day inspection with task counters and one-click task scheduling.
- **Dynamic Subject-to-Task Cascading Linker:**
  - Selecting a Subject filters the Branches dropdown.
  - Selecting a Branch filters the Lectures dropdown.
  - Selecting a Lecture automatically populates the task title and links curriculum progress.
  - Create free-form clinical tasks (e.g. "Solve 50 MCQs", "Revise ECG Criteria") with zero friction.
- **Daily Tasks Agenda ("What do I have to do today?"):**
  - Dedicated agenda answering what needs to be studied today.
  - Automatic Overdue section for incomplete prior tasks.
  - Yesterday / Tomorrow navigation stepper.
- **Dynamic Examination Countdown:**
  - Large live seconds countdown targeted to **19 February 2027** (or user-customized board date).
  - Built-in date & time picker that updates immediately across the platform.
- **Topic Progression & Analytics:**
  - 100% real-data metrics (no simulated values or hardcoded charts).
  - GitHub-style study activity heatmap displaying daily completion intensity.
  - Consecutive active study day streak and longest streak tracker.
  - Subject mastery comparison bars with branch-level drilldown.
  - Smart clinical study insights derived from actual completion velocity.
- **Offline Persistence & Zero-Backend Privacy:**
  - Runs 100% on vanilla HTML5, CSS3, and JavaScript.
  - Data saved to `localStorage` with defensive error handling and stable IDs.
  - Full JSON backup export and restore with validation.
  - Factory reset option with confirmation safeguards.
- **Visual Identity:**
  - Bespoke dark navy (`#101827`) and muted gold (`#C99A2E`) aesthetic.
  - Architectural geometric "4" logo and matching vector favicon.
  - Right-side persistent collapsible sidebar (desktop LTR) and bottom drawer (mobile).
  - Responsive across smartphones, tablets, and ultra-wide desktops.

---

## 📁 Directory Structure

```text
/
├── index.html              # Main single-page application entry point
├── README.md               # Documentation and GitHub Pages deployment guide
├── assets/
│   ├── logo.svg            # Distinctive geometric '4' logo
│   └── favicon.svg         # Matching browser favicon
├── css/
│   └── styles.css          # Core CSS variables, layout, animations & responsiveness
└── js/
    ├── data.js             # Initial 5 subjects, branches, 89 lectures & default settings
    ├── icons.js            # Offline scalable SVG icon library
    ├── date-utils.js       # Gregorian & Umm al-Qura Hijri date engine & streak counter
    ├── storage.js          # LocalStorage manager, backup export/import & activity logger
    ├── subjects.js         # Curriculum manager, branch management & lecture editor
    ├── tasks.js            # Task controller & Daily Tasks agenda view
    ├── calendar.js         # Month/Week/Day interactive calendar
    ├── dashboard.js        # Main dashboard, live exam countdown & summary tiles
    ├── analytics.js        # Topic Progression, SVG charts & activity heatmap
    ├── settings.js         # Examination date editor, density & data management
    └── app.js              # Application orchestrator, modal system & toast notifications
```

---

## 🚀 Running Locally

Because this application uses standard static files, you can run it immediately without compiling or installing Node packages:

### Option 1: Any Local Static HTTP Server (Recommended)
Using Python (preinstalled on most computers):
```bash
# In the project directory
python -m http.server 8000
```
Open [http://localhost:8000](http://localhost:8000) in your web browser.

### Option 2: Node http-server or npx serve
```bash
npx serve .
```

### Option 3: Direct File Opening
Double-click `index.html` to open it in your browser. (All relative paths and localStorage work in modern browsers).

---

## 🌐 Deploying to GitHub Pages

Deploying takes under 2 minutes:

1. Create a new GitHub repository (e.g. `rabia-tab-planner`).
2. Push your project files to the repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of رابعة طب Medical Study Planner"
   git branch -M main
   git remote add origin https://github.com/<your-username>/rabia-tab-planner.git
   git push -u origin main
   ```
3. In your GitHub repository:
   - Navigate to **Settings** > **Pages** (under the "Code and automation" section).
   - Under **Build and deployment** > **Source**, choose **Deploy from a branch**.
   - Select branch: `main`, folder: `/ (root)`.
   - Click **Save**.
4. GitHub Pages will build and deploy your site within 60 seconds at:
   `https://<your-username>.github.io/rabia-tab-planner/`

---

## 🛡️ Data Backup & Privacy Reminder

All data is stored directly in your browser's `localStorage`:
- No clinical information or study schedules leave your device.
- To transfer your data between devices or share your setup with classmates, open **Settings** > **Export Data (JSON)**.
- Use **Import Backup File** on any other device to instantly restore all subjects, progress, and tasks.

---

## ⚖️ License

MIT License. Designed with excellence for 4th-year medical students.

