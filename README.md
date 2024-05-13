# Travel Mode and Sentiment Analysis Using LLMs

## Summary
This repository contains the final code and associated documents for a project focused on analyzing travel data from Twitter using Large Language Models (LLMs). The primary goal is to extract travel modes, sentiments, and reasons behind these sentiments from tweets. The code of final experiment is Step 1:LLM_extraction.ipynb, Step 2:LLM_verification.ipynb and Step 3:LLM_output_analysis.ipynb. The code for the experiments is available in the code_experiment folder.

## Methodology
The methodology employed leverages various LLMs, specifically GPT-3.5-turbo, to analyze unlabelled travel data from Twitter. The process is structured into three main steps:

### Step 1: Extraction
The initial extraction phase utilizes GPT-3.5-turbo to determine travel modes mentioned in tweets based on three key questions:

**What is the corresponding travel mode in this tweet? (Possible answers: Irrelevant (NA), subway, bus, bike, taxi, car)**
**What is the user sentiment regarding the travel mode's service? (Possible answers: positive, negative, neutral)**
**If related to a specific travel mode, what are the reasons for the sentiment expressed?**
The process integrates chain-of-thought reasoning to systematically structure the model’s output, followed by in-context learning with demonstrations for precise and relevant outputs. Prompts are designed to elicit close-ended responses in a JSON format with lowercase outputs.

### Step 2: Verification and Refinement
The extracted data is subjected to a three-part verification process:

**Self-Verification: Conducted by GPT-3.5-turbo to ensure accuracy and consistency.**
**Cross-Verification: Performed by GPT-4-turbo and LLAMA-2-7b to provide a broader evaluation scope.**
**Human Verification: Outputs are reviewed by humans to confirm contextual and factual accuracy.**
Feedback from these verification steps informs the refinement of the prompts used in Step 1. This iterative process continues until the outputs meet desired accuracy and relevance standards.

### Step 3: Output Analysis
The final step involves analyzing the verified data to explore travel modes and sentiments expressed in tweets. This includes comparing results from different prompt styles and approaches to identify the most effective methods in extracting and understanding travel patterns and user sentiments. Metrics and visualizations aid in demonstrating how travel preferences and public sentiment towards various transportation modes are articulated on social media.

## Further Development
Further improvements will focus on deploying additional LLMs for cross-verification to mitigate bias and enhance the reliability and generalizability of findings. This continuous development aims to refine the robustness and applicability of the methodology in real-world scenarios.
