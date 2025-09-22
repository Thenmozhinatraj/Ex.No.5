

# EXP 5: COMPARATIVE ANALYSIS OF DIFFERENT TYPES OF PROMPTING PATTERNS AND EXPLAIN WITH VARIOUS TEST SCENARIOS

# Aim: 
To test and compare how different pattern models respond to various prompts (broad or unstructured) versus basic prompts (clearer and more refined) across multiple scenarios. Analyze the quality, accuracy, and depth of the generated responses 

### AI Tools Required: 
1. ChatGPT (or any Generative AI tool supporting LLMs)

2. Text editor/Word processor for documentation

3. Spreadsheet/Tabular tool for comparison

# Explanation: 
- Large Language Models like ChatGPT generate text depending on the context provided in the prompt.
- If the prompt is vague, the model has to “guess” the intention, which may lead to generic or incomplete results.
- When the prompt is structured and explicit, the model can focus on relevant details, leading to more accurate, richer, and well-organized answers.

# Types of Prompts

Naïve Prompt
Definition: A broad or unstructured prompt with minimal guidance.
Example: “Write a story.”
Expected Output: Often short, generic, and lacking depth because the AI receives little direction.

Basic / Structured Prompt
Definition: A clear, detailed prompt providing specific instructions, context, and desired style or constraints.
Example: “Write a 300-word science-fiction story set on Mars about a scientist who discovers alien life, maintaining a suspenseful tone.”
Expected Output: Richer content, coherent structure, and better alignment with the user’s intention.

# Procedure

1. Define Prompt Types
- Created paired prompts (one naïve and one basic) for each chosen task.
  
2. Select Multiple Test Scenario
- Creative story generation.
- Answering a factual question.
- Summarising an article or concept.
- Providing advice or recommendations.
  
3. Run Experiments
- Input the naïve prompt into ChatGPT and record the generated output.
- Input the corresponding basic prompt and capture its output.
- Repeated the process for all selected scenarios.
  
4. Evaluate Responses
- Analysed and compared outputs on Quality (coherence, richness)
- Accuracy (correctness of information), and
- Depth (level of detail, completeness).
- Observed whether basic prompts consistently outperform naïve prompts,and noted any situations where naïve prompts worked equally well.

# OUTPUT
<img width="700" height="254" alt="image" src="https://github.com/user-attachments/assets/ad9354bf-6e3c-49c9-9e55-ab26df696e70" />


# Chatgpt:
- Naive prompt:
- Input:
“Summarize the following article about renewable energy.”

### Article Excerpt for Testing
- Renewable energy comes from natural sources like sunlight, wind, rain, tides, and geothermal heat. Unlike fossil fuels, these sources are naturally replenished. In recent years, solar and wind power have grown rapidly as technology costs fall. Governments worldwide are investing heavily in renewable infrastructure to cut carbon emissions and combat climate change. However, challenges remain, including energy storage, grid integration, and balancing supply with demand.

Typical Output:

- “Renewable energy uses natural sources such as sun, wind, water, and heat from the earth. It is increasing globally because it helps reduce carbon emissions and fight climate change, though storage and grid issues still need solutions.”

### Basic (Structured) Prompt

- Input:
“Summarize the following article about renewable energy in 150–180 words.
- Highlight the main sources.
- Explain why global adoption is increasing.
- Mention at least two key challenges.
- Write in simple language suitable for high-school students.”

### Article Excerpt for Testing

Renewable energy comes from natural sources like sunlight, wind, rain, tides, and geothermal heat. Unlike fossil fuels, these sources are naturally replenished. In recent years, solar and wind power have grown rapidly as technology costs fall. Governments worldwide are investing heavily in renewable infrastructure to cut carbon emissions and combat climate change. However, challenges remain, including energy storage, grid integration, and balancing supply with demand.

### Typical Output:

“Renewable energy refers to power derived from naturally replenishing sources such as sunlight, wind, rain, tides, and geothermal heat. These resources are becoming the focus of worldwide energy policy because they reduce dependence on fossil fuels and help cut carbon emissions, a major driver of climate change. Falling technology costs have made solar and wind power especially attractive, prompting governments to invest heavily in renewable infrastructure. Despite this progress, several challenges remain. Energy storage systems must improve to ensure a steady power supply when sunlight or wind is unavailable, and electrical grids need upgrades to handle the variable output from renewable sources. Balancing energy supply with fluctuating demand is another ongoing issue. Addressing these problems will be essential for a smooth global transition to clean, sustainable energy.”

# Gemini:
- Naive Prompt
Scenario: Creative Story Generation

- Naive Prompt: Tell me a story.

- AI Output:
"Once upon a time, in a land far away, lived a brave knight. He went on an adventure, fought a dragon, and rescued a princess. They lived happily ever after."

### Basic/Structured Prompt:
Scenario: Creative Story Generation

Basic/Structured Prompt: Write a 300-word story set on Mars about a scientist who discovers alien life, using a suspenseful tone.

### AI Output (Summary):

"Dr. Anya Sharma adjusted her helmet, the crimson dust of Mars swirling around her habitat. For weeks, the seismic sensors had pinged with anomalous readings beneath Olympus Mons—too regular for natural phenomena. Today, she'd finally reached the deepest anomaly. Her drilling probe breached a cavern, revealing a faint, bioluminescent glow. As she lowered a camera, strange, crystalline spores drifted into view, vibrating with an eerie, rhythmic hum. A sudden tremor shook the chamber, and a fissure cracked open in the cavern floor, a deeper light pulsing within. Anya's comms crackled with static, isolating her. Was it truly life, or something far more ancient and menacing awakening?"

<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/6dd01af0-f617-4cdf-9720-82af99badea4" />

## Prompt:
1. Zero-Shot Prompting (New Example)
Explanation: The model performs a task directly without any examples, relying on its general knowledge.

- New Example:
Prompt: "What is the capital of France?"

- Expected AI Output: "Paris"
<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/d49aa1b5-ecf1-4a6f-b8d5-7e9119510859" />

2. Few-Shot Prompting (New Example)
Explanation: The model is given a few examples to understand the pattern before solving a new problem.

- New Example:
Prompt:
"Identify the odd one out in the following lists:

```
Apple, Banana, Carrot, Orange -> Carrot
Dog, Cat, Bird, Table -> Table
Chair, Desk, Sofa, Book -> ?"

```
- Expected AI Output: "Book"
<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/67c99e6d-933b-4046-bbd4-ab48b1b334fe" />

3. Chain-of-Thought (CoT) Prompting (New Example)
Explanation: The model is encouraged to show intermediate reasoning steps to arrive at the solution for complex tasks.

- New Example:
Prompt:
"I have 3 boxes, and each box contains 5 red balls and 2 blue balls. If I add 1 blue ball to each box, how many blue balls do I have in total across all boxes? Let's think step by step."

- Expected AI Output (with CoT):
- Step 1: Initially, each box has 2 blue balls.
- Step 2: There are 3 boxes, so initially 2 blue balls/box * 3 boxes = 6 blue balls.
- Step 3: 1 blue ball is added to each of the 3 boxes, so 1 blue ball/box * 3 boxes = 3 blue balls added.
- Step 4: Total blue balls = Initial blue balls + Added blue balls = 6 + 3 = 9 blue balls.
- Answer: You have 9 blue balls in total."

<img width="1024" height="1024" alt="image" src="https://github.com/user-attachments/assets/2afe8827-9e80-4e9f-8c90-947f7cb9da23" />

# Detailed Analysis

1. Quality of Output

    - Naïve prompts produced responses that were generic, less organised, and often lacking vivid details.
    - Basic prompts resulted in well-structured, polished, and engaging content.

2. Accuracy of Information

   - Naïve prompts sometimes led to partially correct or incomplete facts.
   - Structured prompts guided the AI to focus on essential details, improving factual correctness.

3. Depth of Explanation

   - Naïve prompts typically gave surface-level answers.
   - Basic prompts encouraged the model to elaborate, provide context, and add supporting points.

4. Scenario-Specific Observations

   - Creative tasks: Even naïve prompts generated acceptable stories, but refining the prompt added coherence and richness.
   - Factual, summarisation, and advice tasks: Structured prompts significantly enhanced accuracy and completeness, proving the necessity of prompt engineering for knowledge intensive queries.


# Summary of Findings

1. Prompt clarity directly influences output quality.

2. Basic (structured) prompts consistently outperform naïve prompts across most scenarios.

3. For factual questions, summarisation, and advice, structured prompts ensure accuracy and completeness.

4. For creative tasks, naïve prompts can still produce interesting results, but structured prompts provide better narrative flow and richer details.

# Result

The experiment successfully demonstrated that structured prompt engineering improves the quality, accuracy, and depth of ChatGPT’s responses across diverse tasks.
While naïve prompts can work for highly creative tasks, well-designed basic prompts consistently deliver superior, reliable outputs and are recommended for all professional or academic applications.
