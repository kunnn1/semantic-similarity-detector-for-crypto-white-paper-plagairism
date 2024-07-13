# TokenConduct
My  project is a semantic similarity detector designed to identify and measure the similarity between different crypto white papers. The primary goal is to detect potential plagiarism and ensure the originality of academic and technical documents in the cryptocurrency domain, addressing the common fraud assoicated with white papers and fake ICOs. The detector uses natural language processing (NLP) techniques, specifically BERT embeddings, to calculate the semantic similarity between documents.
# Who Am I?
My name is Khasim Amedu and I am incoming freshman @ UIC and an aspiring AI/Machine Learning Engineer and Researcher. My Portfolio: https://kunnn1.github.io/
# Motivation
The inspiration behind my project goes back to a project in my senior year of high school in my AP Government class, where students were to submit bill propositions that address pertinent real-world issues and aim to get our proposed bills passed. While our bill ended up passing a unanimous vote, there was a particular bill proposed by a group of my classmates that I believed deserved to be passed, which was an act delineating the regulation of cryptocurrency under the principles of laissez-faire and our American economy to prevent cases of cryptocurrency scams amidst the alarming figures. Being aware of just how much a lack of regulation contributes to the rise of cryptocurrency scams, I wanted to create a project that could mitigate an infinitesimal part of the horizon of cryptocurrency fraud. Therefore, my project aims to provide a robust tool for detecting plagiarism in the rapidly growing field of cryptocurrency. With the increasing number of white papers being published, it is critical to have a reliable method to ensure the originality and authenticity of these documents.
# Appartus/Tech Used
Python
BERT (Bidirectional Encoder Representations from Transformers)
NLTK (Natural Language Toolkit)
Pandas
NumPy
Transformers (Hugging Face Library)
PyTorch
# Project Structure
main.py: The main script and logic to run the plagiarism detection.
preprocessing.py: Uses functions for text preprocessing.
model.py: Uses functions to generating BERT embeddings.
similarity.py: Contains functions for calculating similarity between embeddings.
whitepaper_database.py: Manages the database of white papers.
extract_text.py: Uses functions to extract text from files.
downloads.py: Handles downloading necessary resources or datasets.
requirements.txt: Lists all the dependencies required for you to use the project. 
# How the Plagairism Detector Actually (Basically) Works
The detector intitally extracts text from inputted .txt file converting them into plain text that can be proccessed and analyzed. The extracted text is then cleaned and standardized by removing punctuation and numbers, converting to lowercase, eliminating stopwords, tokenization and lemmatization. This new preprocessed text is "fed" into a pre-trained BERT model, which generates numerical representations or embeddings that capture the semantic meaning of the text (roughly). The detector then compares the BERT embeddings of the input white paper against those of other documents in the crypto white paper database authroed by Sergi Valverde and Salva Duran-Nebreda (you can find on figshare :D) using cosine similarity to measure the semantic similarity. The white paper documents with cosine similarity scores above a predefined threshold of 0.9 are flagged as potential plagiarism cases, indicating a high degree of semantic similarity with the input white paper document. The output result of the program generates a report listing all flagged white papers and their similarity scores so that you can go back and review your white paper with the flagged ones.
# Drawbacks/Limits
The semantic similarity detector is pretty intensive, requiring significant processing power and time, especially for large datasets, which limits scalability and convenience as a tool for users. The testing phase of this building this detector adduced struggle with sophisticated paraphrasing, cross-lingual plagiarism, and nuanced domain-specific content, potentially leading to false positives. Additionally, the effectiveness depends on setting appropriate similarity thresholds and may require frequent updates to stay relevant as language evolves. Otherwise, it's pretty decent. 
