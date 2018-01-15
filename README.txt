Prerequisites to run this project:
1) Python Environment
2) Java IDE like Eclipse to import entire Lucene Folders as Java Projects


Steps for project execution:

NOTE: Execute each file in the exact order as mentioned below.
Execute python file by:
> python file_name.py

Only Lucene model is implemented in Java. To execute it, just import the entire project into Eclipse
> Run project as Java Application
1) Phase 1/Task 1/Step 4/Lucene/src/Lucene.java
2) Phase 1/Task 3/Part A/Step 4/Lucene (Stopped)/src/Lucene.java
3) Phase 1/Task 3/Part B/Step 3/Lucene (Stemmed)/src/Lucene.java


Execute each file in the exact order as mentioned below.
Input and output fields for every file has been mentioned for better understanding.
-----------------------------------------------------------------------------------------------------------------------------

PHASE 1:

TASK 1 Steps:

1. Execute Phase 1/Task 1/Step 1/tokenizer.py
I/P: Raw HTML dir
O/P: Phase 1/Task 1/Step 1/Tokenizer Output/

2. Execute Phase 1/Task 1/Step 2/create_inverted_list.py
	- I/P: Phase 1/Task 1/Step 1/Tokenizer Output/
	
	- O/P: Phase 1/Task 1/Setp 2/Inverted_List.txt
	- O/P: Phase 1/Task 1/Step 2/DocumentID_DocLen.txt
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Inverted_List.txt
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-DocumentID_DocLen.txt

3. Execute Phase 1/Task 1/Step 3/query_cleaning.py
	- I/P: Phase 1/Task 1/Step 3/cacm.query.txt
	- O/P: Phase 1/Task 1/Step 3/Cleaned_Queries.txt
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt

4. Execute the 4 algorithms of ranking (BM25, Lucene, TFIDF, Query Likelihood Model)

A.

a. Execute Phase 1/Task 1/Step 4/BM25/bm25_no_relevance.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Inverted_List.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-DocumentID_DocLen.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	
	- O/P: Phase 1/Task 1/Step 4/BM25/BM25_NonRelevance_Top5_Docs.txt
	- O/P: Phase 1/Task 1/Step 4/BM25/BM25_NonRelevance_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 1/Step 4/BM25/BM25_NonRelevance_Top100_Pages.txt
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25-NoRelevance-Top100Docs-perQuery/
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25_NoRelevance_Top5_Query_Pages.txt

b. Execute Phase 1/Task 1/Step 4/BM25/rel_doc.py
	- I/P: cacm.rel.txt
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-QueryID_RelevantDocs.txt

c. Execute Phase 1/Task 1/Step 4/BM25/bm25_relevance.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Inverted_List.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-DocumentID_DocLen.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-QueryID_RelevantDocs.txt
	
	- O/P: Phase 1/Task 1/Step 4/BM25/BM25_Relevance_Top5_Docs.txt
	- O/P: Phase 1/Task 1/Step 4/BM25/BM25_Relevance_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 1/Step 4/BM25/BM25_Relevance_Top100_Pages.txt
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25-Relevance-Top100Docs-perQuery/
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25-Relevance-Top5Docs-perQuery/
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25_Relevance_Top5_Query_Pages.txt

B. Executee Phase 1/Task 1/Step 4/TF-IDF/tf-idf_normalized.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Inverted_List.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-DocumentID_DocLen.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	
	- O/P: Phase 1/Task 1/Step 4/TF-IDF/TF_IDF_Normalized_Top5_Docs.txt
	- O/P: Phase 1/Task 1/Step 4/TF-IDF/TF_IDF_Normalized_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 1/Step 4/TF-IDF/TF_IDF_Normalized_Top100_Pages.txt
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-TF-IDF-Normalized-Top100Docs-perQuery/
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-TF_IDF_Normalized_Top5_Query_Pages.txt

C. Executee Phase 1/Task 1/Step 4/QLM/QLM.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Inverted_List.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-DocumentID_DocLen.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	
	- O/P: Phase 1/Task 1/Step 4/QLM/QLM_Top5_Docs.txt
	- O/P: Phase 1/Task 1/Step 4/QLM/QLM_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 1/Step 4/QLM/QLM_Top100_Pages.txt
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-QLM-Top100Docs-perQuery/
	- O/P: Phase 1/Task 1/Encoded Data Structures/Encoded-QLM_Top5_Query_Pages.txt

D. Execute Phase 1/Task 1/Step 4/Lucene/src/Lucene.java

Task 2 Steps:

1. Execute generate_QueryID_Top5Docs_Dictionary.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25-Relevance-Top5Docs-perQuery/
	- O/P: Phase 1/Task 2/Encoded Data Structures (PRF)/Encoded-QueryID_Top5Docs_BM25_Relevance.txt

2. Execute creating_inv_list_for_top_5.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- I/P: Phase 1/Task 2/common_words.txt
	- I/P: Phase 1/Task 2/Encoded Data Structures (PRF)/Encoded-QueryID_Top5Docs_BM25_Relevance.txt
	- I/P: Phase 1/Task 1/Step 1/Tokenizer Output/
	- O/P: Phase 1/Task 2/Encoded Data Structures (PRF)/Encoded-Queries_With_Their_Expansion_Terms.txt

3. Execute create_expanded_queries.py
	- I/P: Phase 1/Task 2/Encoded Data Structures (PRF)/Encoded-Queries_With_Their_Expansion_Terms.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-QueryID_RelevantDocs.txt
	- O/P: Phase 1/Task 2/Encoded Data Structures (PRF)/Encoded-Expanded_Queries.txt

4. Execute bm25_Relevance_PRF.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Inverted_List.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-DocumentID_DocLen.txt
	- I/P: Phase 1/Task 2/Encoded Data Structures (PRF)/Encoded-Expanded_Queries.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-QueryID_RelevantDocs.txt
	- I/P: Phase 1/Task 1/Step 1/Tokenizer Output/
	
	- O/P: Phase 1/Task 2/Step 4/BM25_Relevance_PRF_Top100_Pages.txt
	- O/P: Phase 1/Task 2/Encoded Data Structures (PRF)/Encoded-BM25-Relevance-PRF-Top100Docs-perQuery/

TASK 3 Steps:

Part A (Stopping):

Steps:
1. Exectute Phase 1/Task 3/Part A/Step 1/tokenizer_with_stopping.py
	- I/P: Raw HTML dir
	- I/P: Phase 1/Task 3/Part A/common_words.txt
	- O/P: Phase 1/Task 3/Part A/Step 1/Stopped Tokenizer Output/

2. Execute Phase 1/Task 3/Step 2/create_stopped_inverted_list.py
	- I/P: Phase 1/Task 3/Part A/Step 1/Stopped Tokenizer Output/
	
	- O/P: Phase 1/Task 3/Part A/Step 2/Stopped_Inverted_List.txt
	- O/P: Phase 1/Task 3/Part A/Step 2/Stopped_DocumentID_DocLen.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_Inverted_List.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_DocumentID_DocLen.txt

3. Execute Phase 1/Task 3/Step 3/query_cleaning_stopwords_removed.py
	- I/P: Phase 1/Task 3/Part A/common_words.txt
	- I/P: Phase 1/Task 3/Part A/Step 3/cacm.query.txt
	
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Cleaned_Queries_Stopped.txt
	- O/P: Phase 1/Task 3/Part A/Step 3/Cleaned_Queries_Stopped.txt

4.

Part A (BM25 (Stopped))
1. Execute Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/bm25_no_relevance_stopping.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_Inverted_List.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_DocumentID_DocLen.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Cleaned_Queries_Stopped.txt
	
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/Stopped_BM25_NoRelevance_Top5_Docs.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/Stopped_BM25_NoRelevance_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/Stopped_BM25_NoRelevance_Top100_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_BM25-NoRelevance-Top100Docs-perQuery/
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_BM25_NoRelevance_Top5_Query_Pages.txt

2. Execute Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/rel-doc-stopped.py
	- I/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/cacm.rel.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_QueryID_RelevantDocs.txt

3. Execute Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/bm25_relevance_stopping.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_Inverted_List.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_DocumentID_DocLen.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Cleaned_Queries_Stopped.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_QueryID_RelevantDocs.txt
	- I/P: Phase 1/Task 3/Part A/Step 1/Stopped Tokenizer Output/

	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/Stopped_BM25_Relevance_Top5_Docs.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/Stopped_BM25_Relevance_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/Stopped_BM25_Relevance_Top100_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_BM25-Relevance-Top100Docs-perQuery/
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_BM25_Relevance_Top5_Query_Pages.txt

Part B (QLM (Stopped))
Execute Phase 1/Task 3/Part A/Step 4/QLM (Stopped)/qlm_stopping.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_Inverted_List.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_DocumentID_DocLen.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Cleaned_Queries_Stopped.txt
	
	- O/P: Phase 1/Task 3/Part A/Step 4/QLM (Stopped)/Stopped_QLM_Top5_Docs.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/QLM (Stopped)/Stopped_QLM_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/QLM (Stopped)/Stopped_QLM_Top100_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_QLM-Top100Docs-perQuery/
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_QLM_Top5_Query_Pages.txt

Part C (TF-IDF (Stopped))
Execute Phase 1/Task 3/Part A/Step 4/TF-IDF (Stopped)/tf-idf_normalized_stopping.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_Inverted_List.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_DocumentID_DocLen.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Cleaned_Queries_Stopped.txt
	
	- O/P: Phase 1/Task 3/Part A/Step 4/TF-IDF (Stopped)/Stopped_TF-IDF_Normalized_Top5_Docs.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/TF-IDF (Stopped)/Stopped_TF-IDF_Normalized_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/TF-IDF (Stopped)/Stopped_TF-IDF_Normalized_Top100_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_TF-IDF-Normalized-Top100Docs-perQuery/
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_TF-IDF_Normalized_Top5_Query_Pages.txt

Part D (Lucene)
Execute Phase 1/Task 3/Part A/Step 4/Lucene (Stopped)/src/Lucene.java


Task 3 Part B (Stemming):

Steps:
1. Execute Phase 1/Task 3/Part B/Step 1/cacm_stem_extracter.py
	- I/P: Phase 1/Task 3/Part B/Step 1/cacm_stem.txt
	- O/P: Phase 1/Task 3/Part B/Step 1/Stemmed_Corpus/

2. Execute Phase 1/Task 3/Part B/Step 2/create_stemmed_inverted_list.py
	- I/P: Phase 1/Task 3/Part B/Step 1/Stemmed_Corpus/
	- O/P: Phase 1/Task 3/Part B/Step 2/Stemmed_Inverted_List.txt
	- O/P: Phase 1/Task 3/Part B/Step 2/Stemmed_DocumentID_DocLen.txt
	- O/P: Phase 1/Task 3/Part B/Encoded Data Structures (Stemmed)/Encoded-Stemmed_Inverted_List.txt
	- O/P: Phase 1/Task 3/Part B/Encoded Data Structures (Stemmed)/Encoded-Stemmed_DocumentID_DocLen.txt

3. (BM25 (Stemmed))
1. Execute Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/bm25_no_relevance_stemming.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_Inverted_List.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_DocumentID_DocLen.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Cleaned_Queries_Stemmed.txt
	
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/Stemmed_BM25_NoRelevance_Top5_Docs.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/Stemmed_BM25_NoRelevance_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/Stemmed_BM25_NoRelevance_Top100_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_BM25-NoRelevance-Top100Docs-perQuery/
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_BM25_NoRelevance_Top5_Query_Pages.txt

2. Execute Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/rel-doc-stemmed.py
	- I/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/cacm.rel.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_QueryID_RelevantDocs.txt

3. Execute Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/bm25_relevance_stemming.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_Inverted_List.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_DocumentID_DocLen.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Cleaned_Queries_Stemmed.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_QueryID_RelevantDocs.txt
	- I/P: Phase 1/Task 3/Part A/Step 1/Stemmed Tokenizer Output/

	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/Stemmed_BM25_Relevance_Top5_Docs.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/Stemmed_BM25_Relevance_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stemmed)/Stemmed_BM25_Relevance_Top100_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_BM25-Relevance-Top100Docs-perQuery/
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_BM25_Relevance_Top5_Query_Pages.txt

Part B (QLM (Stemmed))
Execute Phase 1/Task 3/Part A/Step 4/QLM (Stemmed)/qlm_stemming.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_Inverted_List.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_DocumentID_DocLen.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Cleaned_Queries_Stemmed.txt
	
	- O/P: Phase 1/Task 3/Part A/Step 4/QLM (Stemmed)/Stemmed_QLM_Top5_Docs.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/QLM (Stemmed)/Stemmed_QLM_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/QLM (Stemmed)/Stemmed_QLM_Top100_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_QLM-Top100Docs-perQuery/
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_QLM_Top5_Query_Pages.txt

Part C (TF-IDF (Stemmed))
Execute Phase 1/Task 3/Part A/Step 4/TF-IDF (Stemmed)/tf-idf_normalized_stemming.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_Inverted_List.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_DocumentID_DocLen.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Cleaned_Queries_Stemmed.txt
	
	- O/P: Phase 1/Task 3/Part A/Step 4/TF-IDF (Stemmed)/Stemmed_TF-IDF_Normalized_Top5_Docs.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/TF-IDF (Stemmed)/Stemmed_TF-IDF_Normalized_Top5_Query_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Step 4/TF-IDF (Stemmed)/Stemmed_TF-IDF_Normalized_Top100_Pages.txt
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_TF-IDF-Normalized-Top100Docs-perQuery/
	- O/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stemmed)/Encoded-Stemmed_TF-IDF_Normalized_Top5_Query_Pages.txt

Part D (Lucene)
Execute Phase 1/Task 3/Part A/Step 4/Lucene (Stemmed)/src/Lucene.java

-----------------------------------------------------------------------------------------------------------------------------


PHASE 2:

Exectute Phase 2/Snippet_generation.py
	- I/P: Raw HTML dir
	- I/P: Phase 2/common_word.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_Inverted_List.txt
	- I/P: Phase 1/Task 3/Part A/Step 4/Lucene (Stopped)/Stopped_Lucene_Top5_Docs.txt
	- I/P: Phase 1/Task 3/Part A/Step 4/BM25 (Stopped)/Stopped_BM25_NoRelevance_Top5_Docs.txt
	- I/P: Phase 1/Task 3/Part A/Step 4/QLM (Stopped)/Stopped_QLM_Top5_Docs.txt
	- I/P: Phase 1/Task 3/Part A/Step 4/TF-IDF (Stopped)/Stopped_TF_IDF_Normalized_Top5_Docs.txt
	
	- O/P: Phase 2/Snippets_Text/Snippets_Stopped_Lucene.txt
	- O/P: Phase 2/Snippets_Text/Snippets_Stopped_BM25_NoRelevance.txt
	- O/P: Phase 2/Snippets_Text/Snippets_Stopped_QLM.txt
	- O/P: Phase 2/Snippets_Text/Snippets_Stopped_TF_IDF_Normalized.txt
	- O/P: Phase 2/Snippets_HTML/Snippets_Stopped_Lucene.html
	- O/P: Phase 2/Snippets_HTML/Snippets_Stopped_BM25_NoRelevance.html
	- O/P: Phase 2/Snippets_HTML/Snippets_Stopped_QLM.html
	- O/P: Phase 2/Snippets_HTML/Snippets_Stopped_TF_IDF_Normalized.html


-----------------------------------------------------------------------------------------------------------------------------


PHASE 3:

Steps:

1. Part A 
Execute Phase 3/Step 1/BM25 (No Relevance)/generate_QueryID_Top100Docs_bm25_no_relevance.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25-NoRelevance-Top100Docs-perQuery/
	- O/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_BM25_NoRelevance.txt

1. Part B
Execute Phase 3/Step 1/BM25 (Relevance)/generate_QueryID_Top100Docs_bm25_relevance.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25-Relevance-Top100Docs-perQuery/
	- O/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_BM25_Relevance.txt

1. Part C
Execute Phase 3/Step 1/Lucene/generate_QueryID_Top100Docs_lucene.py
	- I/P: Phase 1/Task 1/Step 4/Lucene/Lucene_Top100_Docs.txt
	- O/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_Lucene.txt

1. Part D
Execute Phase 3/Step 1/QLM/generate_QueryID_Top100Docs_QLM.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-QLM-Top100Docs-perQuery/
	- O/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_QLM.txt

1. Part E
Execute Phase 3/Step 1/TF-IDF/generate_QueryID_Top100Docs_tf-idf_normalized.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-TF-IDF-Normalized-Top100Docs-perQuery/
	- O/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_tf-idf_normalized.txt

1. Part F
Execute Phase 3/Step 1/BM25 (Relevance with PRF)/generate_QueryID_Top100Docs_bm25_relevance_PRF.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25-Relevance-PRF-Top100Docs-perQuery/
	- O/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_BM25_Relevance_PRF.txt

1. Part G
Execute Phase 3/Step 1/BM25 (Relevance Stopped)/generate_QueryID_Top100Docs_bm25_relevance_stopped.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_BM25-Relevance-Top100Docs-perQuery
	- O/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_Stopped_BM25_Relevance.txt

1. Part H
Execute Phase 3/Step 1/Lucene (Stopped)/generate_QueryID_Top100Docs_lucene_stopped.py
	- I/P: Phase 1/Task 3/Part A/Step 4/Lucene (Stopped)/Stopped_Lucene_Top100_Docs.txt
	- O/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_Stopped_Lucene.txt

1. Part I
Execute Phase 3/Step 1/TF-IDF (Stopped)/generate_QueryID_Top100Docs_tf-idf_normalized_stopped.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_TF-IDF-Normalized-Top100Docs-perQuery
	- O/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_Stopped_tf-idf_normalized.txt



2. Part A 
Execute Phase 3/Step 2/BM25 (No Relevance)/retrieval_model_evaluation_bm25_no_relevance.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-QueryID_RelevantDocs.txt
	- I/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_BM25_NoRelevance.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- O/P: Phase 3/Precision Recall Tables/BM25 Evaluation Results/BM25 (No Relevance)/

2. Part B
Execute Phase 3/Step 2/BM25 (Relevance)/retrieval_model_evaluation_bm25_relevance.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25-Relevance-Top100Docs-perQuery/
	- I/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_BM25_Relevance.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- O/P: Phase 3/Precision Recall Tables/BM25 Evaluation Results/BM25 (Relevance)/

2. Part C
Execute Phase 3/Step 2/Lucene/retrieval_model_evaluation_lucene.py
	- I/P: Phase 1/Task 1/Step 4/Lucene/Lucene_Top100_Docs.txt
	- I/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_Lucene.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- O/P: Phase 3/Precision Recall Tables/Lucene Evaluation Results/Lucene/

2. Part D
Execute Phase 3/Step 2/QLM/retrieval_model_evaluation_QLM.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-QLM-Top100Docs-perQuery/
	- I/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_QLM.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- O/P: Phase 3/Precision Recall Tables/QLM Evaluation Results/QLM/

2. Part E
Execute Phase 3/Step 2/TF-IDF/retrieval_model_evaluation_tf-idf_normalized.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-TF-IDF-Normalized-Top100Docs-perQuery/
	- I/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_tf-idf_normalized.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- O/P: Phase 3/Precision Recall Tables/TF-IDF Evaluation Results/TF-IDF/

2. Part F
Execute Phase 3/Step 1/BM25 (Relevance with PRF)/retrieval_model_evaluation_by_bm25_with_relevance_for_PRM_s_top_100.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-BM25-Relevance-Top100Docs-perQuery/
	- I/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_BM25_Relevance_PRF.txt
	- I/P: Phase 1/Task 2/Encoded-Expanded_Queries.txt
	- O/P: Phase 3/Precision Recall Tables/BM25 (Relevance with PRF)/

2. Part G
Execute Phase 3/Step 1/BM25 (Relevance Stopped)/retrieval_model_evaluation_relevance_stopped.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_BM25-Relevance-Top100Docs-perQuery/
	- I/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_Stopped_BM25_Relevance.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Cleaned_Queries_Stopped.txt
	- O/P: Phase 3/Precision Recall Tables/BM25 (Relevance Stopped)/

2. Part H
Execute Phase 3/Step 1/Lucene (Stopped)/retrieval_model_evaluation_lucene_stopped.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_QueryID_RelevantDocs.txt
	- I/P: Phase 3/Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_Stopped_Lucene.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Cleaned_Queries_Stopped.txt
	- O/P: Phase 3/Precision Recall Tables/Lucene (Stopped)/

2. Part I
Execute Phase 3/Step 1/TF-IDF (Stopped)/retrieval_model_evaluation_tf-idf_normalized_stopped.py
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Stopped_QueryID_RelevantDocs.txt
	- I/P: Encoded Data Structures (Phase 3)/Encoded-QueryID_Top100Docs_Stopped_tf-idf_normalized.txt
	- I/P: Phase 1/Task 3/Part A/Encoded Data Structures (Stopped)/Encoded-Cleaned_Queries_Stopped.txt
	- O/P: Phase 3/Precision Recall Tables/TF-IDF-Normalized (Stopped)/


-----------------------------------------------------------------------------------------------------------------------------


Supplementary Features:

Part A (No Stopping):

Execute Supplementary Features/Part A (No Stopping)/create_inverted_list_with_positions_no_stop.py
	- I/P: Phase 1/Task 1/Step 1/Tokenizer Output
	- O/P: Supplementary Features/Inverted_List_With_Positions_No_Stopping.txt
	- O/P: Supplementary Features/Encoded Data Structures (Bonus)/Encoded-Inverted_List_Position_No_Stopping.txt

Execute Supplementary Features/Part A (No Stopping)/proximity_no_stop.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-DocumentID_DocLen.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- I/P: Supplementary Features/Encoded Data Structures (Bonus)/Encoded-Inverted_List_Position_No_Stopping.txt
	- O/P: Supplementary Features/Encoded Data Structures (Bonus)/Encoded-Top100-Docs-Proximity-NoStopping/
	- O/P: Supplementary Features/Part A (No Stopping)/Proximity_NoStopping_Top100_Pages.txt

Part B (Stopping):

Execute Supplementary Features/Part B (Stopping)/create_inverted_list_with_positions_stop.py
	- I/P: Phase 1/Task 3/Part A/Step 1/Stopped Tokenizer Output
	- I/P: Phase 1/Task 3/Part A/common_words.txt
	- O/P: Supplementary Features/Inverted_List_With_Positions_Stopping.txt
	- O/P: Supplementary Features/Encoded Data Structures (Bonus)/Encoded-Inverted_List_Position_With_Stopping.txt

Execute Supplementary Features/Part B (Stopping)/proximity_with_stop.py
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-DocumentID_DocLen.txt
	- I/P: Phase 1/Task 1/Encoded Data Structures/Encoded-Cleaned_Queries.txt
	- I/P: Supplementary Features/Encoded Data Structures (Bonus)/Encoded-Inverted_List_Position_With_Stopping.txt
	- O/P: Supplementary Features/Encoded Data Structures (Bonus)/Encoded-Top100-Docs-Proximity-With-Stopping/
	- O/P: Supplementary Features/Part B (Stopping)/Proximity_With_Stopping_Top100_Pages.txt