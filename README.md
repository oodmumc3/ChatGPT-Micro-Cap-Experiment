## ChatGPT 소형주 실험

이 저장소는 ChatGPT가 실제 현금으로 소형주 포트폴리오를 관리하는 저의 6개월 실시간 트레이딩 실험의 기반입니다.

-----

### 시작 개요: [여기](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/blob/main/Start%20Your%20Own/README.md)

### 저장소 구조

  * **`trading_script.py`** - 포트폴리오 관리 및 손절매 자동화 기능을 갖춘 주요 트레이딩 엔진
  * **`Scripts and CSV Files/`** - 저의 개인 포트폴리오 (매 거래일 업데이트됨)
  * **`Start Your Own/`** - 나만의 실험을 시작하기 위한 템플릿 파일 및 가이드
  * **`Weekly Deep Research (MD|PDF)/`** - 심층 연구 요약 및 성과 보고서
  * **`Experiment Details/`** - 문서, 방법론, 프롬프트 및 Q\&A

-----

## 컨셉

매일 저평가된 주식을 인공지능이 골라준다는 똑같은 광고를 계속 보았습니다. 분명히 형편없는 서비스에 가입하도록 유도하는 것이었기에, 저는 그저 눈을 흘겼습니다.
그러다가 "이게 실제로 얼마나 잘 작동할까?"라는 궁금증이 들기 시작했습니다.

그래서 저는 단 **100달러**로 시작하여, 간단하지만 강력한 질문에 답하고자 했습니다.

**ChatGPT와 같은 강력한 대규모 언어 모델이 실시간 데이터를 사용하여 실제로 '알파(Alpha)'를 창출하거나 (적어도 현명한 트레이딩 결정을 내릴 수 있을까?**

### 매 거래일마다:

  * 저는 포트폴리오에 있는 주식에 대한 거래 데이터를 제공합니다.
  * 엄격한 손절매(Stop-loss) 규칙이 적용됩니다.
  * 매주 심층 연구를 통해 계정을 재평가하도록 허용합니다.
  * 성과 데이터는 저의 블로그([여기](https://nathanbsmith729.substack.com))에 매주 추적 및 공개됩니다.

### 연구 및 문서

  * [연구 색인 (Research Index)](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/blob/main/Experiment%20Details/Deep%20Research%20Index.md)
  * [면책 조항 (Disclaimer)](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/blob/main/Experiment%20Details/Disclaimer.md)
  * [질문 및 답변 (Q\&A)](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/blob/main/Experiment%20Details/Q%26A.md)
  * [프롬프트 (Prompts)](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/blob/main/Experiment%20Details/Prompts.md)
  * [나만의 실험 시작하기 (Starting Your Own)](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/blob/main/Start%20Your%20Own/README.md)
  * [연구 요약 (MD)](https://www.google.com/search?q=https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/tree/main/Weekly%2520Deep%2520Research%2520\(MD\))
  * [전체 심층 연구 보고서 (PDF)](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/tree/main/Weekly%20Deep%20Research%20\(PDF\))
  * [채팅 기록 (Chats)](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/blob/main/Experiment%20Details/Chats.md)

-----

## 현재 성과

**현재 포트폴리오 결과**

\![Latest Performance Results] (Results.png)

**현재 상태:** 포트폴리오가 S\&P 500 벤치마크보다 **저조한 성과**를 보이고 있습니다.

*성과 데이터는 매 거래일 후에 업데이트됩니다. 자세한 일일 추적 기록은 `Scripts and CSV Files/` 폴더의 CSV 파일을 참조하세요.*

-----

## 이 저장소의 특징

  * 실시간 트레이딩 스크립트 — 가격을 평가하고 보유 주식을 매일 업데이트하는 데 사용됩니다.
  * LLM 기반 의사 결정 엔진 — ChatGPT가 거래를 선택합니다.
  * 성과 추적 — 일일 손익(PnL), 총 자산 및 거래 내역을 담은 CSV 파일
  * 시각화 도구 — ChatGPT와 지수를 비교하는 Matplotlib 그래프
  * 로그 및 거래 데이터 — 투명성을 위한 자동 저장된 로그

### 기여를 원하시면?

기여는 언제나 환영합니다\! 이 프로젝트는 커뮤니티 지향적이며, 여러분의 도움은 매우 중요합니다.

  * **이슈(Issues):** 버그를 발견하거나 개선 아이디어가 있다면 알려주세요.
  * **풀 리퀘스트(Pull Requests):** PR 제출을 자유롭게 해 주세요. 저는 보통 며칠 내로 검토합니다.
  * **협업(Collaboration):** 가치 있는 기여자들은 프로젝트의 미래를 함께 만들어갈 유지보수 담당자/관리자로 초대될 수 있습니다.

오타 수정, 기능 추가, 새로운 아이디어 논의 등 모든 기여에 감사드립니다\!

더 자세한 정보는 다음을 확인하세요: [기여 가이드 (Contributing Guide)](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/blob/main/Other/CONTRIBUTING.md)

-----

## 왜 이 프로젝트가 중요할까요?

AI는 모든 산업에서 과대 광고되고 있지만, 과연 AI가 지도 없이 돈을 관리할 수 있을까요?

이 프로젝트는 투명성, 데이터, 그리고 실제 예산을 가지고 그 해답을 찾으려는 시도입니다.

-----

## 기술 스택 및 특징

### 핵심 기술

  * **Python** - 핵심 스크립트 및 자동화
  * **pandas + yFinance** - 시장 데이터 가져오기 및 분석
  * **Matplotlib** - 성능 시각화 및 차트 작성
  * **ChatGPT-5** - AI 기반 트레이딩 의사 결정 엔진

### 주요 특징

  * **강력한 데이터 소스** - 신뢰성을 위해 Yahoo Finance를 주 소스로, Stooq를 대체 소스로 사용
  * **자동 손절매(Stop-Loss)** - 구성 가능한 손절매를 통한 자동 포지션 관리
  * **대화형 트레이딩 (Interactive Trading)** - 시가 주문(Market-on-Open, MOO) 및 지정가 주문 지원
  * **백테스팅 지원** - 과거 분석을 위한 ASOF\_DATE 오버라이드
  * **성과 분석** - CAPM 분석, 샤프/소르티노 비율, 드로다운 지표
  * **거래 로깅** - 상세한 실행 로그를 통한 완벽한 투명성

### 시스템 요구 사항

  * Python 3.11+
  * 시장 데이터를 위한 인터넷 연결
  * CSV 데이터 파일을 위한 약 10MB의 저장 공간

-----

## 팔로우하기

이 실험은 2025년 6월부터 2025년 12월까지 진행됩니다.
매 거래일마다 포트폴리오 CSV 파일을 업데이트할 것입니다.
비슷한 작업을 해보고 싶다면, 이 프로젝트를 청사진으로 자유롭게 사용하세요.

업데이트는 매주 제 블로그에 게시될 예정이며, 곧 더 많은 내용이 올라올 것입니다\!

블로그: [A.I Controls Stock Account](https://nathanbsmith729.substack.com)

기능 요청이나 조언이 있으신가요?

여기로 연락해 주세요: **nathanbsmith.business@gmail.com**