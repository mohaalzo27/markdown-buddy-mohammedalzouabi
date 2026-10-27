# Reflection Questions

AI Assistance Declaration: I used Grok (xAI, Grok 4.7, October 26, 2026) for structuring reflection responses and ensuring they addressed assignment objectives. Prompts used included requests to outline strengths and weaknesses of AI for Markdown documentation and to draft ethical considerations. I verified and substantially rewrote all responses for personal accuracy and originality. All final reflections are my own.

## Question 1: What are the strengths and weaknesses of using AI tools to draft Markdown documentation for R projects?

Strengths include speed and consistency. AI quickly produced a well-organized list of standard sections (Overview, Installation, Example Usage, Dependencies, License) that matched recommendations from the GitHub Markdown Guide and tidyverse-style repositories. It also generated clean code blocks and header hierarchy with almost no syntax errors on the first pass. This saved time compared with writing everything from scratch and helped me focus on content rather than formatting.

Weaknesses appeared in specificity and tone. The initial draft was slightly generic and included placeholder language that did not fully match my synthetic retail sales project. It occasionally over-explained simple steps or used phrasing that felt less concise than professional READMEs I reviewed (for example, the tidyverse package README). I had to manually tighten the language, remove unnecessary sentences, and ensure every section accurately described only what the project actually does. AI is useful for structure but still requires human judgment for project-specific accuracy.

## Question 2: How did you verify and refine the AI-generated content to ensure it was accurate and professional?

I followed the verification pattern suggested in the assignment. First, I compared the AI-proposed section list against a real tidyverse repository README and the official GitHub Markdown Guide. Second, I pasted the generated Markdown into a local preview tool and into GitHub’s file preview to confirm that headers, bullet lists, and fenced code blocks rendered correctly. Third, I performed a self spot-check by reading the README aloud and checking that every claim (package names, column names, workflow steps) matched the actual script I documented.

Refinements included: adding a clear Project Structure section, shortening the Overview for conciseness, adjusting the example code to use realistic column names from the synthetic dataset, and moving the AI disclosure to the bottom exactly as required. For the .Rmd file, I verified that code chunks used proper R Markdown syntax (` ```{r} `) and that header levels created a logical hierarchy. These checks took less than 15 minutes but removed several small clarity issues that the AI draft contained.

## Question 3: What ethical practices did you apply when using AI for this assignment, and what did you learn about AI-assisted workflows?

I applied three ethical practices. First, I disclosed every AI tool, version, date, and main prompts in both the README and the top of the .Rmd and Reflection files. Second, I never uploaded real or personal data; the project uses only synthetic sales figures. Third, I treated the AI as a design assistant rather than a final author: every section was reviewed, edited, and validated by me before inclusion.

What I learned is that AI-assisted documentation is most effective when paired with deliberate verification. The tool accelerates the first draft and reduces formatting mistakes, but it does not replace understanding the project or checking outputs against real standards. Clear attribution and a short reflection on the process also make the workflow transparent and academically honest. Going forward, I will continue using AI for structure and boilerplate while keeping content ownership and final accuracy firmly in my own hands.
