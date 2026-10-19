# How to one shot slide shows
## By Daniel Picarello

---

## Step 1 get a good prompt: {.scrollable}

CompTIA PenTest+ validates the ability to **identify, mitigate, and report** system vulnerabilities across modern attack surfaces.

### Here's the one I used:

```markdown
You are an expert presentation designer and content strategist. Your task is to generate a complete slide deck in Pandoc-compatible Reveal.js Markdown based on the topic and structure outlined below.

---

### Presentation Overview & Inputs
- **Topic / Subject:** [e.g., Introduction to Quantum Computing]
- **Target Audience:** [e.g., High school students with a basic physics background]
- **Key Takeaways / Goal:** [e.g., Understand qubits, superposition, and quantum supremacy]
- **Tone & Style:** [e.g., Engaging, professional, concise, educational]
- **Desired Length:** [e.g., 8-12 slides]

---

### Strict Technical Rules (Pandoc + Reveal.js Syntax)

1. **Slide Separation:**
   - Use horizontal rules (`---`) to create standard horizontal slides.
   - Use vertical rules (`--`) ONLY if creating vertical/nested slide stacks.
   - Header levels define slides:
     - `# Slide Title` for top-level/section breaks.
     - `## Slide Title` for standard content slides.

2. **Content Formatting Rules:**
   - Keep text **concise and scannable**. Avoid long paragraphs. Use bullet points (`*` or `-`).
   - Use bolding (`**term**`) for emphasis on key takeaways.
   - Use standard Markdown for code snippets, blockquotes, and tables where applicable.

3. **Reveal.js Attributes & Presenter Notes:**
   - **Slide Backgrounds / Styling:** Attach Reveal.js slide attributes right after the header:
     `## Slide Title {data-background="#1a1a2e" data-transition="zoom"}`
   - **Fragment Animations (Incremental Lists):** Add `.build` or `.incremental` to lists or divs when bullet points should appear step-by-step:
     `::: {.incremental}`
     `- First point`
     `- Second point`
     `:::`
   - **Speaker Notes:** Include speaker notes at the bottom of relevant slides using the Pandoc note block syntax:
     `::: notes`
     `Speaker commentary and key talking points go here.`
     `:::`
   - **Two-Column Layouts:** Use Pandoc div blocks for columns:
     `:::: {.columns}`
     `::: {.column width="50%"}`
     `Left column content`
     `:::`
     `::: {.column width="50%"}`
     `Right column content`
     `:::`
     `::::`

4. **Output Requirements:**
   - Output ONLY the raw Pandoc Reveal.js Markdown inside a single clean code block.
   - Do NOT include intro/outro chat text before or after the code block.

---

### Outline & Content to Include:
[Insert brief outline, raw text notes, or key points you want included across the slides]

```

### QUESTION: Where do you get this?

---

## Step 2: Fill it in with your content {.scrollable}

Modify the prompt to specify your demands;

### Here's what mine looked like after filling it in:

```markdown

You are an expert presentation designer and content strategist. Your task is to generate a complete slide deck in Pandoc-compatible Reveal.js Markdown based on the topic and structure outlined below.

---

### Presentation Overview & Inputs
- **Topic / Subject:** The Comptia Pentest+ Certification
- **Target Audience:** Capstone Cybersecurity Students
- **Key Takeaways / Goal:** Objectives of the Exam and how to prepare
- **Tone & Style:** engaging
- **Desired Length:** less than 15 min reading time

---

### Strict Technical Rules (Pandoc + Reveal.js Syntax)

1. **Slide Separation:**
   - Use horizontal rules (`---`) to create standard horizontal slides.
   - Use vertical rules (`--`) ONLY if creating vertical/nested slide stacks.
   - Header levels define slides:
     - `# Slide Title` for top-level/section breaks.
     - `## Slide Title` for standard content slides.

2. **Content Formatting Rules:**
   - Keep text **concise and scannable**. Avoid long paragraphs. Use bullet points (`*` or `-`).
   - Use bolding (`**term**`) for emphasis on key takeaways.
   - Use standard Markdown for code snippets, blockquotes, and tables where applicable.

3. **Reveal.js Attributes & Presenter Notes:**
   - **Slide Backgrounds / Styling:** Attach Reveal.js slide attributes right after the header:
     `## Slide Title {data-background="#1a1a2e" data-transition="zoom"}`
   - **Fragment Animations (Incremental Lists):** Add `.build` or `.incremental` to lists or divs when bullet points should appear step-by-step:
     `::: {.incremental}`
     `- First point`
     `- Second point`
     `:::`
   - **Speaker Notes:** Include speaker notes at the bottom of relevant slides using the Pandoc note block syntax:
     `::: notes`
     `Speaker commentary and key talking points go here.`
     `:::`
   - **Two-Column Layouts:** Use Pandoc div blocks for columns:
     `:::: {.columns}`
     `::: {.column width="50%"}`
     `Left column content`
     `:::`
     `::: {.column width="50%"}`
     `Right column content`
     `:::`
     `::::`

4. **Output Requirements:**
   - Output ONLY the raw Pandoc Reveal.js Markdown inside a single clean code block.
   - Do NOT include intro/outro chat text before or after the code block.

---

### Outline & Content to Include:
An outline of what i'd like on each slide:
* Slide 1: What is the Pentest+ certification
* Slide 2: What isn't the pentest+ (what this doesn't cover)
* Slide 3: Why I'm choosing to presue it (job relevance)
* Slide 4: How to prepare for the pentest+ / What I'm doing to prepare
* Slide 5: how not to prepare for the pentest+ / what to avoid
* Slide 6: An example lab (incorporate previous slide deck)
* Slide 7: AI and penetration-testing
* Slide 8: What's missing from this exam
* Slide 9: bonus (how to use AI to efficiently make slide decks)
```


---

## Step 3: Hand it off to the AI {.scrollable}

Paste the prompt into an AI Chat

Bonus tip: use multiple and compare the outputs to find one you like

I like https://duck.ai because they let you use different models for free

---

## Step 4: Save the output to a markdown file {.scrollable}

- literally just `deck.md`. 

- Paste the full output into this file.

---

## Step 5: Run pandoc on the markdown file to turn it into a reveal.js slide deck {.scrollable}

- literally just 1 command: `pandoc -t revealjs -s deck.md -o deck.html`

- to learn how to install `pandoc` on your system visit: https://pandoc.org/



---

## Step 6: You're good to go {.scrollable}

- You're now ready to rock. You'll have a file called `deck.html` which can be presented from any browser

---

## What I'm trying to tell you {.scrollable}

###  It's not just about content anymore

- we're living in the age of generative AI. content can be generated in just a few clicks.
- anyone can make a slide deck about any thing in just seconds

### It's all about **DELIVERY**

- be confident
- familiarize yourself with the subject
- smile
- breath deeply 
- speak loudly

---


## View these slides on github

[https://github.com/dpjjjj/oneshotslides]
