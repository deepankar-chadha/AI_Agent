Deep Thought AI Agent Final Submission
SECTION 1: BASIC DETAILS
Name: Deepankar Chadha
AI Agent Title / Use Case: AI Agent to Suggest Daily Writing Prompts for Bloggers
SECTION 2: PROBLEM FRAMING
2.1 What problem does your AI Agent solve?
Bloggers often struggle with writer's block or need inspiration to maintain a daily writing habit. This agent helps generate relevant and creative writing prompts tailored to their interests, tone, or goals.
2.2 Why is this agent useful?
It helps bloggers stay consistent, improves creativity, and saves time brainstorming ideas — especially useful for content creators working under deadlines.
2.3 Who is the target user?
Independent bloggers, content writers, or creators who write regularly and want help with idea generation. Specifically helpful for bloggers focusing on lifestyle, self-development, tech, or niche content.
2.4 What not to include?
❌ No long blog outlines or full blog writing (focus only on prompt generation)
❌ No SEO optimization or keyword stuffing
❌ Avoid generic prompts — aim for personal, fresh, or thought-provoking suggestions
SECTION 3: 4-LAYER PROMPT DESIGN
3.1 INPUT UNDERSTANDING
Prompt:
You are an AI assistant that helps bloggers come up with daily writing prompts. First, extract and understand what the user is asking. Identify their desired theme, tone, or specific interests. If unclear, default to a general creative writing prompt.
Responsibility:
Helps the agent detect what kind of prompt the user wants (e.g., motivational, tech-related, nostalgic, etc.).
Example:
Input: 'I want something inspiring for Monday morning'
Extracted understanding: Theme = inspiration; Context = Monday/morning; Tone = positive
3.2 STATE TRACKER
Prompt:
Track and retain the user’s writing preferences (e.g., favorite themes, tone, topics they've used recently). Use this state to avoid repeating similar prompts. If this is the first interaction, create a blank preference profile.
Responsibility:
Simulates memory by tracking preferences like topic and tone across turns.
Memory:
Stored in a dictionary structure like: { 'themes': [...], 'tone': 'reflective' }
3.3 TASK PLANNER
Prompt:
Based on the extracted user input and saved preferences, follow these steps:
1. Choose a prompt theme based on user intent or past interest.
2. Add creative constraints (e.g., specific word, question-based, metaphor-driven).
3. Generate a single original writing prompt.
Responsibility:
Detects theme, adds variation, avoids repetition using chaining logic.
3.4 OUTPUT GENERATOR
Prompt:
Format the output as a clear writing prompt. Use markdown for structure (e.g., bold title, short intro). Keep the tone aligned with user preference. If no preference is set, keep it motivational and light. End with a reflective question to trigger writing.
Responsibility:
Structures output with formatting and tone control. Adds engagement.
SECTION 4: CHATGPT EXPLORATION LOG
Attempt #	Prompt Variant	What Happened	What You Changed	Why You Changed It
1	Initial prompt – ‘something for a rainy Sunday’	Correctly inferred tone; prompt was weather/mood specific	Added line to detect mood/environment	To improve emotional adaptation
2	Simulated user change in tone from ‘inspirational’ to ‘light-hearted’	Tracked change and used memory-like structure	Added max 5 prompts in history	Avoid memory overload
3	Request: ‘something fun and quirky’	Generated houseplants gossiping prompt	Added check to avoid repeat themes	Encourage novelty
SECTION 5: OUTPUT TESTS
Test: Normal input
Input: I want a journaling prompt about career confusion
Output:
**📝 Prompt: Fork in the Road**
“Write about a moment when you questioned your career path. What signs were you ignoring? What voices were you listening to?”
Test: Vague input
Input: Give me something to think about
Output:
** Prompt: The Thing You Always Avoid**
“What is one thought or question you’ve been avoiding lately? Write about why it lingers, and what it might say if it could speak.”
Test: Empty input
Input: 
Output:
**Prompt: Unwritten Moments**
“Describe a scene from a day in your life that you’ve never told anyone about. Why has it stayed unwritten until now?”
SECTION 6: REFLECTION
6.1 The hardest part was designing prompts that were modular and specific to their roles without overlapping.
6.2 I enjoyed testing how the AI responded to creative or abstract inputs.
6.3 I’d simulate evolving user profiles and allow users to set writing themes across days.
6.4 Prompt design is about logical decomposition, not scripting. Modular thinking matters.
6.5 Yes, especially with task planning. I asked ChatGPT meta-questions to debug and improve.
SECTION 7: HACK VALUE (Optional)
Yes — I added enhancements:
- Simulated memory logic via user_preferences
- Mood detection from environmental cues (e.g., ‘rainy Sunday’)
- Creative constraints like metaphor or narrative twists
