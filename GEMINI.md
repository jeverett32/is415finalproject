# Gemini Project Plan: IS Recruiting Insights Dashboard

This document outlines the plan for creating the IS Recruiting Insights Dashboard and the accompanying storytelling chart as per the project description.

## 1. Project Setup & Data Preparation

The first step is to set up the environment and prepare the data for analysis.

*   **Tool Selection:** This plan will assume the use of **Tableau** for the dashboard and storytelling chart, but Power BI or other tools can be used.
*   **Data Loading:** Connect to the `IS Core Admission Survey for IS 415 - combined.xlsx` file.
*   **Data Cleaning & Transformation:**
    *   **Column Renaming:** Rename columns for easier use (e.g., shorten long question names).
    *   **Calculated Fields for "Very Influential":** For each class and activity, create a calculated field to count the number of "3" ratings.
        *   Example for IS 201: `IF [IS 201] = 3 THEN 1 ELSE 0 END`
    *   **Calculated Fields for "How did you hear...":** Create calculated fields to parse the multi-select question.
        *   Example for "IS 201": `IF CONTAINS([How did you hear...], "IS 201") THEN 1 ELSE 0 END`
    *   **Data Type Verification:** Ensure all columns have the correct data types (e.g., Year as a dimension, influence scores as measures).

## 2. Dashboard Creation

The dashboard will be built with interactivity and clarity in mind.

*   **Global Filters:** Add filters for `Year` and `Gender` that apply to the entire dashboard.
*   **A. IS Prerequisite Classes:**
    *   Create a bar chart showing the average influence score for `IS 110`, `IS 201`, and `IS 303`.
    *   Use color to highlight the highest and lowest scoring classes.
    *   Use a line chart or side-by-side bars to compare 2024 vs. 2025 data.
*   **B. Recruiting Activities:**
    *   Create a bar chart for the average influence score of each recruiting activity.
    *   Use color to highlight the highest and lowest scores.
    *   Enable year-over-year comparison.
*   **C. "Very Influential" Counts:**
    *   Create a bar chart showing the count of "3" ratings for each class and activity.
    *   Highlight the items with the most and fewest "3"s.
    *   Allow for comparison between years.
*   **D. How Students Heard About IS:**
    *   Create a bar chart displaying the count for each source, using the calculated fields from the preparation step.
*   **Dashboard Assembly & Usability Testing:**
    *   Combine all the created views into a single dashboard.
    *   Arrange the views logically for a clean and intuitive user experience.
    *   Share the dashboard with at least two people for feedback and make adjustments based on their input.

## 3. One-Slide Storytelling Chart

This slide will focus on a single, actionable insight.

*   **Chosen Question:** The analysis will focus on: **"What insights help explain the disproportionate decline in female applicants in 2025, and what steps might the department take to encourage more female students to apply?"**
*   **Data Analysis:**
    *   Filter the data for 2025 and analyze the differences in influence scores and "how you heard" between male and female students.
    *   Compare these findings to the 2024 data to identify trends.
*   **Chart Design:**
    *   Create a single, focused chart (e.g., a slope chart, a diverging bar chart) that clearly communicates the key insight.
    *   Use a strong title to state the main takeaway.
    *   Use color and annotations to guide the audience's attention.
    *   Add a concise recommendation for action based on the insight.
*   **Feedback and Refinement:** Get feedback on the clarity and impact of the slide.

## 4. Final Deliverables

*   **Dashboard:** Publish the completed dashboard to Tableau Public and generate a shareable link.
*   **Storytelling Slide:** Export the final slide as a PDF.
