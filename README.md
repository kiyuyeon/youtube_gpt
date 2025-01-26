# youtube_gpt
---
```
# 유튜브 오디오를 활용한 질문-응답 시스템 (LangChain 기반)

이 프로젝트는 유튜브 동영상에서 오디오를 추출하고, 이를 텍스트로 변환한 뒤, 문서를 처리하여 FAISS와 LangChain을 사용해 질문-응답(QA) 시스템을 생성합니다.

---


## 주요 기능
- 유튜브 동영상에서 오디오 다운로드
- OpenAI Whisper를 사용해 오디오를 텍스트로 변환
- 텍스트를 적절한 크기로 분할
- FAISS 벡터 스토어를 생성하여 문서 검색 지원
- LangChain의 `RetrievalQA`를 사용해 질문-응답 시스템 생성

---
## 설치 방법

1. 저장소 클론:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
   ```

2. 환경 변수 설정:
   - 프로젝트 루트 디렉토리에 `.env` 파일 생성
   - OpenAI API 키 추가:
     ```env
     OPENAI_API_KEY=your_openai_api_key
     ```

---

---

## 주요 라이브러리
- `langchain`
- `faiss-cpu`
- `openai`
- `python-dotenv`
- `yt-dlp`

---

## 프로젝트 주요 내용

- **오디오 처리:** 유튜브에서 오디오 추출 후 텍스트로 변환
- **텍스트 분할:** `RecursiveCharacterTextSplitter`를 사용하여 텍스트를 적절히 분할
- **벡터 스토어:** FAISS를 활용한 빠른 유사도 검색
- **질문-응답:** 사용자 질문에 대해 실시간 응답 스트리밍을 지원하는 `StreamCallback` 구현

---

## 향후 개선 사항
- LLama 등 오픈소스를 활용한 모델 파인튜닝을 통해 최적화된 성능 구현. 
- 프로젝트에 적합한 데이터를 수집, 전처리하여 특정 도메인에 특화된 커스텀 모델을 생성. 예를 들어, 유튜브 오디오 데이터 및 특정 산업 분야 데이터를 포함한 코퍼스를 구축하여 모델의 도메인 적합성을 높이는 방향으로 진행.  
- 사용자 친화적인 프론트엔드 통합

---
