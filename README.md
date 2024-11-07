# Prompting_Test
해당 부분에서는 Prompting 요소, 기법 등을 배우고 실습하는 공간입니다.

**Prompting 구성 요소**: input, context, example
- input: 모델에게 응답을 요구하는 프로세스, 작업, 테스크 대상 포함
- context: 추가 정보 제공 / 모델 동작 방법, 특정 규칙 등 지정
- example: 예제를 포함하여 모델이 응답 패천을 식별하고 적용
  
- **효과적 프롬프트 4가지 요소** (Persona: 역할 설정 / role: 임무 부여, context: 맥락 설정, Format: 출력 포맷 설정)

**주요 파라미터** : temperature, top_p, top_k, max_tokens, freqeuncy_penalty
- temperature: 확률 분포에 가중치 변화를 주어 문장의 다양성을 조절 →  낮을수록 일관적이고 일반적인 답변, 높을수록 다양하고 창의적인 답변
- top_p : 선택 확률 값이 높은 토큰을 순서대로 나열한 후 , 설정한 누적 확률 값에 포함되지 않는 토큰을 제거할 때 사용하는 기준값  → 답변 생성 시 가능한 모든 토큰을 고려하는 대신, 누적 확률 값이 특정 임계값(top_p) 이하인 토큰 집합 내에서 무작위적으로 선택 (ex. top_p = 0.8 인 경우 누적 확률 값이 상위 80%에 포함된 토큰만 후보로 선택)
- top_k : 모델이 예측한 토큰의 선택 확률 분포에서 확률 값이 가장 높은 k개 중에서 하나를 선택할 때의 기준 값 (ex. top_k=5이면 가장 확률값이 높은 5개 의 토큰 중 하나의 토큰이 선택)
- max_tokens : 답변의 최대 길이 제한 (토큰 단위)
- frequency_penalty : 특정 단어 반복 억제 (높을수록 같은 결괏값을 반복적으로 생성할 확률이 감소)
![image](https://github.com/user-attachments/assets/1e03af03-7024-40e6-b449-d2a38198315c)

**프롬프트 원칙 5가지 카테고리**
- Principled Instructions Are All You Need for Questioning LLaMA-1/2, GPT-3.5/4 (https://arxiv.org/abs/2312.16171)
 √ 프롬프트의 구조와 명확성 (Prompt Structure and Clarity)
 √ 구체성과 정보 (Specificity and Information)
 √ 사용자 상호작용과 참여 (User Interaction and Engagement)
 √ 콘텐츠와 언어 스타일 (Content and Language Style)
 √ 복잡한 작업과 코딩 프롬프트 (Complex Tasks and Coding Prompts)
