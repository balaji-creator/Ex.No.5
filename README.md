

# EXP 5: COMPARATIVE ANALYSIS OF DIFFERENT TYPES OF PROMPTING PATTERNS AND EXPLAIN WITH VARIOUS TEST SCENARIOS

# Aim: To test and compare how different pattern models respond to various prompts (broad or unstructured) versus basic prompts (clearer and more refined) across multiple scenarios.  Analyze the quality, accuracy, and depth of the generated responses 

### AI Tools Required: 

# Explanation: 
Define the Two Prompt Types:

Write a basic Prompt: Clear, detailed, and structured prompts that give specific instructions or context to guide the model.
Based on that pattern type refined the prompt and submit that with AI tool.
Get the ouput and write the report.

Prepare Multiple Test Scenarios:
Select various scenarios such as:
Generating a creative story.
Answering a factual question.
Summarizing an article or concept.
Providing advice or recommendations.
Or Any other test scenario
For each scenario, create both a naïve and a basic prompt. Ensure each pair of prompts targets the same task but with different levels of structure.
Run Experiments with ChatGPT:
Input the naïve prompt for each scenario and record the generated response.
Then input the corresponding basic prompt and capture that response.
Repeat this process for all selected scenarios to gather a full set of results.
Evaluate Responses : 
	Compare how ChatGPT performs when given naïve versus basic prompts and analyze the output based on Quality,Accuracy and Depth. Also analyse does ChatGPT consistently provide better results with basic prompts? Are there scenarios where naïve prompts work equally well?
Deliverables:
A table comparing ChatGPT's responses to naïve and basic prompts across all scenarios.
Analysis of how prompt clarity impacts the quality, accuracy, and depth of ChatGPT’s outputs.
Summary of findings with insights on how to structure prompts for optimal results when using ChatGPT.


# OUTPUT
1) BASIC PROMPT (baseline)
Aim

Get a short, clear explanation of the greenhouse effect for a high-school student.

Apparatus required

A language model (e.g., ChatGPT), prompt text box.

Theory

A direct instruction with minimal context relies on the model's default knowledge and style. Fast and simple, but can be vague about tone, length or level.

Procedure

Prompt used:

Explain the greenhouse effect in 2–3 sentences for a high-school student.


Test scenarios:

S1 — Simple: as written.

S2 — Ambiguous audience: replace "high-school student" with "engineer".

S3 — Edge case length: ask for 1 sentence instead of 2–3.

Output (example)

S1: “The greenhouse effect happens when gases such as carbon dioxide and methane trap heat in Earth’s atmosphere. Sunlight warms Earth’s surface, and greenhouse gases absorb and re-emit that heat, keeping the planet warmer than it would be otherwise.”

S2 (engineer): model may still give a similar answer but possibly more technical terms.

S3 (1 sentence): model compresses content into a single sentence; risk of losing clarity.

Notes: Basic prompt is quick but can be under-specified (tone, detail, examples).

2) ZERO-SHOT PROMPT (explicit constraints, no examples)
Aim

Produce a constrained, predictable short explanation without examples.

Apparatus required

Same as above.

Theory

Zero-shot: give clearer instructions about style, format, and constraints so the model has less room to guess. No demonstrations are provided.

Procedure

Prompt used:

In exactly 2–3 sentences, explain the greenhouse effect for a high-school student. Use no technical equations, include one concrete example (e.g., CO₂ from cars), and end with a short sentence on why it matters.


Test scenarios:

Z1 — Standard: run as written.

Z2 — Different audience: change “high-school student” → “10-year-old child”.

Z3 — Domain twist: request inclusion of one simple analogy.

Output (example)

Z1: “The greenhouse effect occurs when gases like CO₂ and methane trap heat radiating from Earth, warming the atmosphere. For example, CO₂ from car exhaust adds to these gases and helps hold heat close to the surface. This matters because increased greenhouse gases lead to climate change and affect weather, sea level, and ecosystems.”

Notes: Zero-shot gives more control (format, constraints) without requiring examples. Good for predictable outputs.

3) FEW-SHOT PROMPT (provide examples)
Aim

Steer style, tone and structure by showing examples — increases consistency and reduces ambiguity.

Apparatus required

Language model plus two or more example input→output pairs embedded in the prompt.

Theory

Few-shot prompting shows demonstrations of the desired mapping from instruction to output. The model generalizes the pattern to the new input, usually producing outputs that mimic the examples’ style and detail level.

Procedure

Prompt used (examples included):

Example 1:
Task: Explain photosynthesis in 2–3 sentences for a high-school student.
Output: "Photosynthesis is the process plants use to turn sunlight, water, and CO₂ into glucose and oxygen. Chlorophyll in leaves captures light energy to power this change, which provides food for the plant and oxygen for the atmosphere."

Example 2:
Task: Explain the water cycle in 2–3 sentences for a high-school student.
Output: "The water cycle describes how water evaporates from surfaces, forms clouds, and returns as precipitation, then flows back to rivers and oceans. Sun energy drives evaporation and gravity drives runoff, keeping water moving through the environment."

Now:
Task: Explain the greenhouse effect in 2–3 sentences for a high-school student.
Output:


Test scenarios:

F1 — Standard: use the prompt as above.

F2 — More formal style: alter examples to be more formal to see effect.

F3 — Include or omit analogies in examples: test sensitivity to demonstration content.

Output (example)

F1: “The greenhouse effect happens when gases like carbon dioxide and methane trap heat radiating from Earth, warming the atmosphere and surface. These gases act like a blanket—for example, CO₂ from cars increases the blanket’s thickness and traps more heat. As a result, global temperatures can rise, altering climates and ecosystems.”

Notes: Few-shot is powerful for controlling style/level. The model often mirrors the phrasing and structure shown in examples.

4) CHAIN-OF-THOUGHT STYLE PROMPT (stepwise reasoning shown)
Aim

Request stepwise reasoning and an explicit final summary to ensure transparency in how the answer was reached.

Apparatus required

Language model that can produce multi-step outputs. (When using any model, prefer an instruction to provide structured reasoning rather than raw internal chain-of-thought. See safety notes.)

Theory

Asking the model to show reasoning steps can help users trace how the model arrived at the final answer and can improve correctness for some tasks. However, large models’ internal chain-of-thought is private; instead we request an explainable stepwise justification that is safe to show.

Procedure

Prompt used:

You are a teacher. For the task below, do two parts:
1) Write numbered, short reasoning steps (one or two lines each) that explain the key points you will include.
2) Then give a concise final answer (2–3 sentences) for a high-school student.

Task: Explain the greenhouse effect in 2–3 sentences for a high-school student.


Test scenarios:

C1 — Standard: as written.

C2 — Request more steps: ask for 4–6 steps.

C3 — Ask for misconception check: add a final bullet correcting a common misconception.

Output (example)

(1) Reasoning steps

Define what the greenhouse effect is in simple terms.

Identify main greenhouse gases (CO₂, CH₄) and their source (e.g., cars, agriculture).

Explain mechanism briefly (sunlight in → heat trapped by gases).

Give one concrete example to make it tangible.

State the consequence/why it matters.
# RESULT: The prompt for the above said problem executed successfully
