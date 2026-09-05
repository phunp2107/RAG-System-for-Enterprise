Project:
    AI Customer Support Platform

Problem:
    Customer support phải xử lý lượng lớn câu hỏi
    bằng cách tìm kiếm thủ công trong nhiều tài liệu.

Goal:
    Xây dựng AI platform hỗ trợ tự động trả lời câu hỏi
    dựa trên knowledge base nội bộ bằng RAG.

Users:
- Customer:
    Ask question
    View conversation
    Give feedback
- Agent:
    View customer conversations
    Use AI suggestion
    Search knowledge base
    Correct AI answer
- Admin:
    Manage users
    Upload documents
    Manage permissions
    View analytics
    Manage AI configuration

Use Cases:
    UC01 — Customer hỏi AI
        Customer
        ↓
        Send question
        ↓
        AI processes question
        ↓
        RAG retrieves documents
        ↓
        LLM generates answer
        ↓
        Return answer

    UC02 — Upload document
        Admin
        ↓
        Upload PDF
        ↓
        Document Service
        ↓
        Parse
        ↓
        Chunk
        ↓
        Embedding
        ↓
        Vector DB

        UC03 — Feedback
        Customer
        ↓
        👍 / 👎
        ↓
        Feedback Service
        ↓
        Evaluation Dataset

    UC04 — Agent review
        Customer question
                ↓
            AI answer
                ↓
            Agent
                ↓
        Approve / Edit

Security:
- OAuth2/JWT
- RBAC
- HTTPS
- Secret management
- Audit logging
- Document-level authorization

AI:
- RAG
- Hybrid search
- Reranking
- Citation
- Hallucination protection
- Evaluation pipeline

Infrastructure:
- Docker
- Kubernetes
- CI/CD
- Monitoring
- Automated backup