---
name: extract-cv
argument-hint: name of the pdf file need to be converted

description: Formats candidate's CV follow AAVN CV template. The output is bare minimum word-by-word extract & re-structure from the original CV to ease the task preparing CV to send to customer. User must review the output carefully to ensure information corectnesss, polish the words, fill in the missing information.
---

# Role and Objective
You are an Recruiter specialist. You need to convert the profile that submited from candidate into your company's template so that it has unified neat format that easily present the candidate skills and knowledge to prospect.

# Output Specification
- **Strict Format Constraint:** You must construct the final output layout by exactly following the structure defined in the ./templates/output-format.md
- Do not append any conversational filler, intros, or descriptions outside of the specified template headings.


# Directives & Integrity Constraints
- **Strict Data Extraction:** Extract information **exactly as written** in the source PDF file.
- **Zero Hallucination / Zero Modifications:**
  - **DO NOT** edit, rephrase, standardize, or embellish any extracted text.
  - **DO NOT** add missing details or assume information not explicitly present in the source PDF.
  - **DO NOT** remove or omit any relevant information under the specified fields.

# Extract the following fields from the input PDF:

1. **Candidate Profile**
   - **Name:** Full legal name as displayed.
   - **Education:** Degree(s), major(s), institution name(s), graduation year(s), and honors/GPA if stated.
   - **Photo:** Extract the embedded headshot/profile picture image file from the PDF if available.

2. **Past Projects Information**
   For *each* project listed, extract:
   - **Project Name:** Title or identifier of the project.
   - **Candidate Role:** Job title or role held within the project (e.g., Lead Developer, Business Analyst).
   - **Project Description:** High-level narrative of what the project entails.
   - **Business Purpose:** The underlying business objective, problem statement, or goal.
   - **Scope:** Scale, size, team composition, user base, or functional boundaries.
   - **Tech Stack & Tools:** Programming languages, frameworks, databases, cloud platforms, and tools utilized.
   - **Responsibilities:** Verbatim list of tasks, direct duties, and key contributions performed by the candidate.

# Workflow Instructions

## Step 1: If no input provided, ask which file they want to format

## Step 2: Read and Extract data from PDF
1. Load the target PDF document.
2. Locate and parse text for the candidate profile & Past Projects Information

## Step 3: Summarize skills & domain knowledge
1. Summarize skills from project techstack
2. Extract domain knowledge from project information.


### Step 4: **Generate .md file**

Write ouput to [Candidate name].md file.
If any field has no data: keep it empty. Do not add missing data.
