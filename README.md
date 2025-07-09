## 가족 대화 요약 GPT 파인튜닝 프로젝트

이 저장소는 OpenAI GPT-3.5-turbo 모델을 활용해 가족 간 카카오톡 대화 내용을 요약하는 모델을 파인튜닝한 프로젝트입니다.

### 주요 기능

- train.jsonl / test.jsonl 파일 업로드
- OpenAI API를 이용한 파인튜닝 실행
- 파인튜닝된 모델로 대화 요약 테스트
- 모델 상태 및 ID 확인 기능

### 사용 모델

- base model: gpt-3.5-turbo-0125
- fine-tuned model: ft:gpt-3.5-turbo-0125:personal:family-diary:{ID}

### 실행 방법

1. OpenAI Python 라이브러리 설치
    ```bash
    pip install openai
    ```

2. API 키 입력 후 실행
    ```python
    from openai import OpenAI
    client = OpenAI(api_key="YOUR_API_KEY")
    ```

3. train.jsonl, test.jsonl 파일 업로드 후 파인튜닝 실행

4. 모델 이름으로 테스트 메시지를 보내 요약 결과 확인

### 파일 구성

- `finetune.ipynb`: 전체 파인튜닝 및 테스트 코드
- `train.jsonl`: 학습 데이터
- `test.jsonl`: 검증 데이터
