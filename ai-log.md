# AI Use Log

This file documents the AI-assisted planning and implementation used for the SWE 380 Assignment 1 portfolio project.

## Planning Prompt

You are assisting with a small public static portfolio website for my SWE 380 assignment.

Project purpose:
The purpose of this project is to personalize an existing HTML/CSS/JavaScript portfolio template using my professional background, education, technical skills, and projects. The finished website will be used as a professional portfolio for employers, recruiters, internship reviewers, professors, and other professionals.

Existing system:
The project is based on the vCard Personal Portfolio template and uses HTML, CSS, and JavaScript.

Allowed changes:
- Update portfolio text and personal information
- Update professional experience and education
- Add or update skills
- Add or update portfolio/project content
- Update navigation content if necessary
- Make small styling, responsive-layout, or accessibility improvements where needed
- Modify front-end HTML, CSS, and JavaScript only when necessary

Do not add:
- A backend
- A database
- A login system
- Analytics or tracking
- External data collection
- Unnecessary frameworks or dependencies

Acceptance criteria:
1. The landing page displays my name and professional role.
2. The portfolio includes an About section describing my professional and educational background.
3. The portfolio displays at least three projects with a title and short description for each.
4. All navigation links move to the correct sections of the portfolio.
5. The website remains readable and usable on a narrow mobile-sized browser window.

Content source:
Use only information provided in content-notes.md. Do not invent education, employment history, awards, projects, skills, certifications, links, or personal information.

Technical constraints:
- Preserve the existing overall layout and structure of the portfolio.
- Keep the website static.
- Preserve the original license and required attribution.
- Keep the site usable on mobile screens.
- Maintain readable text contrast.
- Preserve or improve keyboard navigation.
- Use meaningful link text.
- Use useful alternative text for meaningful images.
- Do not expose private or sensitive information.
- Avoid unnecessary rewrites of working code.
- Prefer small, understandable changes that can be committed incrementally.

Before making any implementation changes, provide:

1. A file-by-file implementation plan explaining which files should be changed and why.
2. Any assumptions you are making.
3. Any technical or content risks you identify.
4. A proposed testing checklist based on the acceptance criteria and accessibility requirements.
5. Any questions that should be answered before implementation.

Do not modify or generate replacement files yet. I want to review the plan before implementation.

## AI Response

## AI Response

### File-by-file implementation plan

1. `index.html`
   - Replace template placeholder identity information with the name, professional role, background, education, skills, experience, and projects from `content-notes.md`.
   - Review navigation labels and section links to ensure they point to the correct portfolio sections.
   - Update project entries so at least three projects have a title and description.
   - Review image alternative text and link text for accessibility.

2. `assets/css/style.css`
   - Review the existing responsive layout before making changes.
   - Make only small styling changes if content becomes difficult to read or use at narrow viewport sizes.
   - Preserve the existing overall visual design.
   - Verify text contrast and spacing remain readable.

3. `assets/js/script.js`
   - Review existing navigation and interactive behavior.
   - Avoid changing JavaScript unless a navigation or interaction issue is identified during testing.
   - If a change is needed, keep it small and directly related to an acceptance criterion.

4. Existing image/assets folders
   - Review images currently used by the template.
   - Remove or replace any template images that incorrectly represent the portfolio owner.
   - Ensure meaningful images use appropriate alternative text.
   - Avoid adding unnecessary assets.

5. `content-notes.md`
   - Use this file as the source of truth for professional and project information.
   - Do not add information that is not present in this file.

6. `ai-log.md`
   - Record the planning prompt, AI response, implementation decisions, and major AI-assisted changes made during the assignment.

### Assumptions

- The starter repository already has a functional static HTML/CSS/JavaScript structure.
- The existing responsive behavior works reasonably well and will only require small corrections if issues are found.
- The information in `content-notes.md` is approved for public use.
- Existing template sections can be reused instead of creating an entirely new site structure.

### Risks

- Template placeholder information could be missed and remain visible on the published site.
- AI could accidentally invent professional details or add information not included in `content-notes.md`.
- Changing too much CSS could break the existing responsive design.
- Navigation links could become incorrect if section IDs are changed.
- Existing template images may not appropriately represent the portfolio owner.
- Accessibility issues such as unclear link text, missing alternative text, or weak keyboard navigation may already exist in the template.

### Proposed test checklist

- Verify the page loads without visible errors.
- Verify the landing page displays Daniel Belville and the correct professional role.
- Verify the About section contains the intended professional and educational background.
- Verify at least three projects appear with titles and descriptions.
- Verify all navigation links reach the correct sections.
- Verify no template placeholder names, email addresses, text, or unrelated personal information remain.
- Test the page at a narrow mobile viewport.
- Test keyboard navigation using the Tab key.
- Check meaningful images for useful alternative text.
- Check external and project links.
- Check the browser console for unexplained errors.
- Verify no private information, passwords, tokens, or secrets are exposed.
- Compare the final implementation against all five acceptance criteria.

### Questions before implementation

- Should the portfolio display a personal email address or should public contact information be limited?
- Are there specific project links or GitHub repositories that should be included?
- Should the existing template profile image be removed, replaced, or left as a placeholder until a suitable image is available?
- Are there any sections in the starter template that should intentionally remain unused?

## Implementation Notes

To be added.

## AI Plan Review

### Accepted Plan Element
I accepted the plan to use content-notes.md as the source of truth and to make small, file-specific changes instead of rewriting the entire portfolio.

### Revised Plan Element
I revised the plan so that JavaScript will only be changed if testing shows that navigation or another interaction is not working correctly. I do not want unnecessary JavaScript changes.

### Risk the AI Identified
The AI identified the risk that placeholder content from the original template could remain in the final published site.

### Risk the AI Missed
The AI did not explicitly identify the risk of accidentally publishing contact information or other personal details that I may not want publicly visible.

## Human Code Review

| File or Region | What the AI Changed | What I Verified | Change Made After Review |
|---|---|---|---|
| `index.html` - Sidebar and About section | Replaced the template name, role, and biography with my own professional information and removed fake contact information. | I verified that my name and professional role are correct, the About text matches `content-notes.md`, and the template email, phone number, birthday, and location were removed. | No additional change was needed. |
| `index.html` - Resume section | Replaced the template education, work experience, and skills with my own education, Bizzdesign experience, and technical skills. | I verified that the education and work information matches `content-notes.md` and that no employment history, education, or certifications were invented. | I noted that the skill percentage bars are visual estimates and may be removed later because they are not factual measurements from my resume. |
| `index.html` - Portfolio and navigation | Replaced template projects with Activity Finder, AI and Enterprise Architecture Research, and Unity Game Development. Removed unused Blog and Contact navigation and template content. | I verified that all three projects came from `content-notes.md`, the visible navigation matches the remaining sections, and unrelated template projects and placeholder content were removed. | Dead `#` project links were removed so the project cards do not appear to link somewhere when no real project URL was provided. |

### Review Summary

During the review, I checked the AI-generated changes for correctness, privacy, accessibility, unnecessary changes, and invented content. I confirmed that the professional information used on the site came from `content-notes.md` and that placeholder information from the original template was removed.

I also reviewed whether the AI changed more code than necessary. Most changes were limited to `index.html`, and the existing CSS and JavaScript were left unchanged because there was not yet evidence that they needed modification.
