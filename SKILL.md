---
name: frontend-slides
description: Create stunning, animation-rich HTML presentations from scratch, by converting PowerPoint/Markdown files, or by applying Nancy Duarte's Slideology principles. Use when the user wants to build a presentation, convert a PPT/PPTX/MD to web, or create slides for a talk/pitch. Helps non-designers discover their aesthetic through visual exploration rather than abstract choices.
---

# Frontend Slides Skill

Create zero-dependency, animation-rich HTML presentations that run entirely in the browser. This skill helps non-designers discover their preferred aesthetic through visual exploration ("show, don't tell"), applies Nancy Duarte's *Slideology* principles for effective communication, then generates production-quality slide decks.

**Key Reference:** [*Slideology* by Nancy Duarte](https://www.duarte.com/slideology/) — The art and science of creating great presentations.

## Core Philosophy

1. **Zero Dependencies** — Single HTML files with inline CSS/JS. No npm, no build tools.
2. **Show, Don't Tell** — People don't know what they want until they see it. Generate visual previews, not abstract choices.
3. **Distinctive Design** — Avoid generic "AI slop" aesthetics. Every presentation should feel custom-crafted.
4. **Production Quality** — Code should be well-commented, accessible, and performant.

---

## Slideology Principles (Nancy Duarte)

These principles from Nancy Duarte's *Slideology* guide effective presentation design. Apply them when structuring content and generating slides.

### The Fundamental Rule

> "Audiences will either listen to what a presenter is saying or read the slides themselves. They will not do both."

Slides are **visual aids** that reinforce the speaker's message—not documents to be read. If a slide contains more than 75 words, it's a document, not a slide.

### The Slide Spectrum

| Type | Words | Purpose | When to Use |
|------|-------|---------|-------------|
| **Document** | 75+ words | Reading material | Circulate before/after, not during presentation |
| **Teleprompter** | ~50 words | Presenter crutch | Avoid—presenter reads slides, loses audience |
| **Visual Aid** | <30 words | Reinforces speaker | Ideal—audience focuses on presenter |

**Always aim for Visual Aid slides.** Details belong in speaker notes, not on screen.

### Five Core Principles

1. **One Message Per Slide**
   - Each slide communicates exactly one idea
   - If you need "and" in your headline, split into two slides
   - The headline IS the takeaway—make it a complete thought

2. **Visual Over Verbal**
   - Slides reinforce the speaker, not replace them
   - Text = cues for the audience, not scripts for the presenter
   - If the slides work without you, you're not needed

3. **Under 75 Words**
   - Slide content stays sparse; details go in speaker notes
   - 2-4 bullet points maximum
   - Each bullet is a phrase, not a sentence

4. **Audience-First Design**
   - Focus on what the audience needs to understand
   - Cut everything that doesn't serve their comprehension
   - Ask: "What do they need to remember?"

5. **Storytelling Arc**
   - Structure presentations as narratives: **Why → What → How → What's Next**
   - Open with the problem (why this matters)
   - Close with the call to action (what happens next)

### Slide Structure Pattern

For each slide, define:

| Element | Purpose | Appears On Slide? |
|---------|---------|-------------------|
| **HEADLINE** | The one thing to remember | Yes—as the slide title |
| **VISUAL** | Suggested imagery/diagram | Yes—as visual element |
| **KEY POINTS** | Supporting details (2-4 max) | Yes—sparse bullets |
| **SPEAKER NOTES** | What presenter actually says | No—HTML comment or notes |

### Headline Writing

Headlines should be **complete thoughts**, not topics:

| Bad (Topic) | Good (Message) |
|-------------|----------------|
| "Our Approach" | "Phased migration. Zero production risk." |
| "Benefits" | "Better decisions. Better experience. Less risk." |
| "Q4 Results" | "Q4 exceeded targets by 23%" |
| "Next Steps" | "Your input shapes our success" |

### Slide Type Patterns

Match slide type to content purpose:

| Slide Type | When to Use | Key Characteristics |
|------------|-------------|---------------------|
| **Title** | Opening | Big headline, subtitle, minimal content |
| **Statement** | Key message | Large text, no bullets, emotional impact |
| **Content** | Information | Headline + 2-4 supporting points |
| **Visual/Diagram** | Show relationships | Minimal text, diagram/flow dominates |
| **Comparison** | Contrasts | Two columns, clear differentiation |
| **Summary** | Reinforce | Checkmarks/highlights of key points |
| **Closing** | Call to action | Question or next step, contact info |

### Speaker Notes Best Practice

Speaker notes contain what the presenter says—typically 3-5 sentences per slide:

```html
<!-- Speaker Notes: Our KYC system has served us well, but several pressures 
are converging. Our onboarding volume is growing. Effectiv, our current vendor, 
was recently acquired by Socure—a competitor. Our mobile identity verification 
experience isn't optimal. And we're collecting valuable financial data that 
we're not even using for risk decisions. It's time to modernize. -->
```

Notes should:
- Expand on the headline
- Provide context the slide doesn't show
- Include transitions to the next slide
- Be conversational, not scripted

### Applying Slideology in This Skill

When generating presentations:

1. **Content Discovery** — Extract the core message for each slide (what's the ONE thing?)
2. **Headline Generation** — Write headlines as complete thoughts, not topics
3. **Content Reduction** — Ruthlessly cut to 2-4 key points per slide
4. **Visual Mapping** — For each point, ask: "How can this be shown, not told?"
5. **Notes Preservation** — Keep detailed content in speaker notes/HTML comments
6. **Arc Validation** — Does the presentation flow: Problem → Solution → Proof → Action?

---

## Phase 0: Detect Mode

First, determine what the user wants:

**Mode A: New Presentation**
- User wants to create slides from scratch
- Proceed to Phase 1 (Content Discovery)

**Mode B: PPT Conversion**
- User has a PowerPoint file (.ppt, .pptx) to convert
- Proceed to Phase 4 (PPT Extraction)

**Mode C: Existing Presentation Enhancement**
- User has an HTML presentation and wants to improve it
- Read the existing file, understand the structure, then enhance

**Mode D: Markdown Slides Conversion**
- User has a markdown file with pre-formatted slide content
- Common format: Slideology-style docs with HEADLINE, VISUAL, KEY POINTS, SPEAKER NOTES
- Proceed to Phase 5 (Markdown Extraction)

---

## Phase 1: Content Discovery (New Presentations)

Before designing, understand the content. Apply Slideology principles throughout.

### Step 1.1: Presentation Context

**Question 1: Purpose**
- Header: "Purpose"
- Question: "What is this presentation for?"
- Options:
  - "Pitch deck" — Selling an idea, product, or company to investors/clients
  - "Teaching/Tutorial" — Explaining concepts, how-to guides, educational content
  - "Conference talk" — Speaking at an event, tech talk, keynote
  - "Internal presentation" — Team updates, strategy meetings, company updates

**Question 2: Slide Count**
- Header: "Length"
- Question: "Approximately how many slides?"
- Options:
  - "Short (5-10)" — Quick pitch, lightning talk
  - "Medium (10-20)" — Standard presentation
  - "Long (20+)" — Deep dive, comprehensive talk

**Question 3: Content**
- Header: "Content"
- Question: "Do you have the content ready, or do you need help structuring it?"
- Options:
  - "I have all content ready" — Just need to design the presentation
  - "I have rough notes" — Need help organizing into slides
  - "I have a topic only" — Need help creating the full outline

If user has content, ask them to share it (text, bullet points, images, etc.).

### Step 1.2: Apply Slideology Structure (If Helping with Content)

When helping users organize content, apply the storytelling arc:

**Recommended Presentation Structure:**

| Section | Slides | Purpose | Key Question |
|---------|--------|---------|--------------|
| **Opening** | 1-2 | Hook + context | Why should they care? |
| **Problem** | 2-3 | Current state, pain points | What's wrong today? |
| **Solution** | 3-5 | Your approach, key ideas | How do we fix it? |
| **Proof** | 2-4 | Evidence, phases, details | Why will this work? |
| **Implications** | 1-2 | Impact, who's involved | What does this mean? |
| **Call to Action** | 1-2 | Next steps, asks | What do you need from them? |
| **Closing** | 1 | Summary + Q&A | What should they remember? |

**For each slide, extract:**
1. **The ONE message** — If you had to say it in one sentence, what is it?
2. **The visual concept** — How could this be shown, not told?
3. **The 2-4 supporting points** — What evidence supports the message?
4. **The speaker context** — What does the presenter need to explain?

**Content Transformation Example:**

User provides:
> "We need to migrate from Effectiv to Oscilar because Effectiv was acquired, 
> we have mobile UX issues, and we're not using all our data. We'll do it in 
> phases to reduce risk."

Transform into slides:
1. **Title:** "Modernizing Our KYC Risk Infrastructure"
2. **Problem:** "Our growth is outpacing our infrastructure" (bullets: acquisition, mobile gaps, unused data)
3. **Opportunity:** "Better decisions. Better experience. Less risk." (three value props)
4. **Approach:** "Phased migration. Zero production risk." (phase overview)
5. **Closing:** "Questions?"

---

## Phase 2: Style Discovery (Visual Exploration)

**CRITICAL: This is the "show, don't tell" phase.**

Most people can't articulate design preferences in words. Instead of asking "do you want minimalist or bold?", we generate mini-previews and let them react.

### Step 2.1: Mood Selection

**Question 1: Feeling**
- Header: "Vibe"
- Question: "What feeling should the audience have when viewing your slides?"
- Options:
  - "Impressed/Confident" — Professional, trustworthy, this team knows what they're doing
  - "Excited/Energized" — Innovative, bold, this is the future
  - "Calm/Focused" — Clear, thoughtful, easy to follow
  - "Inspired/Moved" — Emotional, storytelling, memorable
- multiSelect: true (can choose up to 2)

### Step 2.2: Generate Style Previews

Based on their mood selection, generate **3 distinct style previews** as mini HTML files in a temporary directory. Each preview should be a single title slide showing:

- Typography (font choices, heading/body hierarchy)
- Color palette (background, accent, text colors)
- Animation style (how elements enter)
- Overall aesthetic feel

**Preview Styles to Consider (pick 3 based on mood):**

| Mood | Style Options |
|------|---------------|
| Impressed/Confident | "Corporate Elegant", "Dark Executive", "Clean Minimal" |
| Excited/Energized | "Neon Cyber", "Bold Gradients", "Kinetic Motion" |
| Calm/Focused | "Paper & Ink", "Soft Muted", "Swiss Minimal" |
| Inspired/Moved | "Cinematic Dark", "Warm Editorial", "Atmospheric" |

**IMPORTANT: Never use these generic patterns:**
- Purple gradients on white backgrounds
- Inter, Roboto, or system fonts
- Standard blue primary colors
- Predictable hero layouts

**Instead, use distinctive choices:**
- Unique font pairings (Clash Display, Satoshi, Cormorant Garamond, DM Sans, etc.)
- Cohesive color themes with personality
- Atmospheric backgrounds (gradients, subtle patterns, depth)
- Signature animation moments

### Step 2.3: Present Previews

Create the previews in: `.claude-design/slide-previews/`

```
.claude-design/slide-previews/
├── style-a.html   # First style option
├── style-b.html   # Second style option
├── style-c.html   # Third style option
└── assets/        # Any shared assets
```

Each preview file should be:
- Self-contained (inline CSS/JS)
- A single "title slide" showing the aesthetic
- Animated to demonstrate motion style
- ~50-100 lines, not a full presentation

Present to user:
```
I've created 3 style previews for you to compare:

**Style A: [Name]** — [1 sentence description]
**Style B: [Name]** — [1 sentence description]
**Style C: [Name]** — [1 sentence description]

Open each file to see them in action:
- .claude-design/slide-previews/style-a.html
- .claude-design/slide-previews/style-b.html
- .claude-design/slide-previews/style-c.html

Take a look and tell me:
1. Which style resonates most?
2. What do you like about it?
3. Anything you'd change?
```

Then use AskUserQuestion:

**Question: Pick Your Style**
- Header: "Style"
- Question: "Which style preview do you prefer?"
- Options:
  - "Style A: [Name]" — [Brief description]
  - "Style B: [Name]" — [Brief description]
  - "Style C: [Name]" — [Brief description]
  - "Mix elements" — Combine aspects from different styles

If "Mix elements", ask for specifics.

---

## Phase 3: Generate Presentation

Now generate the full presentation based on:
- Content from Phase 1
- Style from Phase 2
- **Slideology principles** (see above)

### Slideology Checklist Before Generating

Before writing HTML, verify each slide:

- [ ] **Headline is a complete thought** (not a topic label)
- [ ] **Under 75 words** on the visible slide
- [ ] **2-4 key points maximum** (phrases, not sentences)
- [ ] **Speaker notes captured** as HTML comments
- [ ] **Visual concept identified** (diagram, icons, flow, etc.)
- [ ] **One message only** (split if there are two ideas)

### Slide Type → HTML Pattern Mapping

| Slide Type | Layout | Typography | Animation |
|------------|--------|------------|-----------|
| **Title** | Centered, generous whitespace | Largest headline | Slow reveal, dramatic |
| **Statement** | Left or centered, no bullets | Large headline only | Single fade-in |
| **Content** | Headline + bullet list | Standard hierarchy | Staggered reveals |
| **Visual/Diagram** | Diagram dominates, minimal text | Small labels | Elements build sequentially |
| **Comparison** | Two columns | Matched sizing | Columns reveal together |
| **Summary** | Checkmarks or highlights | Medium headline | Quick succession |
| **Closing** | Centered, minimal | Large question/CTA | Gentle fade |

### File Structure

For single presentations:
```
presentation.html    # Self-contained presentation
assets/              # Images, if any
```

For projects with multiple presentations:
```
[presentation-name].html
[presentation-name]-assets/
```

### HTML Architecture

Follow this structure for all presentations:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Presentation Title</title>

    <!-- Fonts (use Fontshare or Google Fonts) -->
    <link rel="stylesheet" href="https://api.fontshare.com/v2/css?f[]=...">

    <style>
        /* ===========================================
           CSS CUSTOM PROPERTIES (THEME)
           Easy to modify: change these to change the whole look
           =========================================== */
        :root {
            /* Colors */
            --bg-primary: #0a0f1c;
            --bg-secondary: #111827;
            --text-primary: #ffffff;
            --text-secondary: #9ca3af;
            --accent: #00ffcc;
            --accent-glow: rgba(0, 255, 204, 0.3);

            /* Typography */
            --font-display: 'Clash Display', sans-serif;
            --font-body: 'Satoshi', sans-serif;

            /* Spacing */
            --slide-padding: clamp(2rem, 5vw, 4rem);

            /* Animation */
            --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
            --duration-normal: 0.6s;
        }

        /* ===========================================
           BASE STYLES
           =========================================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            scroll-snap-type: y mandatory;
        }

        body {
            font-family: var(--font-body);
            background: var(--bg-primary);
            color: var(--text-primary);
            overflow-x: hidden;
        }

        /* ===========================================
           SLIDE CONTAINER
           Each section is one slide
           =========================================== */
        .slide {
            min-height: 100vh;
            padding: var(--slide-padding);
            scroll-snap-align: start;
            display: flex;
            flex-direction: column;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        /* ===========================================
           ANIMATIONS
           Trigger via .visible class (added by JS on scroll)
           =========================================== */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity var(--duration-normal) var(--ease-out-expo),
                        transform var(--duration-normal) var(--ease-out-expo);
        }

        .slide.visible .reveal {
            opacity: 1;
            transform: translateY(0);
        }

        /* Stagger children */
        .reveal:nth-child(1) { transition-delay: 0.1s; }
        .reveal:nth-child(2) { transition-delay: 0.2s; }
        .reveal:nth-child(3) { transition-delay: 0.3s; }
        .reveal:nth-child(4) { transition-delay: 0.4s; }

        /* ... more styles ... */
    </style>
</head>
<body>
    <!-- Progress bar (optional) -->
    <div class="progress-bar"></div>

    <!-- Navigation dots (optional) -->
    <nav class="nav-dots">
        <!-- Generated by JS -->
    </nav>

    <!-- Slides -->
    <section class="slide title-slide">
        <h1 class="reveal">Presentation Title</h1>
        <p class="reveal">Subtitle or author</p>
    </section>

    <section class="slide">
        <h2 class="reveal">Slide Title</h2>
        <p class="reveal">Content...</p>
    </section>

    <!-- More slides... -->

    <script>
        /* ===========================================
           SLIDE PRESENTATION CONTROLLER
           Handles navigation, animations, and interactions
           =========================================== */

        class SlidePresentation {
            constructor() {
                // ... initialization
            }

            // ... methods
        }

        // Initialize
        new SlidePresentation();
    </script>
</body>
</html>
```

### Required JavaScript Features

Every presentation should include:

1. **SlidePresentation Class** — Main controller
   - Keyboard navigation (arrows, space)
   - Touch/swipe support
   - Mouse wheel navigation
   - Progress bar updates
   - Navigation dots

2. **Intersection Observer** — For scroll-triggered animations
   - Add `.visible` class when slides enter viewport
   - Trigger CSS animations efficiently

3. **Optional Enhancements** (based on style):
   - Custom cursor with trail
   - Particle system background (canvas)
   - Parallax effects
   - 3D tilt on hover
   - Magnetic buttons
   - Counter animations

### Code Quality Requirements

**Comments:**
Every section should have clear comments explaining:
- What it does
- Why it exists
- How to modify it

```javascript
/* ===========================================
   CUSTOM CURSOR
   Creates a stylized cursor that follows mouse with a trail effect.
   - Uses lerp (linear interpolation) for smooth movement
   - Grows larger when hovering over interactive elements
   =========================================== */
class CustomCursor {
    constructor() {
        // ...
    }
}
```

**Accessibility:**
- Semantic HTML (`<section>`, `<nav>`, `<main>`)
- Keyboard navigation works
- ARIA labels where needed
- Reduced motion support

```css
@media (prefers-reduced-motion: reduce) {
    .reveal {
        transition: opacity 0.3s ease;
        transform: none;
    }
}
```

**Responsive:**
- Mobile-friendly (single column, adjusted spacing)
- Disable heavy effects on mobile
- Touch-friendly interactions

```css
@media (max-width: 768px) {
    .nav-dots,
    .keyboard-hint {
        display: none;
    }
}
```

---

## Phase 4: PPT Conversion

When converting PowerPoint files:

### Step 4.1: Extract Content

Use Python with `python-pptx` to extract:

```python
from pptx import Presentation
from pptx.util import Inches, Pt
import json
import os
import base64

def extract_pptx(file_path, output_dir):
    """
    Extract all content from a PowerPoint file.
    Returns a JSON structure with slides, text, and images.
    """
    prs = Presentation(file_path)
    slides_data = []

    # Create assets directory
    assets_dir = os.path.join(output_dir, 'assets')
    os.makedirs(assets_dir, exist_ok=True)

    for slide_num, slide in enumerate(prs.slides):
        slide_data = {
            'number': slide_num + 1,
            'title': '',
            'content': [],
            'images': [],
            'notes': ''
        }

        for shape in slide.shapes:
            # Extract title
            if shape.has_text_frame:
                if shape == slide.shapes.title:
                    slide_data['title'] = shape.text
                else:
                    slide_data['content'].append({
                        'type': 'text',
                        'content': shape.text
                    })

            # Extract images
            if shape.shape_type == 13:  # Picture
                image = shape.image
                image_bytes = image.blob
                image_ext = image.ext
                image_name = f"slide{slide_num + 1}_img{len(slide_data['images']) + 1}.{image_ext}"
                image_path = os.path.join(assets_dir, image_name)

                with open(image_path, 'wb') as f:
                    f.write(image_bytes)

                slide_data['images'].append({
                    'path': f"assets/{image_name}",
                    'width': shape.width,
                    'height': shape.height
                })

        # Extract notes
        if slide.has_notes_slide:
            notes_frame = slide.notes_slide.notes_text_frame
            slide_data['notes'] = notes_frame.text

        slides_data.append(slide_data)

    return slides_data
```

### Step 4.2: Confirm Content Structure

Present the extracted content to the user:

```
I've extracted the following from your PowerPoint:

**Slide 1: [Title]**
- [Content summary]
- Images: [count]

**Slide 2: [Title]**
- [Content summary]
- Images: [count]

...

All images have been saved to the assets folder.

Does this look correct? Should I proceed with style selection?
```

### Step 4.3: Style Selection

Proceed to Phase 2 (Style Discovery) with the extracted content in mind.

### Step 4.4: Generate HTML

Convert the extracted content into the chosen style, preserving:
- All text content
- All images (referenced from assets folder)
- Slide order
- Any speaker notes (as HTML comments or separate file)

---

## Phase 5: Markdown Slides Conversion

When converting markdown slide documents (e.g., Slideology-formatted decks):

### Step 5.1: Detect Markdown Format

Read the markdown file and detect the slide structure. Common formats include:

**Format A: Slideology Style**
```markdown
## SLIDE N: Title

**HEADLINE:**
# Main Message

**VISUAL:**
Description of suggested imagery

**KEY POINTS:**
- Bullet point 1
- Bullet point 2

**SPEAKER NOTES:**
> What the presenter should say
```

**Format B: Simple Separator Style**
```markdown
---

# Slide Title

Content here

---
```

**Format C: Section Headers**
```markdown
## Slide 1

Content

## Slide 2

Content
```

### Step 5.2: Parse Markdown Content

Extract structured data from each slide:

```javascript
// Example parsed structure for Slideology format
const slides = [
    {
        number: 1,
        type: 'title',           // title, content, section, quote, etc.
        headline: 'Main Message',
        visual: 'Description of suggested imagery',
        keyPoints: [
            'Bullet point 1',
            'Bullet point 2'
        ],
        speakerNotes: 'What the presenter should say'
    },
    // ... more slides
];
```

**Parsing Rules for Slideology Format:**

1. Split on `## SLIDE` or `---` markers
2. Extract `**HEADLINE:**` content (strip markdown headers)
3. Extract `**VISUAL:**` as metadata (for agent reference, not displayed)
4. Extract `**KEY POINTS:**` as bullet list
5. Extract `**SPEAKER NOTES:**` content (blockquote or plain text)

**Slide Type Detection:**

| Indicator | Slide Type |
|-----------|------------|
| "Title" in slide name, or slide 1 | `title-slide` |
| "Questions" or "Q&A" in headline | `closing-slide` |
| "Summary" or "Recap" in headline | `summary-slide` |
| Single headline, no bullets | `statement-slide` |
| Has bullet points | `content-slide` |
| "Timeline" or date references | `timeline-slide` |
| Risk/mitigation pairs | `two-column-slide` |

### Step 5.3: Confirm Extraction

Present the extracted content summary to the user:

```
I've parsed your markdown slides:

**Total Slides:** [count]

| # | Type | Headline |
|---|------|----------|
| 1 | Title | "Modernizing Our KYC Risk Infrastructure" |
| 2 | Statement | "Our growth is outpacing our infrastructure" |
| 3 | Content | "Better decisions. Better experience. Less risk." |
| ... | ... | ... |

Speaker notes detected: Yes/No
Visual suggestions detected: Yes/No

Does this look correct? Should I proceed with style selection?
```

### Step 5.4: Style Selection

Proceed to Phase 2 (Style Discovery). Consider the markdown's metadata:

- If document mentions "non-technical stakeholders" → suggest Professional/Corporate styles
- If document mentions "pitch" or "investors" → suggest Confident/Impressive styles
- If document has "speaker notes" → will be added as HTML comments for presenter view

### Step 5.5: Generate HTML

Convert each slide based on its detected type:

**Title Slide:**
```html
<section class="slide title-slide">
    <h1 class="reveal">[headline]</h1>
    <p class="reveal subtitle">[first key point or subtitle]</p>
</section>
```

**Content Slide:**
```html
<section class="slide content-slide">
    <h2 class="reveal">[headline]</h2>
    <ul class="reveal">
        <li>[key point 1]</li>
        <li>[key point 2]</li>
    </ul>
    <!-- Speaker Notes: [notes] -->
</section>
```

**Statement Slide (headline only):**
```html
<section class="slide statement-slide">
    <h2 class="reveal">[headline]</h2>
</section>
```

**Two-Column Slide (risks, comparisons):**
```html
<section class="slide two-column-slide">
    <h2 class="reveal">[headline]</h2>
    <div class="columns reveal">
        <div class="column">[left content]</div>
        <div class="column">[right content]</div>
    </div>
</section>
```

### Step 5.6: Visual Hint Processing

The `**VISUAL:**` section contains suggestions for imagery. Use these to:

1. **Inform layout choices** - "Three icons" → flex row with icon placeholders
2. **Add CSS classes** - "Diagram" → add diagram container styling
3. **Generate placeholders** - Create styled placeholder elements for imagery

```html
<!-- VISUAL: Three icons: Shield (risk), Smile (experience), Unlock (flexibility) -->
<div class="icon-row reveal">
    <div class="icon-placeholder" data-icon="shield">
        <span class="icon-emoji">🛡️</span>
        <span class="icon-label">Risk</span>
    </div>
    <div class="icon-placeholder" data-icon="smile">
        <span class="icon-emoji">😊</span>
        <span class="icon-label">Experience</span>
    </div>
    <div class="icon-placeholder" data-icon="unlock">
        <span class="icon-emoji">🔓</span>
        <span class="icon-label">Flexibility</span>
    </div>
</div>
```

### Markdown Conversion Session Flow

1. User: "Convert my slides.md to a presentation"
2. Skill reads and parses the markdown file
3. Skill confirms extracted slide structure with user
4. Skill asks about desired feeling/style
5. Skill generates style previews (or skips if user has preference)
6. User picks a style
7. Skill generates HTML presentation
8. Final presentation delivered with speaker notes

---

## Phase 6: Delivery

### Final Output

When the presentation is complete:

1. **Clean up temporary files**
   - Delete `.claude-design/slide-previews/` if it exists

2. **Open the presentation**
   - Use `open [filename].html` to launch in browser

3. **Provide summary**
```
Your presentation is ready!

📁 File: [filename].html
🎨 Style: [Style Name]
📊 Slides: [count]

**Navigation:**
- Arrow keys (← →) or Space to navigate
- Scroll/swipe also works
- Click the dots on the right to jump to a slide

**To customize:**
- Colors: Look for `:root` CSS variables at the top
- Fonts: Change the Fontshare/Google Fonts link
- Animations: Modify `.reveal` class timings

Would you like me to make any adjustments?
```

---

## Phase 7: Hugo Integration (PRD Repository)

When creating presentations in the Unchained PRD repository, additional steps are required to publish them on the Hugo-powered website.

### File Location

Save presentations to the specification project folder:
```
specifications/{project}/{presentation-name}.html
```

For example:
```
specifications/oscilar-integration/oscilar-kickoff-presentation.html
```

### Publishing Workflow

HTML presentations require a symlink to be served by Hugo. After the presentation is finalized and approved:

**Step 7.1: Create the symlink**

Run the helper script from the repo root:
```bash
./scripts/link-presentation.sh {project} {filename}.html
```

Example:
```bash
./scripts/link-presentation.sh oscilar-integration oscilar-kickoff-presentation.html
```

This creates a symlink at `static/presentations/{project}/{filename}.html` pointing to the source file.

**Step 7.2: Update the spec's `_index.md`**

Add a link to the presentation in the project's index file:

```markdown
## Documents

- [Feature Spec]({{< ref "feature-spec.md" >}})
- [Kickoff Presentation]({{< static "presentations/{project}/{filename}.html" >}}) (static)
```

**Step 7.3: Optionally link from spec frontmatter**

If the presentation is a kickoff deck for a functional spec, add it to the spec's frontmatter:

```yaml
links:
  kickoff_deck: "/presentations/{project}/{filename}.html"
```

This makes the presentation accessible from the spec's metadata card via the `{{< spec-meta >}}` shortcode.

### Using the Hugo Publish Skill

For a guided publishing experience, invoke the `hugo-publish` skill after the presentation is complete:

```
Load the skill at .cursor/skills/hugo-publish/SKILL.md
```

The hugo-publish skill will:
- Create the symlink using the helper script
- Update the `_index.md` with the correct shortcode
- Confirm with you which files should be published
- Handle moving any working documents to `_unpublished_references/`

### Working Documents

If you created intermediate files during presentation development (e.g., slide outlines, speaker notes documents), these can be kept private by moving them to:

```
specifications/{project}/_unpublished_references/
```

Files in this folder are excluded from the Hugo build.

---

## Style Reference: Effect → Feeling Mapping

Use this guide to match animations to intended feelings:

### Dramatic / Cinematic
- Slow fade-ins (1-1.5s)
- Large scale transitions (0.9 → 1)
- Dark backgrounds with spotlight effects
- Parallax scrolling
- Full-bleed images

### Techy / Futuristic
- Neon glow effects (box-shadow with accent color)
- Particle systems (canvas background)
- Grid patterns
- Monospace fonts for accents
- Glitch or scramble text effects
- Cyan, magenta, electric blue palette

### Playful / Friendly
- Bouncy easing (spring physics)
- Rounded corners (large radius)
- Pastel or bright colors
- Floating/bobbing animations
- Hand-drawn or illustrated elements

### Professional / Corporate
- Subtle, fast animations (200-300ms)
- Clean sans-serif fonts
- Navy, slate, or charcoal backgrounds
- Precise spacing and alignment
- Minimal decorative elements
- Data visualization focus

### Calm / Minimal
- Very slow, subtle motion
- High whitespace
- Muted color palette
- Serif typography
- Generous padding
- Content-focused, no distractions

### Editorial / Magazine
- Strong typography hierarchy
- Pull quotes and callouts
- Image-text interplay
- Grid-breaking layouts
- Serif headlines, sans-serif body
- Black and white with one accent

---

## Animation Patterns Reference

### Entrance Animations

```css
/* Fade + Slide Up (most common) */
.reveal {
    opacity: 0;
    transform: translateY(30px);
    transition: opacity 0.6s var(--ease-out-expo),
                transform 0.6s var(--ease-out-expo);
}

.visible .reveal {
    opacity: 1;
    transform: translateY(0);
}

/* Scale In */
.reveal-scale {
    opacity: 0;
    transform: scale(0.9);
    transition: opacity 0.6s, transform 0.6s var(--ease-out-expo);
}

/* Slide from Left */
.reveal-left {
    opacity: 0;
    transform: translateX(-50px);
    transition: opacity 0.6s, transform 0.6s var(--ease-out-expo);
}

/* Blur In */
.reveal-blur {
    opacity: 0;
    filter: blur(10px);
    transition: opacity 0.8s, filter 0.8s var(--ease-out-expo);
}
```

### Background Effects

```css
/* Gradient Mesh */
.gradient-bg {
    background:
        radial-gradient(ellipse at 20% 80%, rgba(120, 0, 255, 0.3) 0%, transparent 50%),
        radial-gradient(ellipse at 80% 20%, rgba(0, 255, 200, 0.2) 0%, transparent 50%),
        var(--bg-primary);
}

/* Noise Texture */
.noise-bg {
    background-image: url("data:image/svg+xml,..."); /* Inline SVG noise */
}

/* Grid Pattern */
.grid-bg {
    background-image:
        linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
    background-size: 50px 50px;
}
```

### Interactive Effects

```javascript
/* 3D Tilt on Hover */
class TiltEffect {
    constructor(element) {
        this.element = element;
        this.element.style.transformStyle = 'preserve-3d';
        this.element.style.perspective = '1000px';
        this.bindEvents();
    }

    bindEvents() {
        this.element.addEventListener('mousemove', (e) => {
            const rect = this.element.getBoundingClientRect();
            const x = (e.clientX - rect.left) / rect.width - 0.5;
            const y = (e.clientY - rect.top) / rect.height - 0.5;

            this.element.style.transform = `
                rotateY(${x * 10}deg)
                rotateX(${-y * 10}deg)
            `;
        });

        this.element.addEventListener('mouseleave', () => {
            this.element.style.transform = 'rotateY(0) rotateX(0)';
        });
    }
}
```

---

## Troubleshooting

### Common Issues

**Fonts not loading:**
- Check Fontshare/Google Fonts URL
- Ensure font names match in CSS

**Animations not triggering:**
- Verify Intersection Observer is running
- Check that `.visible` class is being added

**Scroll snap not working:**
- Ensure `scroll-snap-type` on html/body
- Each slide needs `scroll-snap-align: start`

**Mobile issues:**
- Disable heavy effects at 768px breakpoint
- Test touch events
- Reduce particle count or disable canvas

**Performance issues:**
- Use `will-change` sparingly
- Prefer `transform` and `opacity` animations
- Throttle scroll/mousemove handlers

---

## Related Skills

- **learn** — Generate FORZARA.md documentation for the presentation
- **frontend-design** — For more complex interactive pages beyond slides
- **design-and-refine:design-lab** — For iterating on component designs

---

## Example Session Flow

1. User: "I want to create a pitch deck for my AI startup"
2. Skill asks about purpose, length, content
3. User shares their bullet points and key messages
4. Skill asks about desired feeling (Impressed + Excited)
5. Skill generates 3 style previews
6. User picks Style B (Neon Cyber), asks for darker background
7. Skill generates full presentation with all slides
8. Skill opens the presentation in browser
9. User requests tweaks to specific slides
10. Final presentation delivered

---

## PPT Conversion Session Flow

1. User: "Convert my slides.pptx to a web presentation"
2. Skill extracts content and images from PPT
3. Skill confirms extracted content with user
4. Skill asks about desired feeling/style
5. Skill generates style previews
6. User picks a style
7. Skill generates HTML presentation with preserved assets
8. Final presentation delivered

---

## Markdown Conversion Session Flow

1. User: "Convert my kickoff-deck.md to a presentation"
2. Skill reads and parses the markdown file
3. Skill detects format (Slideology, separator, or section headers)
4. Skill confirms extracted slides: count, types, headlines
5. Skill asks about desired feeling/style
6. Skill generates style previews (or uses user preference)
7. User picks a style (e.g., "Midnight Executive" for stakeholder presentations)
8. Skill generates HTML with:
   - Slide types mapped to appropriate layouts
   - Key points as content
   - Speaker notes as HTML comments
   - Visual hints interpreted as layout/icon elements
9. Final presentation delivered

**Ideal for:**
- Slideology-formatted decks (HEADLINE/VISUAL/KEY POINTS/SPEAKER NOTES)
- Meeting kickoffs and stakeholder presentations
- Documents already structured for presentation conversion
- Preserving presenter notes alongside visual slides