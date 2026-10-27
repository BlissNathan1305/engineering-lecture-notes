---
name: engineering-lecture-notes
description: Prepare or revise clear, illustrated engineering lecture notes and worked examples in Quarto, with accurate equations, dated references, and printable outputs.
---

# Engineering Lecture Notes

Use this skill for lecture notes, lesson handouts, worked examples, and related teaching material in engineering subjects such as fluid mechanics, thermodynamics, machine design, and engineering mathematics. The lecturer prefers a CLI-first workflow, Quarto sources, Python for behind-the-scenes calculation or illustration, and course files saved in Dropbox. Students are not assumed to be learning coding.

For the institutional examples behind this workflow, read [references/teaching-patterns.md](references/teaching-patterns.md). It summarizes public materials from Berkeley, UT Austin, Iowa State, and Purdue, and distinguishes observed public practices from claims about private instructor preparation.

## Workflow

1. **Set the lesson scope.** Use the supplied course, topic, student level, syllabus, prerequisites, class length, and requested format. Ask only for missing details that materially change the lesson. If the lecturer asks you to choose a topic, choose a suitable one and state the assumption.
2. **Choose a teachable outcome.** Write a short set of student-centered, observable learning outcomes. Keep the lesson focused on the central concept, a small number of supporting ideas, and the level of detail students need for the course.
3. **Build the explanation.** Connect the topic to an engineering situation or guiding question. Explain prerequisites and terms before relying on them. Move from physical meaning to model or principle, then to equations and application. Keep paragraphs and sections short enough to follow in print.
4. **Plan useful visuals.** Add figures where they explain geometry, forces, flow, system boundaries, state changes, trends, or a calculation. Prefer original monochrome SVG diagrams or accurately generated plots. Label axes, directions, boundaries, states, symbols, and units. Give each figure a useful caption and alt text. Make meaning independent of colour; cite and check reuse permission for third-party visuals. Do not add a decorative figure merely to fill space.
5. **Present equations and symbols clearly.** Set equations in mathematical notation. Define every symbol at first use, including units and any sign or subscript convention. Give a brief physical explanation and state assumptions and limits where relevant. Check dimensions and confirm that the equation fits the stated geometry and regime.
6. **Work numerical examples fully.** Use a consistent structure: **Given**, **Find**, **Assumptions/diagram** when needed, **Solution**, and **Answer/check**. Show unit conversions, governing equations, rearrangement when needed, numerical substitution, intermediate results, final units, and a brief interpretation or reasonableness check. Use the symbols (for example, \(\rho\), \(\mu\), \(Q\), and \(D\)) in the solution rather than replacing them with English labels. Do not skip algebra by presenting only a calculator result.
7. **Use Python as a preparation aid.** Choose only libraries useful for the topic. Python may verify arithmetic, generate plots, or retrieve properties; it is not part of the student-facing lesson unless the lecturer asks to teach coding. Keep code hidden in executed Quarto cells or separate scripts when appropriate, while displaying the derivation and result as readable mathematics. For thermophysical properties, use CoolProp only when suitable; state fluid, temperature, pressure, and units, and verify the returned values.
8. **Give students a way to check learning.** Add a small number of conceptual questions, short applications, or a worked practice problem tied to the outcomes. Include concise answers or a separate instructor key when useful. A brief misconception check or pause prompt can be included where it fits the lesson.
9. **Cite sources with dates.** Cite sources near the claims, tables, data, equations, and reused figures they support. Use dated textbooks, standards, original papers, or authoritative data/software documentation. Keep in-text citations consistent and provide complete references with publication year/date, authors or issuing body, title, edition/version when relevant, publisher or journal details, and DOI/URL. The lecturer requires dates in the references: do not leave a reference as “n.d.”; find a dated source or include a clear retrieval date for genuinely undated web material. Never invent a citation or factual detail. Follow the user's academic Research & Evidence Workflow when the task involves a scholarly literature review or claim-level literature synthesis.
10. **Render and review.** Write the editable source as `.qmd`; render requested formats with Quarto CLI. Check that the PDF/Word output contains the full equations, readable figures, working cross-references, worked calculation, and references. Compare computed values against the displayed derivation. Do not claim a render or calculation was verified if the required tool or package was unavailable.
11. **Save and report.** The established default is `~/Dropbox/Courses/<Course>/<Lesson_or_Topic>/`. Keep the `.qmd` source, needed figures, and requested handouts together. After saving, check `dropbox filestatus` when the client is available. If Dropbox is stopped, report that the file is in the local synced folder but cloud upload could not be confirmed.

## Output preferences

- Use Quarto and the command line as the default authoring and rendering path.
- Use a clean, readable, high-contrast design that prints clearly in black and white. Use semantic heading levels, legible figure labels, and uncluttered tables.
- Include a brief definition or explanation before using specialized terms or equations.
- For a worked example, use mathematical symbols consistently, define them, and show the complete calculation with units and interpretation.
- Select Python packages by lesson need: for example, SymPy for symbolic mathematics, NumPy/SciPy for numerical calculations, Matplotlib for plots, Pint for units, and CoolProp for fluid-property values. Do not make students install or learn these tools unless requested.
- Preserve the lecturer's supplied technical notation, syllabus sequence, examples, and references. Do not fabricate laboratory setup, property values, standards, or course requirements.
- Apply the academic-humanizer skill to academic explanatory prose when available, while preserving the course's technical meaning and evidence.
- A useful default lesson structure is: title and course, learning outcomes, motivating question/application, prerequisites/key terms, concept sections, annotated figures, equations and symbol definitions, fully worked example(s), student check/practice, summary, dated references. Adapt it to the lesson rather than forcing empty sections.
