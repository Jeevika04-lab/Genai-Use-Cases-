--Table of Contents--
1.Overview Use Cases
2.Text Similarity & Paraphrase Detection
3.Language Translation
4.Medical Assistant Chatbot
5.Data Validation with Pydantic Installation Usage

--Overview--
This project demonstrates how to build and deploy various AI-powered tools using state-of-the-art pre-trained models and libraries: 
*SentenceTransformer for semantic textual similarity. 
*Google Translate API (via googletrans) for language translation. 
*BlenderBot model wrapped with LangChain for interactive medical assistant conversations. 
*Pydantic for robust data validation with error reporting. 
*Each use case highlights how to leverage AI and ML pipelines in Python for real-world applications.

--Use Cases--

1.Text Similarity & Paraphrase Detection
*Objective: Determine if two input sentences are paraphrases (i.e., semantically similar).
*Approach: Use the sentence-transformers model all-MiniLM-L6-v2 to generate sentence embeddings. Compute cosine similarity between sentence embeddings. Apply a threshold (0.8) to decide if sentences are paraphrases.
*Output: Similarity score and a decision if sentences are duplicates or different.

2.Language Translation 
*Objective: Translate an input English text into a supported target language. 
*Approach: Use the googletrans Python library to interface with Google Translate. Support major Indian languages such as Hindi, Bengali, Tamil, Kannada, Malayalam, Marathi, Punjabi, Urdu, Telugu, and English. 
*Output: Translated text printed in the chosen language.

3.Medical Assistant Chatbot 
*Objective: Provide a conversational medical assistant that offers advice without direct diagnosis.
*Approach: Use HuggingFace's facebook/blenderbot-400M-distill model for text generation. Wrap the model with LangChain to add conversational memory and prompt templating. Maintain chat history to provide context-aware responses.
*Usage: Interactive chat interface with the ability to exit by typing 'exit'.

4.Data Validation with Pydantic 
*Objective: Validate and clean structured data entries with automated error detection. 
*Approach: Define a Pydantic BaseModel (DataRecord) with typed fields. Add validators to enforce business rules (e.g., non-empty names, valid statuses). Parse raw data entries, separating valid records and errors. Output structured tables showing both clean data and validation issues.
*Output: Tables for valid records and detailed validation error reports.

--Installation--
The notebook installs required libraries automatically but to run locally, you can use:
bash 
Copy
Edit 
->pip install sentence-transformers scikit-learn googletrans==4.0.0-rc1 langchain langchain-huggingface transformers pydantic matplotlib pandas

--Usage--
Each section is self-contained and can be run interactively in the notebook:
Run the cells under each use case. 
Provide inputs when prompted (e.g., sentences for similarity, text and target language for translation). 
For the chatbot, interactively type queries and get responses. Review validation results in structured pandas DataFrames
