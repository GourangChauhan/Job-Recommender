# 📂 **Job Recommendation System — ML II Project**

---

## 📋 **Overview**

This project is a **Job Recommendation System** designed to bridge the gap between job seekers and recruiters using data-driven machine learning models. It tackles key challenges like automatic job domain tagging, salary prediction, and ultimately matches resumes-to-jobs and jobs-to-resumes, providing intelligent recommendations to improve the job application process.

Developed by **Group 3**:
Akanksha Mathpati, Chris Tomaszkiewicz, Deepali Dagar, Sakshi Bokil for the Machine Learning II course.

---

## **Project Objectives**

1. **Domain Classifier**  
Predict the job domain(s) using multi-label classification on job descriptions and skills.

2. **Salary Prediction**  
Estimate normalized or annual salary using job details like title, description, company, and experience level.

3. **Job & Candidate Recommender**  
- Recommend top job postings for uploaded resumes.  
- Recommend top candidate profiles for uploaded job descriptions.  
- Provide fallback recommendations when no uploads are provided.

---

## **Data Sources**

- **LinkedIn Postings Dataset** (124,000+ jobs from 2023–2024)  
  Features: `job_id`, `company_id`, `title`, `description`, `salary`, `location`, `skills`, `views`, `applies`

- **Resume Dataset** (2400+ resumes in string/PDF format)  
  Features: `id`, `resume_str`, `resume_html`, `category`

---

## **Feature Engineering**

- **Text preprocessing** (lemmatization, stopword removal)  
- **Skill extraction & domain inference**  
- **Unified dataset creation** for model training

---

## **Methodology**

- **Domain Classifier:**  
  XGBoost (best performing)  
  - F1 Micro Score: **0.718**  
  - Hamming Loss: **0.098**

- **Salary Prediction:**  
  Regression modeling (details in notebooks/code)

- **Recommender System:**  
  Embedding-based similarity matching between resumes and job descriptions

---

## **Interface Prototype**

The system includes a prototype interface where:  
- Users can upload resumes to get matched jobs.  
- Recruiters can upload job descriptions to get top candidate recommendations.  
- Default recommendations are available when no uploads are provided.

---

## **Results**

- Achieved robust domain classification using **XGBoost**  
- Provided meaningful **salary predictions** for candidates and recruiters  
- Delivered an effective **top-N job and candidate recommendation system**

---

## **Future Scope**

- **Personalized recommendations** using user feedback (e.g., clicks, applications)  
- **Recommend upskilling opportunities** by identifying resume skill gaps  
- **Deploy as an API or plug-in** for platforms like LinkedIn, Indeed, or ATS tools

---
