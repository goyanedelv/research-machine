---
description: Pipeline to autonomously generate an academic paper on a user-provided topic.
---
# Generate Paper Workflow

This workflow guides Antigravity to step through the Academic Research Machine pipeline to construct a fully researched, formally written markdown paper.

1. **Understand Topic**: Identify the academic topic the user wants a paper on.
2. **Phase 1: Web Research**
   - Read the `.agent/skills/web_research_agent/SKILL.md`.
   - Act as the Web Research Agent: perform deep web retrieval, browser navigation, and information clustering.
   - Save the raw output, including identified references, to `research_notes/`.
3. **Phase 2: Reference Verification**
   - Read the `.agent/skills/reference_verification_agent/SKILL.md`.
   - Act as the Verifier: validate the scraped links and DOIs from the notes to prevent hallucination.
   - Save the cleaned bibliography to `references/`.
4. **Phase 3: Writing & Synthesis**
   - Read the `.agent/skills/writing_agent/SKILL.md`.
   - Act as the Writing Agent: read the references and notes. Synthesize everything into a standard academic format with accurate inline citations formatting.
   - Save the final paper to `output_document/`.
5. **Final Output**
   - Present the final file paths and a brief overview of the outcomes to the user.
