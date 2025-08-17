# ASA DataFest at SMU 2024 -- Digital Textbook Cheating Detection & Engagement Analysis  

## Project Overview
This project was developed for **ASA DataFest 2024 at Southern Methodist University (SMU)**, where our team **GraphOutLoud** represented **The University of Texas at Austin**.  

We analyzed anonymized CourseKata digital textbook log data (~246,000 records from ~250 students across 3 textbooks) to:  
1. Identify textbook question types that drive interest, engagement, and performance.  
2. Target underperforming chapters for revision.  
3. Detect potential academic dishonesty using machine learning.  

---

## Problem Statement  
Digital textbooks generate rich student interaction logs, offering many opportunities to study learning behavior. Our task was to provide actionable recommendations to CourseKata to boost engagement/performance, reduce academic dishonesty, and improve user experience.

---

## Methods  
- **Data:** 6 CSV log datasets with ~246k events (responses, page views, media views, item metadata, and checkpoints (2 files)).  
- **Feature Engineering:** Created 20+ predictors (accuracy, attempts, time per question, idle ratio, % night/weekend, burstiness, and more).  
- **Modeling:** Trained a **Random Forest model** to generate a suspicion score for each student. Top 10% of extreme behavior/performance patterns were labeled “suspicious” to guide the training.
- **Statistical Testing:** Used Welch Two-Sample t-tests to confirm differences in performance across question types (p < 0.001) to better advise design of chapters and questions.

---

## Key Findings  
- **Question Types:**  
  - Multiple choice (MCQ) and plaintext had consistently high interest and performance.
  - On the other hand, choicematrix, image-cloze, short-text, sortlist had lower scores and engagement.  
  - Recommendations: Increase MCQ/plaintext, reduce or rework low-performing types.  

- **Chapter Insights:**
  - High school textbook Ch. 4 showed the lowest performance across all books and chapters.  
  - Drop-off of ~40% in engagement moving into the following chapter.  
  - Recommendations: Shorten chapter length, simplify question types.  

- **Academic Dishonesty:**  
  - Random Forest flagged **5.6% of students** as suspicious (very high accuracy and very low effort).  
  - Distribution of scores clustered near 0 (normal, non-cheating behavior), with a small suspicious tail >0.8.  
  - Recommendation: CourseKata instructors can use the flagged list as a **review/triage queue** to target outreach/support.  

---

## Repository Contents  
- `code/DataFest.Rmd` → Main R Markdown analysis file
- `presentation/DataFest_Presentation.pptx` → Slides used during competition presentation
- `data/README.md` → See note below on restricted CourseKata data 

**Important Note on Data**  
The raw CourseKata datasets cannot be shared publicly. Only our analysis code and presentation slides are provided here.  

---

## Team GraphOutLoud (UT Austin)  
- Quinn Hungerford  
- Kate Liu  
- Anya Ranavat  
- Emma Zhou  

---

*Finalist entry at ASA DataFest SMU 2024, recognized for actionable insights into digital textbook engagement and academic integrity.* 
