# This is a repository of notebooks to explore Retrieval Augmented Generation (RAG) concepts with varying levels of complexities.
# It is a work in progress and will be updated regularly.

- Query analysis
    - text-to-cypher
    - text-to-SQL
    - Re-writing
    - text-to-metdat-filters

- Retrieval

- Re-writing the query
    - Multi-query: rewrite the user question with multiple (different) phrasings, retrieve infor for each questions, return unique documents for all queries
    - Decomposition: separate the question into several parts, answer each part sequentially or in parallel.
    - Step-back: ??
    - HyDE: ??

Key areas to master:
- Chunking strategies (size, overlap, metadata preservation)
- Vector DB selection (Pinecone vs Weaviate vs pgvector)
- Prompt engineering for both embedding and retrieval
- Reranking techniques for better relevance

Start with Langchain's RAG documentation - it's comprehensive and practical. Focus on understanding vector stores, chunking strategies, and embedding models.

Build progressively:
- Simple RAG with local PDFs first
- Add web scraping capabilities
- Experiment with different chunking methods
- Implement hybrid search (semantic + keyword)

Common pitfalls to watch for:
- Poor chunking leading to context loss
- Not handling duplicate content
- Slow retrieval at scale
- Token window limitations

The trickiest part is usually optimizing retrieval quality while maintaining speed. We solved this by implementing parallel processing and custom ranking algorithms.



- LangChain: LLM abstraction and support(though API Key), prmopt template, chains (of tasks in one workflow), indexes for RAG implementation, memory, agents. Prompt chaining.
- LangGraph: Build on top of LangChain to manage agents and their workflows, enables multi-agent workflows. Handles multiple agents. Graph(state, node, edges). Acyclical graph.
- LangFlow: No code builder. Built on top of LangChain. Good for prototyping; not so much for production. Similar tools: Relevance AI, Dify.
- Langsmith: Offers tools for logging, monitoring, and evaluation. Overkill for simple project. No Windows version of Langsmith Studio.

<!-- [Knowledge Augmented Generation](https://arxiv.org/abs/2409.13731) -->