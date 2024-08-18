# Prompt Types

- Type of Prompts
    
    
    | Prompt Type | Description | Prompt Hack |
    | --- | --- | --- |
    | Chain of Thought (CoT) | LLM articulates its reasoning step-by-step while solving a problem.
    
    This approach, particularly effective in tasks involving arithmetic and complex reasoning, helps the model to structure its thoughts and often leads to more accurate answers. | Question 
    + 
    "Let’s think step by step" |
    | Thread-of-Thought (ThoT) | A type of Zero-Shot CoT, which uses an improved prompt. This prompt guides the model through a step-by-step analysis of the problem, similar to CoT but generally superior for complex, information-dense scenarios | Long, complicated context
     + 
    "Walk me through this context in manageable parts step by step, summarizing and analyzing as we go" |
    | Contrastive Chain-of-Thought (CCoT) | Adding an incorrect explanation to the CoT prompt alongside the correct reasoning.
    
     | Correct Example:
    +
    Incorrect Example:
    +
    Prompt |
    | Self-Ask (SA) | Generate and answer follow-up questions before arriving at a final answer |  |
    | Tabular Chain of Thought Prompting (Tab-CoT) | A tabular format, employing tables with specific column names like 
    "|step | question | response|" 
    to direct the model in generating a structured reasoning process |  |
    | Least-to-Most Prompting (LtM) | A technique where the LLM first decomposes a problem into smaller sub-problems, and then solves these sequentially to arrive at the final answer. | Prompt 
    +
    ”To find the solution, first decompose the problem into separate sequential sub-problems. Then, iteratively solve each and use it to answer the next.” |
    | Plan-and-Solve Prompting (PaS) | A technique enhances Zero-Shot CoT with a structured approach. First, the problem is understood, then a plan is formulated, and finally, the problem is solved step by step. | Prompt 
    +
    ”Let’s first understand the problem and devise a plan to solve it. Then, let’s carry out the plan and solve the problem step by step” |
    | Program-of-Thoughts Prompting (PoTh) | PoTh prompting involves having the model generate reasoning steps as code, and then this code is executed to obtain the final answer |  |
    | Self-Criticism | Empowers LLMs to emulate higher-order cognitive processes akin to human problem-solving and critical thinking. Enables LLMs to critically evaluate, refine, and verify their own outputs |  |
    | Self-Evaluation Prompting (SE) | An LLM first proposes an answer to a question, and then assesses the correctness of its own response.
    
    After generating an answer, the model is prompted to evaluate the probability that its answer is correct. |  |
    | Self-Refine Prompting (SR) | Self-Refine technique involves the LLM not only evaluating the validity of its output but also providing feedback for self-improvement and then implementing the suggested refinements. | Prompt 
    +
    ”After you've created the idea, critique it. Finally, use the critiques to refine the initial idea” |
    | Chain-of-Verification Prompting (COVE) | An innovative approach where the LLM first generates an answer, and then creates a list of verification questions to be fact-checked based on this answer. Each item on the list is then verified independently by the LLM. | Prompt
    +
    ”Please create a list of verification questions that could be used to guide a fact-checker on the previous response.” |
    | System 2 Attention Prompting (S2A) | This method involves refocusing the question on the most pertinent aspects, leading to more relevant and concise answers. | Prompt
    +
    ”Please restate this text, but only include information that is relevant to the question at hand” |
    | Rephrase and Respond Prompting (RaR) | This prompting strategy instructs the LLM to first rephrase and expand the question before generating the final answer. | Prompt
    +
    ”Given the question above, rephrase and expand it to better facilitate answering, ensuring all information from the original question is retained. After you've done so, combine the original question with the new, rephrased question. Then go ahead and answer this new question” |
    | Re-reading Prompting (RE2) | Enhances prompts by adding "Read the question again" and then copying & pasting in the question a second time within the same prompt  | Prompt
    +
    ”Read the question again”
    +
    Prompt |
-
