Here is the content of the file converted into formatted Markdown.

Assignment: AI-Assisted Reproduction of Scientific Experiments 

Objective 

In this assignment, you will reverse-engineer a "Toy Experiment" from a recent computer vision research paper. Your goal is not just to write code, but to learn how to effectively collaborate with Large Language Models (LLMs) to accelerate research. You will assess where these tools succeed, where they hallucinate, and how to verify their output against scientific "ground truth".

The Target Paper 

* 
**Paper:** Just Image Transformers for Diffusion (Li et al., 2025) 


* 
**Focus Section:** 3.3 Toy Experiment 


* 
**Goal:** Reproduce Figure 2, which demonstrates the "Manifold Assumption" by comparing x-prediction, -prediction, and v-prediction across increasing dimensions ( to ).



The Task 

Phase 1: The "Clean Room" Extraction (Human Only) 

Before opening an AI tool, you must understand the experiment. Read Section 3.3 carefully. Identify and write down the specific experimental constraints:

* **Data:** What is the underlying geometry? How is it projected? 


* 
**Model:** What specific architecture (layers, hidden units) is used? 


* 
**Loss:** Which specific loss formulation is used for all predictions? 



Phase 2: AI Co-Pilot Implementation 

Use a generative AI tool (ChatGPT, Gemini, Claude, etc.) to write the Python code.

* 
**Iterative Coding:** It is unlikely the code will work perfectly on the first try. You will likely encounter syntax errors (e.g., shape mismatches) or semantic errors (e.g., using the wrong noise schedule).


* 
**The "Unit Test" Check:** Ask the LLM to write a small verification test for different components.



Phase 3: The "Turing Test" for Plots 

Run your code to generate the final visualization. Compare it side-by-side with Figure 2 in the paper.

* 
**Visual Fidelity:** Does your code replicate the catastrophic failure for -prediction at ? 


* 
**Pattern Matching:** Does the x-prediction remain stable even when the model is under-complete? 



The Report (Deliverables) 

Submit a PDF report containing the following three sections:

1. The Reproduction 

* Provide your reproduced version of Figure 2.


* Briefly explain if your results match/don't match the paper's claims.



2. The Failure Log (Critical Analysis) 

Document specific instances where the AI failed or struggled. Categorize them:

* **Syntax/Runtime Error:** Did it write invalid Python? (e.g., SyntaxError, tensor dimension mismatches) .


* 
**Hallucination:** Did it invent a library function that doesn't exist? Did it assume a variable was defined when it wasn't? 


* 
**Math/Logic Error:** Did it implement the equations correctly? 


* Any others... 



3. The Gap Analysis 

* Papers often omit tiny implementation details (e.g., learning rate, batch size, specific random seeds).


* Which hyperparameters were missing from the text? 


* What values did the AI choose for these "hidden" variables? Were those choices reasonable defaults or arbitrary guesses?
