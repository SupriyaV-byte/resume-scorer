# Resume Scorer

A simple ATS-style resume screening tool built in Python. It reads resumes 
(PDF/DOCX/TXT), compares them against a job description, and ranks 
candidates by relevance.

## How it works
- **TF-IDF + Cosine Similarity** — measures how closely a resume matches 
  the job description overall (max 70 points)
- **Skill Keyword Match** — checks for required skills (e.g. Python, 
  Django, AWS, Docker) mentioned in the resume (max 30 points)
- **Total Score** = Similarity Score + Skill Score (out of 100)

## Files
- `resume_scorer.ipynb` — Colab notebook with the scoring code
- `resume_scoring_results.csv` — ranked output of 30 sample resumes

## Usage
1. Update `JOB_DESCRIPTION` and `MUST_HAVE_SKILLS` in the notebook
2. Upload resume files (PDF/DOCX/TXT)
3. Run all cells — get a ranked CSV of top candidates
