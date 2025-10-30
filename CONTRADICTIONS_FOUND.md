# Contradictions Found in UDS Bootcamp Documentation

This document identifies contradictions and inconsistencies discovered in the UDS Bootcamp governance documentation during a systematic review.

---

## 1. Grace Period: One-Time vs. Reusable (CRITICAL)

### Description
The 24-hour grace period for late assignment submissions is described as "one-time" in some documents but this qualifier is missing in others, creating ambiguity about whether students can use this grace period multiple times.

### Documents Affected
- ✓ **RULES.md** (line 24) - **Correctly specifies "one-time"**
- ✓ **FAQ.md** (line 52) - **Correctly specifies "one-time"**
- ✗ **README.md** (line 42) - **Missing "one-time" qualifier**
- ✗ **RECOMMENDATIONS_FOR_MENTORS.md** (line 22) - **Missing "one-time" qualifier**
- ✗ **FAQ.md** (line 76) - **Missing "one-time" qualifier in mentor guidance**

### Current Wording

**RULES.md (Correct):**
> A one-time, 24-hour grace period for a late submission may be granted if requested from the instructor *before* the original deadline.

**README.md (Incomplete):**
> Firm deadlines, a 24-hour grace period (if requested in advance), and the requirement for a good-faith effort on all work.

**RECOMMENDATIONS_FOR_MENTORS.md (Incomplete):**
> Be aware that all assignments have firm deadlines. Remind your mentees that a 24-hour grace period may only be granted if requested *before* the original deadline.

**FAQ.md line 76 (Incomplete):**
> Mentors must remind mentees that all assignments have firm deadlines and that the 24-hour grace period must be requested from the instructor *before* the original deadline.

### Impact
- **Severity: CRITICAL**
- Mentors reading only the RECOMMENDATIONS_FOR_MENTORS.md may incorrectly allow multiple grace periods
- Participants reading only the README.md may expect to use the grace period multiple times
- Inconsistent enforcement across the program could lead to fairness issues

### Recommendation
Add "one-time" qualifier to all mentions of the 24-hour grace period in:
1. README.md (line 42)
2. RECOMMENDATIONS_FOR_MENTORS.md (line 22)
3. FAQ.md (line 76)

---

## 2. Attendance Requirements: Excused Absences vs. 90% Rule (IMPORTANT)

### Description
There is ambiguity about whether excused absences count toward the 90% attendance requirement for program completion. The policy allows for both unexcused absences (max 2) and excused absences (for emergencies), but it's unclear if excused absences affect the 90% completion threshold.

### Documents Affected
- **RULES.md** Section 1.3 (lines 16-19) - Absence policy
- **RULES.md** Section 5.1 (lines 41-43) - Completion criteria

### Current Wording

**Section 1.3 - Absence Policy:**
> Participants are permitted a maximum of **two (2) unexcused absences** throughout the entire bootcamp.
> 
> To have an absence marked as excused, you must notify the program administrator via private message at least **one (1) hour before** the session begins.

**Section 5.1 - Completion Criteria:**
> Attending at least **90%** of all live sessions.

### The Problem
Consider a bootcamp with 20 live sessions:
- 90% attendance = attending 18 sessions = maximum 2 absences total
- Policy explicitly allows 2 unexcused absences
- Policy also allows excused absences for emergencies

**Scenario:**
- Participant has 2 unexcused absences (allowed)
- Participant also has 2 excused absences (illness)
- Total: 4 absences = 80% attendance
- Does this participant meet the 90% completion requirement?

### Impact
- **Severity: IMPORTANT**
- Unclear whether excused absences count against the 90% threshold
- Could lead to disagreements at graduation about certificate eligibility
- May discourage participants from reporting legitimate emergencies

### Recommendation
Clarify one of the following:
1. **Option A:** Excused absences do NOT count toward the 90% requirement (only unexcused absences count)
   - Add to Section 5.1: "Excused absences do not count against the 90% attendance requirement."
2. **Option B:** ALL absences (excused and unexcused) count toward the 90% requirement
   - Modify Section 1.3 to clarify that while excused absences don't result in strikes, they still count toward attendance percentage

---

## 3. Removal Consequences: "May" vs. "Will" (MINOR)

### Description
There is minor inconsistency in the language used to describe removal consequences. Section 1.3 uses "may result in removal" while Section 6.1 uses "will be removed."

### Documents Affected
- **RULES.md** Section 1.3 (line 18)
- **RULES.md** Section 6.1 (line 53)

### Current Wording

**Section 1.3:**
> Exceeding the allowed number of unexcused absences **may result in removal** from the program.

**Section 6.1:**
> Upon accruing **three (3) strikes**, a participant **will be removed** from the program.

### Analysis
Since an unexcused absence results in a strike, exceeding 2 unexcused absences (i.e., having 3) would equal 3 strikes, which "will" result in removal. The language is technically consistent but could be more precise.

### Impact
- **Severity: MINOR**
- Mostly consistent in practice
- "May" in Section 1.3 could imply discretion, but Section 6.1 clarifies it's automatic

### Recommendation
For consistency, consider changing Section 1.3 to:
> Exceeding the allowed number of unexcused absences **will result in removal** from the program under the three-strike policy described in Section 6.1.

---

## 4. Late Submission Wording: "May" vs. Certainty (MINOR)

### Description
The grace period uses "may be granted" language, which could imply discretion, though the policy seems intended to be consistently applied when requested properly.

### Documents Affected
- **RULES.md** Section 2.2 (line 24)
- **FAQ.md** (line 52)

### Current Wording
> A one-time, 24-hour grace period for a late submission **may be granted** if requested from the instructor *before* the original deadline.

### Analysis
The word "may" suggests discretion, but the context implies it should be granted automatically if requested properly (before the deadline). This could lead to inconsistent application.

### Impact
- **Severity: MINOR**
- Could lead to participants being unsure if they'll receive the grace period even when properly requested
- Mentors might interpret this as having discretion to deny properly-requested grace periods

### Recommendation
Consider clarifying:
> A one-time, 24-hour grace period for a late submission **will be granted** if requested from the instructor *before* the original deadline.

Alternatively, if discretion is intended, clarify the criteria for granting/denying.

---

## 5. Capstone Deployment Requirement Clarity (MINOR)

### Description
The CAPSTONE_RECOMMENDATIONS.md specifies that deployment to a live server is "a critical requirement," but this specific requirement is not explicitly mentioned in the RULES.md completion criteria.

### Documents Affected
- **CAPSTONE_RECOMMENDATIONS.md** Section 3.4 (line 57)
- **RULES.md** Section 5.1 (line 43)

### Current Wording

**CAPSTONE_RECOMMENDATIONS.md:**
> Deploy the application to a live server (e.g., Vercel, Netlify for front-end; Heroku, AWS for back-end). A live, functioning project is a critical requirement for portfolio review.

**RULES.md Section 5.1:**
> Achieving a passing evaluation on the final capstone project.

### Impact
- **Severity: MINOR**
- Deployment is clearly stated in the recommendations document
- RULES.md uses "passing evaluation" which could include deployment as a criterion
- Not a true contradiction, but could be more explicit

### Recommendation
Consider clarifying in RULES.md Section 5.1 or adding a note:
> Achieving a passing evaluation on the final capstone project (including successful deployment).

Or add a reference:
> Achieving a passing evaluation on the final capstone project per the criteria in CAPSTONE_RECOMMENDATIONS.md.

---

## 6. Feedback Survey Requirement Impact (MINOR)

### Description
Feedback surveys are stated as "required" in the participation rules, but they are not listed as part of the completion criteria, creating ambiguity about whether completion affects certification.

### Documents Affected
- **RULES.md** Section 3.3 (line 31)
- **RULES.md** Section 5.1 (lines 40-44)

### Current Wording

**Section 3.3 - Participation:**
> Participants are required to complete periodic feedback surveys.

**Section 5.1 - Completion Criteria:**
Lists three criteria:
1. Attending at least 90% of all live sessions
2. Submitting at least 85% of assignments
3. Achieving a passing evaluation on capstone

(Feedback surveys are NOT listed)

### Impact
- **Severity: MINOR**
- Unclear whether survey completion affects certification eligibility
- "Required" suggests it's mandatory, but absence from completion criteria suggests it may not prevent certification
- Could lead to participants skipping surveys if they realize it doesn't affect graduation

### Recommendation
Either:
1. Add feedback surveys to Section 5.1 completion criteria if they are truly required for certification
2. Change Section 3.3 wording to "Participants are expected to complete..." if they're encouraged but not mandatory for certification
3. Add a clarifying note: "Participants are required to complete periodic feedback surveys. While this does not affect certification eligibility, it is critical for program improvement."

---

## Summary Table

| # | Issue | Severity | Documents | Recommended Action |
|---|-------|----------|-----------|-------------------|
| 1 | Grace period "one-time" missing | CRITICAL | README.md, RECOMMENDATIONS_FOR_MENTORS.md, FAQ.md | Add "one-time" qualifier consistently |
| 2 | Excused absences vs. 90% attendance | IMPORTANT | RULES.md | Clarify if excused absences count toward 90% |
| 3 | "May" vs. "will" for removal | MINOR | RULES.md | Use consistent language ("will") |
| 4 | Grace period "may" vs. "will" | MINOR | RULES.md, FAQ.md | Clarify if discretion exists or make automatic |
| 5 | Capstone deployment requirement | MINOR | RULES.md, CAPSTONE_RECOMMENDATIONS.md | Make deployment requirement explicit in completion criteria |
| 6 | Feedback survey requirement impact | MINOR | RULES.md | Clarify if surveys affect certification |

---

## Methodology

This analysis was conducted by:
1. Systematic review of all main governance documents
2. Cross-referencing related policies across documents
3. Identifying inconsistent wording and potential ambiguities
4. Analyzing practical scenarios where contradictions could cause issues
5. Assessing severity based on potential impact on participants and program fairness

---

**Analysis Date:** 2025-10-30  
**Reviewed Documents:**
- README.md
- CODE_OF_CONDUCT.md
- RULES.md
- FAQ.md
- CAPSTONE_RECOMMENDATIONS.md
- RECOMMENDATIONS_FOR_MENTORS.md
- IMPROVEMENT.md
