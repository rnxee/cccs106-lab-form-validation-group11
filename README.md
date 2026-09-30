# CCCS 106 - Week 5 Group Laboratory Task
## CSPC Scholarship Intake Portal Form Validation & Defensive Programming
**Course Instructor:** Allan O. Ibo, Jr., MSc (allanibojr@cspc.edu.ph)


### 1. Group & Team Members Roster
**Group Name / Number:** [Batag]

**Year & Section:** [BSCS 3A]

**Date of Submission:** [2026-09-30]

**Submitting Member:** [Renz Angelo Priela]


|  Role / Order  |  Full Name  |  Student ID Number  |  Institutional Email  |  Key Technical Contribution |
|  --------  | :---: |  :---:  |  :---:  |  ---  |
|  **Member 1**  |  Renz Angelo S. Priela  |  [2411282]  |  [renpriela@my.cspc.edu.ph]  |  [e.g., Regex & Domain Validator Engine]  |
|  **Member 2**  |  Gelorenz D. Sta Ana  |  [2411288]  |  [gestaana@my.cspc.edu.ph]  |  [e.g., Flet UI Reactive Error States & Events]  |
<!--- |  **Member 3**  |  Jay Marion B. Ubante  |  [C20101802]  |  [jayubante@my.cspc.edu.ph]  |  [e.g., Dataclass Contracts & Automated Testing]  | --->

### 2. Functional Requirements Matrix

The application intake form captures five (5) core fields with strict validation rules:

| Field Name | Flet Control | Constraint / Validation Rule | Error Message Feedback |
| --- | --- | --- | --- |
| **Applicant Name** | `ft.TextField` | Mandatory, 2 to 60 characters, alphabetic characters, hyphens, periods, and spaces only. | `"Enter a valid name (2–60 letters, hyphens, or periods)."` |
| **Student ID** | `ft.TextField` | Mandatory, strictly follows CSPC student ID pattern: `^20\d{2}-\d{4,5}$` (e.g., `2024-0123`). | `"Invalid Student ID. Expected format: YYYY-NNNN (e.g., 2024-0123)."` |
| **CSPC Email** | `ft.TextField` | Mandatory, must end with the official institutional domain `@cspc.edu.ph`. | `"Institutional email required (must end with @cspc.edu.ph)."` |
| **Mobile Number** | `ft.TextField` | Mandatory, valid 11-digit Philippine mobile format: `^(?:\+63|0)9\d{9}$`. | `"Invalid mobile number. Expected: 09XXXXXXXXX or +639XXXXXXXXX."` |
| **Academic GWA** | `ft.TextField` | Mandatory numeric float between `1.00` (highest grade) and `5.00` (failing grade). | `"GWA must be a valid number between 1.00 and 5.00."` |
| **Program** | `ft.Dropdown` | Mandatory selection from predefined CSPC scholarship programs. | `"Please select an accredited scholarship program."` |
