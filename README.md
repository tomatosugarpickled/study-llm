# study-llm

국비 과정에서 LLM, LangChain, LCEL, 멀티모달, RAG를 학습하며 정리한 실습 저장소입니다.

단순히 API 호출 예제를 모으기보다, 이후 GlobalGates AI 프로젝트에 적용할 수 있는 기능을 중심으로 실습 내용을 정리했습니다. 이 저장소는 완성형 서비스가 아니라 LLM 기능을 이해하고 실험한 학습 기록입니다.

## GlobalGates AI 포트폴리오 흐름

이 저장소는 GlobalGates AI 포트폴리오 중 **학습 단계**에 해당합니다.

1. `study-llm`: LLM, LangChain, RAG를 학습하며 정리한 실습 저장소
2. `globalgates-ai-project`: GlobalGates 서비스에 적용할 AI 기능을 노트북으로 실험한 저장소
3. `globalgates-ai-backend`: 실험한 기능을 FastAPI 기반 API 서버로 구현한 저장소

## 학습 범위

- OpenAI API와 LangChain 기본 호출
- 스트리밍, 토큰 사용량 확인, 캐시 실습
- LCEL 기반 체인 구성
- Pydantic/JSON output parser
- 멀티모달 입력 처리
- 이미지 생성 API 실습
- FAISS 기반 RAG
- Redis semantic cache
- RAGAnything/docling 기반 문서 처리 실습

## 실습 목록

| 파일 | 내용 |
| --- | --- |
| `a_LLM.ipynb` | LLM 기본 호출, 스트리밍, 캐시, Redis cache |
| `b_multimodal.ipynb` | 이미지 입력을 포함한 멀티모달 모델 실습 |
| `c_LCEL.ipynb` | LangChain Expression Language 체인 구성 |
| `d_image_generator.ipynb` | 이미지 생성 API와 프롬프트 구성 |
| `e_RAG.ipynb` | PDF 로딩, chunking, FAISS 기반 RAG |
| `e_RAG-2.ipynb` | Redis semantic cache, RAGAnything, docling 실습 |
| `인공지능_플랫폼_인터페이스_구현.ipynb` | 프롬프트, parser, 체인 구성 기초 |

## 프로젝트 적용으로 이어진 부분

이 저장소에서 실습한 RAG, LCEL, Redis cache, 문서 처리 흐름은 이후 `globalgates-ai-project`와 `globalgates-ai-backend`에서 무역 문서 질의응답 기능으로 이어졌습니다.

특히 PDF 문서를 chunk로 나누고, 임베딩 후 검색 결과를 LLM 답변에 연결하는 흐름을 먼저 실습한 뒤 GlobalGates 도메인 문서에 적용했습니다.

## 실행 환경

```powershell
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
```

RAGAnything/docling 실습은 별도 패키지 조합을 사용했습니다.

```powershell
pip install -r requirements-raganything.txt
```

## 공개 저장소에서 제외한 항목

- API 키와 `.env`
- 가상환경과 Hugging Face 캐시
- 수업용 PDF 원문
- RAG 저장소와 생성 산출물
- 이미지 생성 결과물

필요한 환경 변수는 `.env.example`에 예시로만 정리했습니다.

## 관련 저장소

- `globalgates-ai-project`: 학습한 내용을 GlobalGates 서비스 문제에 적용한 노트북 실험
- `globalgates-ai-backend`: 실험한 기능을 FastAPI API 서버로 구현한 저장소

