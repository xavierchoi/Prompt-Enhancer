# Claude Code를 위해 작성된 Prompt Enhancer 가이드



**"단 한 줄의 요청을 완벽한 개발 계획으로 변환하는 방법"**

이 문서는 개발자가 AI 언어 모델(LLM)에게 보내는 단순하고 모호한 요청을, 자동으로 분석하고 프로젝트의 맥락과 숨은 요구사항을 더해, 완전하고 실행 가능한 **고품질 개발 지침으로 변환**하는 시스템의 설계 가이드입니다.

---
다운로드: [PROMPT_ENHANCER.md](https://github.com/user-attachments/files/20786025/PROMPT_ENHANCER.md)
---

## 🎯 목적

개발자는 종종 AI 모델에게 다음과 같이 간단하게 요청합니다.
- "이 코드 고쳐줘"
- "검색 기능 추가해 줘"
- "로그인 만들어 줘"

이러한 요청은 AI 모델이 작업을 수행하기엔 제공받은 정보가 부족하여 비효율적인 결과나 의도와 다른 코드를 생성하게 만듭니다. `Prompt Enhancer`는 이 간극을 메우기 위해 작성되었습니다. `Prompt Enhancer`는 사용자의 단순한 의도를 **구체적이고, 체계적이며, 품질 기준까지 포함된 명세서**로 자동 변환하여 개발 생산성을 극대화하는 것을 목표로 합니다.

## ✨ 주요 특징

`PROMPT_ENHANCER.md`에 정의된 시스템은 다음과 같은 강력한 특징을 가집니다.

1.  **체계적인 강화 프로세스 (Enhancement Process)**
    - **`분석 → 컨텍스트 수집 → 요구사항 발견 → 프롬프트 생성`**의 4단계 프로세스를 통해 요청을 체계적으로 구체화합니다.

2.  **지능적인 변환 패턴 (Transformation Rules)**
    - **모호한 요청을 구체적으로:** "코드 수정" → "어떤 파일의 성능을 어떻게 개선할지" 명시
    - **단순 요청을 상세 계획으로:** "기능 추가" → UI, 로직, 상태 관리, 테스트를 포함한 단계별 계획 수립
    - **요청을 완전한 워크플로로:** "로그인 기능" → 백엔드, 프론트엔드, 보안, 테스트를 아우르는 전체 개발 단계 제안

3.  **프로젝트 컨텍스트 자동 통합 (Context Utilization)**
    - **기존 코드 패턴 분석:** 코드 스타일, 에러 처리, 명명 규칙 등을 파악하여 일관성을 유지합니다.
    - **의존성 고려:** `package.json`을 분석하여 기존 라이브러리를 최대한 활용하고 불필요한 의존성 추가를 방지합니다.
    - **아키텍처 일관성:** 폴더 구조와 데이터 흐름을 파악하여 새로운 코드를 올바른 위치에 배치하도록 안내합니다.

4.  **품질 표준 자동 추가 (Automatic Quality Standards)**
    - 사용자가 놓치기 쉬운 **성능, 접근성, 테스트 요구사항**을 자동으로 프롬프트에 추가하여 코드 품질을 상향 평준화합니다.

5.  **실용적인 시나리오 대응 (Special Situations)**
    - **레거시 코드 개선**이나 **긴급 버그 수정**과 같은 특수 상황에 맞는 맞춤형 해결책과 안전장치를 제안합니다.

## ⚙️ 동작 원리

`Prompt Enhancer`는 다음과 같은 가상 시나리오로 동작합니다.



1.  **입력 (User Request):** 사용자가 "검색 기능 추가해 줘"와 같은 간단한 명령을 입력합니다.
2.  **분석 및 컨텍스트 통합 (AI Analysis & Context):**
    - AI는 "추가" 키워드를 통해 '신규 기능 개발' 의도를 파악합니다.
    - 현재 프로젝트의 파일 구조(`src/components`, `src/hooks`), 사용 중인 라이브러리(React, Zustand), 기존 코드 스타일(`UserList.tsx`의 형태)을 가상으로 분석합니다.
3.  **숨은 요구사항 추론 (Requirement Discovery):**
    - 검색 기능에는 당연히 '입력창 UI', '디바운싱(Debouncing)', '상태 관리', '결과 하이라이팅', '테스트'가 필요하다고 추론합니다.
4.  **출력 (Enhanced Prompt):**
    - 위의 모든 정보를 종합하여 아래와 같은 상세한 개발 계획을 생성합니다.

---

### 변환 예시

**원본 요청 (Before):**
> "검색 기능 추가해 줘"

**향상된 프롬프트 (After):**
> **ProductList 컴포넌트를 위한 실시간 검색 기능 구현**
>
> **1. UI 구현:**
>    - `SearchBar.tsx` 컴포넌트를 신규 생성합니다.
>    - 기존 `UserList.tsx`의 스타일과 일관성을 유지합니다.
>
> **2. 검색 로직:**
>    - 상품명, 카테고리, 태그를 기준으로 필터링합니다.
>    - 300ms의 디바운싱(Debouncing)을 적용하여 불필요한 API 호출을 방지합니다.
>    - 검색어와 일치하는 텍스트를 하이라이트 처리합니다.
>
> **3. 상태 관리:**
>    - `useState`를 사용하여 검색어와 결과 목록을 관리합니다.
>    - `useEffect`를 사용하여 검색어 변경 시 API 호출을 최적화합니다.
>
> **4. 테스트:**
>    - `SearchBar` 컴포넌트에 대한 단위 테스트를 작성합니다.
>    - 1,000개 아이템 환경에서 성능 테스트를 수행하여 렌더링 지연이 없는지 확인합니다.

---

## 🚀 활용 방안

`PROMPT_ENHANCER.md` 문서는 다음과 같은 활용 목적을 달성하기 위해 작성되었습니다:

1.  **AI 시스템 프롬프트 (System Prompt):** Claude Code에서 사용 가능한 Opus 4, Sonnet 4와 같은 고성능 LLM의 '시스템 프롬프트' 또는 '커스텀 지시어'로 사용하여, 해당 모델을 더욱 강력한 개발 보조 도구로 변신시킬 수 있습니다.
2.  **AI 어시스턴트 개발 가이드:** 사내 맞춤형 AI 개발 도구나 봇을 제작할 때, 이 Markdown 문서를 핵심 설계 사상으로 사용할 수 있습니다.
3.  **개발자를 위한 프롬프트 작성 가이드:** 개발자 스스로가 AI에게 더 나은 질문을 던지고, 원하는 결과를 얻기 위한 사고방식 훈련 자료로 활용할 수 있습니다.

이 가이드를 통해 개발자와 AI 간의 커뮤니케이션을 혁신하고, 코드 생성의 효율과 품질을 한 차원 높일 수 있습니다.

---

## 📂 사용 방법

1. Claude Code를 실행하는 **프로젝트 폴더**의 최상위 경로에 `PROMPT_ENHANCER.md` 파일을 저장하세요.
2. **CLAUDE.md** 파일에 다음과 같은 명령어를 추가하세요:

### Prompt Enhancement Command

If the user's prompt starts with “EP:”, then the user wants to enhance the prompt. Read the `PROMPT_ENHANCER.md` file and follow the guidelines to enhance the user's prompt. Show the user the enhancement and get their permission to run it before taking action on the enhanced prompt.

3. 만약 영어 외의 다른 자연어 언어로 Claude Code를 사용한다면, 다음과 같은 명령어를 더해주세요(괄호 안의 내용은 지워도 좋습니다):

The enhanced prompts will follow the language of the original prompt (e.g., Korean prompt input will output Korean prompt enhancements, English prompt input will output English prompt enhancements, etc.)

4. 이제 Claude Code에게 작업을 요청할 때, 문장 앞에 'EP:'를 넣어서 작성하면 Claude Code가 `PROMPT_ENHANCER.md` 파일을 읽고 프롬프트 내용을 자동으로 향상시키고, 향상된 내용으로 작업하기 전 사용자에게 보여준 뒤 작업 수행 허가를 묻게 됩니다.

---

## 그럼, Claude Code와 함께 즐거운 개발 되세요!

작성자 링크드인: [xavierchoi](https://www.linkedin.com/in/xavierchoi/)
작성자 X: [whereisxavier](https://x.com/whereisxavier/)

**Full Changelog**: https://github.com/xavierchoi/Prompt-Enhancer/commits/release
