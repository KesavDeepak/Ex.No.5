# EXP 5: COMPARATIVE ANALYSIS OF DIFFERENT TYPES OF PROMPTING PATTERNS AND EXPLAIN WITH VARIOUS TEST SCENARIOS

**Aim:** To test and compare how different pattern models respond to broad or unstructured (naïve) prompts versus basic/refined prompts in a technical scenario, and analyze the quality, accuracy, and depth of the generated responses.

### AI Tools Required:

* **Tool:** ChatGPT / OpenAI Large Language Model

---

## Explanation

### Definition of Prompt Types

1. **Naïve Prompt:** A short, simple prompt containing minimal instructions, context, or constraints.
2. **Basic / Refined Prompt:** A clear, detailed, and structured prompt that incorporates specific prompting patterns (e.g., Persona Pattern, Pedagogical Breakdown Pattern, Output Format Pattern) to provide context, constraints, and explicit formatting.

---

## Single Test Scenario & Experimental Execution

### Scenario: Technical Concept Explanation

* **Task:** Explain the concept of recursion in computer science.

#### 1. Naïve Prompt Execution

* **Naïve Prompt:** "What is recursion?"
* **Naïve Response:** "Recursion is a programming concept where a function calls itself to solve a smaller instance of the same problem. A recursive function must have a base case to stop calling itself; otherwise, it will result in an infinite loop or stack overflow error."

#### 2. Basic / Refined Prompt Execution (Patterns Applied: Persona, Structural Decomposition, & Syntax Patterns)

* **Basic / Refined Prompt:** "Explain recursion to an undergraduate computer science student. Include a breakdown of base cases vs. recursive steps, a brief Python code example calculating a factorial, and an explanation of how the call stack handles the execution."
* **Refined Response:**
"Recursion is a method of solving a problem where the solution depends on solutions to smaller instances of the same problem.
### 1. Structural Components


* **Base Case:** The terminating condition that stops recursion and returns a value without making further recursive calls.
* **Recursive Step:** The logic that reduces the problem size and invokes the function again.


### 2. Code Example (Python)


```python
def factorial(n):
    if n <= 1:  # Base Case
        return 1
    return n * factorial(n - 1)  # Recursive Step

```


### 3. The Call Stack Mechanics


When `factorial(3)` is called, execution frames are pushed onto the call stack:
1. `factorial(3)` calls `factorial(2)`
2. `factorial(2)` calls `factorial(1)`
3. `factorial(1)` hits the base case and returns `1`.


The stack unwinds in reverse order ($1 \rightarrow 2 \rightarrow 6$) until the original call evaluates to `6`."

---

## Deliverables & Output Analysis

### Evaluation Table

| Test Scenario | Prompt Type | Quality (1–5) | Accuracy (1–5) | Depth (1–5) | Average Score |
| --- | --- | --- | --- | --- | --- |
| **Technical Concept Explanation** | Naïve Prompt | 4.0 | 5.0 | 3.0 | **4.00** |
| **Technical Concept Explanation** | Basic / Refined Prompt | 5.0 | 5.0 | 4.8 | **4.93** |

---

### Score Improvement Summary Table

| Test Scenario | Naïve Avg. Score | Basic/Refined Avg. Score | Absolute Improvement |
| --- | --- | --- | --- |
| **Technical Concept Explanation** | 4.00 | 4.93 | **+0.93** |

---

## Detailed Analysis

1. **Impact of Prompt Clarity on Response Parameters:**
* **Quality:** The refined prompt utilized structural patterns (Markdown sections, code blocks, numbered lists) to make the content structured and readable.
* **Accuracy:** Both prompts achieved full accuracy ($5.0$), demonstrating that LLMs maintain strong baseline factual correctness for standard technical definitions regardless of prompt length.
* **Depth:** Specifying target components (base cases, call stack mechanics, Python syntax) increased the depth score significantly ($3.0 \rightarrow 4.8$).


2. **Does ChatGPT Consistently Provide Better Results with Basic Prompts?**
* Yes. The structured basic prompt yielded a far superior educational explanation (+0.93 overall improvement) compared to the simple definition produced by the naïve prompt.


3. **Are There Scenarios Where Naïve Prompts Work Equally Well?**
* A naïve prompt works adequately when the user only needs a brief, top-level definition or quick reference. However, when the goal is comprehensive understanding, instruction, or implementation, refined prompting is necessary.



---

## Summary of Findings & Best Practices

* **Define Target Audience:** Explicitly assigning an audience (e.g., "undergraduate CS student") sets the correct technical depth.
* **Specify Required Artifacts:** Prompting for syntax examples (Python) and execution traces (call stack) ensures a complete explanation.
* **Enforce Section Formatting:** Utilizing structured lists and section headers prevents paragraph-heavy, disorganized output.

---

# RESULT: The prompt for the above said problem executed successfully


