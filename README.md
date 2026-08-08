# EXP 5: COMPARATIVE ANALYSIS OF DIFFERENT TYPES OF PROMPTING PATTERNS AND EXPLAIN WITH VARIOUS TEST SCENARIOS

**Aim:** To test and compare how different pattern models respond to broad or unstructured (naïve) prompts versus basic/refined prompts across multiple test scenarios, and analyze the quality, accuracy, and depth of the generated responses.

### AI Tools Required:

* **Tool:** ChatGPT / OpenAI Large Language Model

---

## Explanation

### Definition of Prompt Types

1. **Naïve Prompt:** A short, simple prompt containing minimal instructions, context, or constraints.
2. **Basic / Refined Prompt:** A clear, detailed, and structured prompt that incorporates specific prompting patterns (e.g., Persona Pattern, Template Pattern, Format Pattern) to provide context, constraints, and explicit output formatting.

---

## Test Scenarios & Experimental Execution

### Scenario 1: Creative Story Generation

* **Naïve Prompt:** "Write a story about a clockmaker."
* **Naïve Response:** "In a small, quiet town, an old clockmaker named Tobias spent his days repairing pocket watches and grand cuckoo clocks. One evening, a stranger brought in an ornate silver timepiece that had stopped at 11:11. Tobias opened the back casing and discovered intricate gears made of an unfamiliar dark metal. As he moved the central gear, time outside his workshop paused entirely. Realizing the clock controlled local time, Tobias carefully tuned its mainspring to reset the moment, restoring movement to the town and placing the clock safely in his vault."
* **Basic / Refined Prompt (Pattern Applied: Persona & Structural Constraint Pattern):** "Act as an atmospheric fantasy writer. Write a 200-word story about a clockmaker in 19th-century Prague who discovers a watch that ticks backward. Focus on sensory details (sound and light) and end with a cliffhanger."
* **Refined Response:** "Amber lantern light flickered across the dust-streaked windows of Master Aris’s Old Town workshop. Rain lashed against the leaded glass as he inspected a brass pocket watch delivered by an unmarked carriage. Its face was inverted; its ticking, a hollow, rhythmic *clack-tick* that vibrated up his brass tweezers. When Aris turned the winding crown, the candle flame beside him unburned, elongating from a dying spark into a full yellow pillar. Outside, the steady patter of raindrops reversed, rising from the cobblestones toward the black sky. Panic seized his chest as the second hand swept counterclockwise past twelve, and a forgotten voice called his name from the dark doorway behind him."

---

### Scenario 2: Factual Question Answering

* **Naïve Prompt:** "Why did the Roman Empire fall?"
* **Naïve Response:** "The Roman Empire fell due to a combination of internal and external factors. Key reasons include continuous invasions by barbarian tribes, economic instability and over-taxation, political corruption and instability, military overexpansion, and the division of the empire into Eastern and Western halves."
* **Basic / Refined Prompt (Pattern Applied: Categorization & Historical Specifier Pattern):** "Explain the primary causes of the fall of the Western Roman Empire in 476 AD. Categorize the reasons into Economic, Military, and Political factors, providing at least one specific historical example or term for each."
* **Refined Response:**
"**1. Economic Factors:** Severe inflation, debasement of currency, and over-taxation crippled trade. The empire relied heavily on slave labor, which stagnated technological innovation and agrarian productivity.
**2. Military Factors:** Reliance on Germanic mercenaries (*foederati*) weakened loyalty and discipline. Continuous incursions by barbarian groups—such as the Sack of Rome by Alaric’s Visigoths in 410 AD—gradually dismantled Western territorial control.
**3. Political Factors:** Systemic corruption and instability plagued the imperial seat (e.g., the Crisis of the Third Century). The structural division of the empire by Diocletian in 285 AD permanently diverted economic and military resources away from Rome toward Constantinople."

---

### Scenario 3: Summarization

* **Naïve Prompt:** "Summarize this text: Remote work has reshaped global labor dynamics over the past decade. While employees cite increased flexibility and eliminated commute times as major benefits, organizations face challenges regarding corporate culture and onboarding. Studies indicate productivity remains stable or slightly increases for individual contributor tasks, but collaborative creative processes often experience friction. Additionally, blurred lines between work and personal life have led to reported increases in employee burnout."
* **Naïve Response:** "Remote work offers flexibility and removes commutes, keeping individual productivity stable. However, companies struggle with culture and onboarding, collaboration can suffer, and blurred boundaries cause burnout."
* **Basic / Refined Prompt (Pattern Applied: Template / Explicit Bullet Pattern):** "Summarize the text into exactly three bullet points: one covering Employee Benefits, one covering Organizational Challenges, and one covering Overall Productivity Impact."
* **Refined Response:**
* **Employee Benefits:** Staff gain schedule flexibility and eliminate daily commutes, though they risk burnout due to overlapping personal and professional boundaries.
* **Organizational Challenges:** Companies experience difficulties maintaining corporate culture, managing onboarding, and facilitating smooth collaborative creative processes.
* **Overall Productivity Impact:** Individual contributor output remains stable or slightly improves, whereas group collaboration encounters operational friction.



---

### Scenario 4: Advice or Recommendation

* **Naïve Prompt:** "How can I prepare for a job interview?"
* **Naïve Response:** "To prepare for a job interview: research the company, review the job description, practice common interview questions, dress appropriately, bring copies of your resume, arrive early, and send a thank-you email afterward."
* **Basic / Refined Prompt (Pattern Applied: Actionable Framework / Role Pattern):** "I have a senior software engineer interview in two weeks focusing on system design and behavioral questions. Provide a structured 3-step preparation framework including specific methodologies for answering questions."
* **Refined Response:**
"**Step 1: Master the STAR Method for Behavioral Questions**
Structure responses using **S**ituation, **T**ask, **A**ction, and **R**esult. Prepare 4–5 core stories highlighting leadership, conflict resolution, and handling architectural failure. Quantify results (e.g., 'reduced latency by 30%').
**Step 2: System Design Architecture Practice**
Review foundational distributed systems concepts: load balancing, caching strategies, database sharding, and CAP theorem. Practice sketching end-to-end architectures using the framework: Clarify Requirements $\rightarrow$ Define API $\rightarrow$ High-Level Design $\rightarrow$ Deep Dive bottlenecks.
**Step 3: Mock Interviews & Company Alignment**
Conduct at least two timed mock system design sessions. Research the target company’s engineering blog to understand their technical stack and recent architectural shifts."

---

### Scenario 5: Technical Concept Explanation

* **Naïve Prompt:** "What is recursion?"
* **Naïve Response:** "Recursion is a programming concept where a function calls itself to solve a smaller instance of the same problem. A recursive function must have a base case to stop calling itself; otherwise, it will result in an infinite loop or stack overflow error."
* **Basic / Refined Prompt (Pattern Applied: Pedagogical Breakdown & Syntax Pattern):** "Explain recursion to an undergraduate computer science student. Include a breakdown of base cases vs. recursive steps, a brief Python code example calculating a factorial, and an explanation of how the call stack handles the execution."
* **Refined Response:**
"Recursion is a method of solving a problem where the solution depends on solutions to smaller instances of the same problem.
### 1. Structural Components


* **Base Case:** The terminating condition that stops recursion and returns a value without further calls.
* **Recursive Step:** The logic that reduces the problem size and calls the function again.


### 2. Code Example (Python)


```python
def factorial(n):
    if n <= 1:  # Base Case
        return 1
    return n * factorial(n - 1)  # Recursive Step

```


### 3. The Call Stack Mechanics


When `factorial(3)` is called, memory frames are pushed onto the call stack:
1. `factorial(3)` calls `factorial(2)`
2. `factorial(2)` calls `factorial(1)`
3. `factorial(1)` hits the base case and returns `1`.


The stack unwinds in reverse order ($1 \rightarrow 2 \rightarrow 6$) until the original call evaluates to `6`."

---

## Deliverables & Output Analysis

### Comparison Table Across All Test Scenarios

| Test Scenario | Prompt Type | Quality (1–5) | Accuracy (1–5) | Depth (1–5) | Average Score |
| --- | --- | --- | --- | --- | --- |
| **1. Creative Story** | Naïve Prompt | 3.5 | 5.0 | 2.5 | **3.67** |
| **1. Creative Story** | Basic / Refined Prompt | 4.8 | 5.0 | 4.5 | **4.77** |
| **2. Factual Question** | Naïve Prompt | 4.0 | 4.5 | 3.0 | **3.83** |
| **2. Factual Question** | Basic / Refined Prompt | 4.8 | 5.0 | 4.5 | **4.77** |
| **3. Summarization** | Naïve Prompt | 4.0 | 5.0 | 3.0 | **4.00** |
| **3. Summarization** | Basic / Refined Prompt | 5.0 | 5.0 | 4.2 | **4.73** |
| **4. Advice & Rec.** | Naïve Prompt | 3.5 | 4.5 | 2.5 | **3.50** |
| **4. Advice & Rec.** | Basic / Refined Prompt | 4.8 | 5.0 | 4.8 | **4.87** |
| **5. Technical Explanation** | Naïve Prompt | 4.0 | 5.0 | 3.0 | **4.00** |
| **5. Technical Explanation** | Basic / Refined Prompt | 5.0 | 5.0 | 4.8 | **4.93** |

---

### Score Improvement Summary Table

| Test Scenario | Naïve Avg. Score | Basic/Refined Avg. Score | Absolute Improvement |
| --- | --- | --- | --- |
| **Creative Story Generation** | 3.67 | 4.77 | **+1.10** |
| **Factual Question Answering** | 3.83 | 4.77 | **+0.94** |
| **Summarization** | 4.00 | 4.73 | **+0.73** |
| **Advice or Recommendation** | 3.50 | 4.87 | **+1.37** |
| **Technical Concept Explanation** | 4.00 | 4.93 | **+0.93** |

---

## Detailed Analysis

1. **Impact of Prompt Clarity on Response Parameters:**
* **Quality:** Refined prompts with explicit formatting constraints (e.g., bullet points, numbered steps, code blocks) eliminate conversational filler and improve structural readability.
* **Accuracy:** Factuality remains relatively high across both prompt types due to LLM pre-training. However, refined prompts reduce ambiguity and hallucination risks by specifying target sub-domains (e.g., "Western Roman Empire in 476 AD" vs general "Roman Empire").
* **Depth:** Additional context (personas, target audience, technical requirements) directly correlates with increased response depth and detail density.


2. **Does ChatGPT Consistently Provide Better Results with Basic Prompts?**
* Yes. Across all five scenarios, the structured basic prompts outperformed naïve prompts, achieving higher average scores.


3. **Are There Scenarios Where Naïve Prompts Work Equally Well?**
* For straightforward factual retrieval and brief text summarization, naïve prompts achieve high accuracy ($5.0$). When brief, top-level answers are sufficient, naïve prompting is adequate. However, for specialized tasks, actionable advice, or formatted technical content, refined prompting is strictly necessary.



---

## Summary of Findings & Best Practices

* **Persona & Audience Assignment:** Defining target audiences (e.g., "undergraduate CS student") sets the correct complexity level.
* **Output Format Enforcement:** Requesting specific structural schemas (e.g., Markdown tables, numbered steps, code blocks) prevents disjointed paragraphs.
* **Constraint Boundaries:** Setting explicit parameters (word count, specific sub-topics, excluded terms) ensures conciseness and high information density.

---

# RESULT: The prompt for the above said problem executed successfully
