# 7주차 - 대화형 RAG Chatbot

## 1. 실습 목표

이번 실습에서는 6주차의 Basic RAG를 확장하여  
**이전 대화를 반영할 수 있는 대화형 RAG Chatbot**을 구현합니다.

주요 목표는 다음과 같습니다.

- 로컬 LLM 실행 환경 이해
- Ollama와 Gemma 연결
- PDF 문서 검색
- Chroma Vector DB 활용
- Basic RAG 구현
- 이전 대화를 반영하는 대화형 RAG 구현
- Streamlit 기반 Chat UI 구현

---

## 3.폴더 구조

```text
STEP 1
Ollama 연결 확인
↓
STEP 2
관련 문서 검색
↓
STEP 3
Basic RAG 답변 생성
↓
STEP 4
대화형 RAG 구현
↓
STEP 5
Streamlit Chat UI 구현


## 2. 전체 실습 흐름
C:\2026-open
├─ 6w
│  └─ data
│     ├─ 공지1.pdf
│     ├─ 공지2.pdf
│     └─ ...
│
└─ 7w
   ├─ .venv
   ├─ step1_ollama.py
   ├─ step2_retrieval.py
   ├─ step3_basic_rag.py
   ├─ step4_chat_rag.py
   ├─ app.py
   └─ requirements.txt
- step1_ollama.pyPython에서 Ollama의 gemma3:4b를 호출해 **LLM 연결만 확인**
- step2_retrieval.py6w/data의 공지 PDF를 읽어서 **Chunking → Embedding → Chroma → Retrieval**까지 구현
- step3_basic_rag.pyRetrieval 결과를 Ollama에 넘겨 **Basic RAG 답변 생성**
- step4_chat_rag.py이전 대화를 저장하고 **후속 질문이 가능한 대화형 RAG** 구현
- app.py 또는 step5_streamlit.pyStreamlit을 붙여 **브라우저에서 사용하는 RAG Chatbot** 완성


## 4. 사용 도구
도구	역할
Python 3.12	실습 코드 실행
VS Code	코드 작성 및 실행
Ollama	로컬 LLM 실행
Gemma 3 4B	답변을 생성하는 AI 모델
LangChain	RAG 처리 과정 연결
Chroma	Vector DB 및 문서 검색
sentence-transformers	문장 Embedding
PyPDF	PDF 문서 읽기
Streamlit	웹 기반 Chat UI
torch / torchvision	AI 라이브러리 실행 지원


