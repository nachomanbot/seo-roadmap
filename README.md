# SEO Roadmap Builder (Prototype)

Streamlit prototype that generates a **DOCX action-plan skeleton** from:
- a **pre-loaded Play Pack XLSX** in the repo (per client profile, with Priority Order + Month Allocation)
- optional keyword/topic CSV upload (enrichment)

## What this prototype does
- Select a client profile (one tab in the Play Pack XLSX)
- Optionally apply a few “audit override” toggles (prototype)
- Optionally upload a keyword/topic CSV
- Generate and download a DOCX “skeleton” action plan

---

## Repo contents
- `app.py` — Streamlit app
- `requirements.txt` — dependencies
- `runtime.txt` — python version (useful for Streamlit Cloud)
- `.streamlit/config.toml` — Streamlit config
- `SEO_PreMade_Plays_By_Client_Profile_v2.xlsx` — **pre-loaded** play pack used by default (no upload needed)

---

## Local run
```bash
python -m venv .venv
# mac/linux
source .venv/bin/activate
# windows
# .venv\Scripts\activate

pip install -r requirements.txt
streamlit run app.py
```

Open: http://localhost:8501

---

## Deploy (Streamlit Community Cloud)
1. Push this repo to GitHub
2. Go to Streamlit Community Cloud → “New app”
3. Select the repo + branch
4. Set **Main file path**: `app.py`
5. Deploy

---

## Prototype notes
- This version generates the “skeleton” sections and timeline table.
- Next iteration: map Plays → Tasks using the Optimization Library, and generate per-month sections with task lists.

