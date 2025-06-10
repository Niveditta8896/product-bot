
## Customer Service Chatbot Evaluation

Project Overview
This project builds and evaluates a customer service chatbot that:

Answers user questions about products and categories.

Extracts relevant product info from user queries using LLM (like GPT-3.5).

Is evaluated for correctness and factual consistency.

✅ Progress Summary
1. Product Extraction Assistant
Implemented a function to extract product names and categories from customer queries.

Used few-shot prompting with examples to guide the model (find_category_and_product_v1()).

2. Built a Simple Chatbot UI
Used Panel for an interactive UI.

Users can type questions in a text input box and click a button to get LLM responses.

Conversations are stored in a global context and visualized using pn.Row() and pn.Column().

3. Tested with User Queries
Tested the chatbot with different user inputs.

Noted issues like duplicate responses, formatting errors (\n), and empty contexts.

Debugged and improved message handling and visual layout.

🔍 Evaluation Phase
A. Structured Extraction Accuracy
Created a development set (msg_ideal_pairs_set) with:

Customer queries

Ideal product/category pairs

Evaluated extraction accuracy using:

eval_response_with_ideal() → compares model's JSON output to ideal output.

B. Rubric-Based Evaluation
eval_with_rubric() compares assistant response with original context.

Evaluates via criteria like:

Did it use only provided context?

Did it answer all questions?

Was there any contradiction?

C. Expert Answer Comparison
eval_vs_ideal() compares LLM’s answer to an expert's.

Classifies answer into 5 categories (subset, superset, exact, disagreement, irrelevant).

🧠 Concepts Learned
Few-shot prompting

Contextual memory in chatbots

Structured output parsing

Evaluation via rubrics and expert answers

Debugging Panel layout, API response errors, and JSON formatting issues

🔧 Next Steps
Clean and modularize the code into functions and scripts.

Add logging and better error handling.

Add BLEU score / ROUGE / F1 as another evaluation metric.

Deploy a simplified version using Streamlit or Flask for demo.
