# Candidate Assessment System - Usage Guide

## Overview
This system provides a comprehensive, automated approach to assessing software engineering candidates for Junior and Mid-Level positions at Devkind. It uses AI-driven evaluation based on standardized scoring criteria and produces consistent, fair assessments.

## System Components

### 📁 Folder Structure
```
candidate-assessments/
├── agentic-assessment-prompt.md    # Main assessment AI prompt
├── processed-resumes/              # Converted markdown resumes
├── evaluations/                   # Individual candidate assessments
├── rankings/                      # Position-based candidate rankings
├── templates/                     # Assessment templates
│   ├── junior-engineer-template.md
│   └── mid-level-engineer-template.md
└── workflow-guide.md              # This file
```

## Getting Started

### Prerequisites
1. Access to Microsoft Markitdown tool for document conversion
2. AI assistant capable of following complex prompts
3. Candidate resumes in various formats (PDF, DOC, etc.)

### Step-by-Step Workflow

#### Phase 1: Document Processing
1. **Convert Resumes to Markdown**
   ```bash
   # Use markitdown to convert resume files
   # Example for a single file:
   markitdown convert "Application Tracker/candidate-name.pdf" 
   # Save to: processed-resumes/candidate-name.md
   ```

2. **Organize Processed Files**
   - Save all converted files to `processed-resumes/` folder
   - Use consistent naming: `firstname-lastname.md`
   - Ensure files are clean and readable

#### Phase 2: Individual Assessment
1. **Load Assessment Prompt**
   - Copy the content from `agentic-assessment-prompt.md`
   - Paste into your AI assistant

2. **Process Each Candidate**
   - Provide the candidate's processed markdown resume
   - Specify the target position (Junior/Mid-Level)
   - Run the assessment using the agentic prompt

3. **Save Assessment Results**
   - Save each assessment to `evaluations/`
   - Use naming format: `[position]-[firstname-lastname]-assessment.md`

#### Phase 3: Ranking and Comparison
1. **Generate Position-Specific Rankings**
   - Collect all assessments for each position
   - Create comparative ranking reports
   - Save to `rankings/` folder

2. **Create Summary Reports**
   - Top candidates overview
   - Statistical analysis of candidate pool
   - Hiring recommendations

## Assessment Positions

### Junior Software Engineer
**Target Profile:**
- 0-2 years experience OR strong educational background
- Proficiency in modern web technologies
- Growth mindset and learning potential
- Basic understanding of software development lifecycle

**Scoring Focus:**
- Education and foundational knowledge (40%)
- Technical skills and framework knowledge (45%)
- Growth potential and attitude (15%)

### Mid-Level Software Engineer
**Target Profile:**
- 2-5 years relevant experience
- Strong technical depth and breadth
- DevOps and cloud experience
- Leadership and mentoring capabilities

**Scoring Focus:**
- Experience and proven track record (55%)
- Advanced technical and specialized skills (35%)
- Leadership and problem-solving abilities (10%)

## Quality Assurance

### Review Checklist
- [ ] All scores have supporting evidence from candidate profile
- [ ] Scoring calculations are accurate
- [ ] Recommendations align with total scores
- [ ] Assessment is free from bias and assumptions
- [ ] Cultural fit considerations are noted
- [ ] Interview recommendations are specific and actionable

### Common Issues to Avoid
1. **Over-scoring based on potential rather than evidence**
2. **Under-valuing non-traditional backgrounds**
3. **Inconsistent application of scoring criteria**
4. **Missing key technical requirements**
5. **Insufficient justification for recommendations**

## Integration with Existing Systems

### Application Tracker Integration
- Process candidates from existing Application Tracker folder
- Maintain consistency with current tracking methods
- Link assessments back to original profiles

### Hiring Pipeline Integration
- Use assessments for initial screening decisions
- Provide interview teams with detailed candidate insights
- Track assessment accuracy over time

## Batch Processing Instructions

### Processing Multiple Candidates
1. **Prepare Batch List**
   ```markdown
   # Candidates to Process - [Date]
   
   ## Junior Engineer Candidates
   - [ ] Candidate Name 1 (file: name1.md)
   - [ ] Candidate Name 2 (file: name2.md)
   
   ## Mid-Level Engineer Candidates
   - [ ] Candidate Name 3 (file: name3.md)
   - [ ] Candidate Name 4 (file: name4.md)
   ```

2. **Process Systematically**
   - Work through candidates one by one
   - Use templates for consistency
   - Save progress regularly

3. **Generate Comparative Analysis**
   - Create ranking documents
   - Identify top performers
   - Note interesting patterns or insights

## Markitdown Integration

### Converting Resume Files
```bash
# Single file conversion
markitdown convert path/to/resume.pdf > processed-resumes/candidate-name.md

# Batch conversion (if supported)
for file in "Application Tracker"/*.pdf; do
    name=$(basename "$file" .pdf)
    markitdown convert "$file" > "processed-resumes/${name}.md"
done
```

### Post-Processing Clean-up
After markitdown conversion, review files for:
- Proper formatting and readability
- Complete information extraction
- Removal of conversion artifacts
- Consistent structure across files

## Sample Assessment Flow

### Example: Junior Engineer Assessment
1. **Load candidate**: `processed-resumes/john-doe.md`
2. **Apply prompt**: Use junior engineer scoring criteria
3. **Generate assessment**: Follow template structure
4. **Save result**: `evaluations/junior-john-doe-assessment.md`
5. **Update tracking**: Mark candidate as assessed

### Example Output Structure
```markdown
# Assessment: John Doe - Junior Software Engineer
- Total Score: 75/100
- Recommendation: Good Fit - Proceed to Interview
- Key Strengths: Strong React skills, good learning attitude
- Areas for Development: Limited cloud experience, needs database training
```

## Reporting and Analytics

### Individual Reports
- Detailed scoring breakdown
- Evidence-based justifications
- Interview recommendations
- Cultural fit assessment

### Aggregate Reports
- Position-wise candidate rankings
- Score distribution analysis
- Skill gap identification
- Market competitiveness insights

## Best Practices

### For Accurate Assessments
1. **Read the complete profile** before scoring
2. **Look for concrete evidence** of skills and experience
3. **Consider the role requirements** specifically
4. **Be consistent** across all candidates
5. **Document reasoning** for all scores

### For Fair Evaluation
1. **Focus on technical qualifications** and measurable achievements
2. **Consider alternative pathways** to traditional education
3. **Evaluate potential** alongside current skills
4. **Avoid unconscious bias** based on names, schools, etc.
5. **Use standardized criteria** for all candidates

## Troubleshooting

### Common Issues
1. **Incomplete resume information**
   - Solution: Assess based on available data, note missing information

2. **Unclear or conflicting information**
   - Solution: Make conservative assumptions, request clarification if needed

3. **Candidate overqualified/underqualified**
   - Solution: Assess for best-fit position, note alternative role potential

4. **Technical skills difficult to verify**
   - Solution: Focus on verifiable evidence, suggest technical interview focus

### Support and Maintenance
- Review scoring criteria quarterly for market relevance
- Update templates based on feedback and hiring outcomes
- Maintain consistency with company hiring standards
- Track assessment accuracy against actual hire performance

---

## Quick Start Checklist

- [ ] Set up folder structure
- [ ] Install/access markitdown tool
- [ ] Load assessment prompt into AI system
- [ ] Convert first batch of resumes
- [ ] Process 2-3 test assessments
- [ ] Review results for quality and consistency
- [ ] Begin full candidate assessment process

**Need Help?** Refer to the detailed `agentic-assessment-prompt.md` for comprehensive scoring guidelines and assessment criteria.