# RAG Fusion

<img width="876" alt="image" src="https://github.com/AshishCodeCraft26/RAG-RAGFusion/assets/135592934/a6654ffe-5ae5-48e4-83e4-1a4abfc9830b">

<br>

RAG Fusion’s primary objectives is to bridge the gap between what users explicitly ask and what they intend to ask. 
By employing multiple query generation and RRF, it captures the nuances behind our queries, uncovering the transformative knowledge 
that often remains hidden beneath the surface of top search results. It helps mitigate bias in search results by diversifying the sources of information. 
This also helps to broaden the scope of information available and hence, enriches the user experience.

A single query cannot cover all the aspects of user queries, and it might be too narrow to provide comprehensive results; 
that’s why multiple query generation must consider all the different elements and provide a well-curated answer.

RRF works by combining the ranks of different search queries and increases the chances for all the relevant documents to appear in the final results.
Besides, it doesn’t rely on absolute scores assigned by search engines but rather on relative ranks, 
so combining results with different scales or distributions of scores becomes practical.

How it works?<br>
<img width="758" alt="image" src="https://github.com/AshishCodeCraft26/RAG-RAGFusion/assets/135592934/3da29b65-fabb-40e4-a4a6-ecf9d77d23ac">

<br>

The significance of RRF lies in its ability to produce a unified ranking that consistently yields better results than any single system. 
By combining ranks from different queries, RRF enhances the chances of the most relevant documents appearing at the top of the final list. 
What sets RRF apart is its reliance on relative ranks rather than absolute scores assigned by search engines. 
This makes it particularly well-suited for integrating results from queries with varying scales or distributions of scores.


A key feature of RRF is its simplicity in operation. The algorithm involves sorting documents based on a straightforward scoring formula, 
where the constant k plays a crucial role in mitigating the impact of outlier systems and ensuring the importance of lower-ranked documents is not overlooked.

As per the <a href="chrome-extension://oemmndcbldboiebfnladdacbdfmadadm/https://plg.uwaterloo.ca/~gvcormac/cormacksigir09-rrf.pdf">original paper</a>, given a set of documents (D) and rankings (R) representing permutations from 1 to the document count (|D|), 
RRF calculates the score for each document (d ∈ D) using the formula:

<img width="810" alt="image" src="https://github.com/AshishCodeCraft26/RAG-RAGFusion/assets/135592934/8c8cb25f-1947-4b98-a6b0-89883369fe02">

where k = 60 was established during an initial investigation and remained unchanged throughout subsequent validation processes.



