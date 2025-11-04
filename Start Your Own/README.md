# 직접 시작하기

이 폴더를 통해 여러분은 거래 실험을 여러분의 컴퓨터에서 직접 실행할 수 있습니다. 여기에는 두 개의 작은 스크립트와 그 스크립트들이 생성하는 CSV 파일이 포함되어 있습니다.

아래 명령어를 저장소 루트에서 실행하세요. 스크립트가 CSV 데이터를 자동으로 이 폴더 안에 저장합니다.

## 개요

**의존성 설치:**

```bash
# 권장: 가상 환경 사용
python -m venv venv
source venv/bin/activate  # Windows의 경우: venv\Scripts\activate

pip install -r requirements.txt
```

### `trading_script.py`

### `trading_script.py` 인자(Argument) 표

| 인자 | 단축 | 기본값 | 선택 가능한 값 | 설명 |
|---|---|---|---|---|
| `--data-dir` | | 없음 | | **필수** 데이터 디렉터리 |
| `--asof` | | 없음 | | 이 `YYYY-MM-DD`를 "오늘"로 간주 |
| `--log-level` | | 없음 | DEBUG, INFO, WARNING, ERROR, CRITICAL | 로깅 레벨 설정 (기본값: 없음) |
| `--starting-equity` | `-s` | 없음 | | 선택 사항. 시작 자금 (현금 금액) |

### 예시

  - 실행에 필요한 데이터 디렉터리:
    `python trading_script.py --data-dir "Start Your Own"`

  - 오늘이 2025-10-01이라고 가정하고 실행:
    `python trading_script.py --data-dir "Start Your Own" --asof 2025-10-01`

  - 상세 로깅을 활성화하고 실행:
    `python trading_script.py --data-dir "Start Your Own" --log-level DEBUG`

  - $10,000의 시작 자금으로 실행:
    `python trading_script.py --data-dir "Start Your Own" --starting-equity 10000`

  - 여러 옵션 조합하여 실행:
    `python trading_script.py --data-dir "Start Your Own" --asof 2025-10-01 --log-level INFO -s 5000`

### `Start Your Own/ProcessPortfolio.py`

`trading_script.py`의 단순한 래퍼(Wrapper)입니다. 데이터 디렉터리로 'Start Your Own'을 자동으로 사용합니다. 단, 다른 인자는 지원하지 않습니다.

**그래프 생성:**

**프로그램은 항상 'Start Your Own/chatgpt\_portfolio\_update.csv'의 데이터를 사용합니다.**

1.  **포트폴리오 데이터가 있는지 확인하세요.**

      - `chatgpt_portfolio_update.csv`에 데이터가 있도록 `ProcessPortfolio.py`를 최소 한 번 실행해야 합니다.

    <!-- end list -->

    ```bash
    python "Start Your Own/Generate_Graph.py"
    ```

### 'Generate\_Graph.py' 인자 표

| 인자 | 타입 | 기본값 | 설명 |
|---|---|---|---|
| `--start-date` | 문자열(str) | CSV 파일의 시작 날짜 | `YYYY-MM-DD` 형식의 시작 날짜 |
| `--end-date` | 문자열(str) | CSV 파일의 끝 날짜 | `YYYY-MM-DD` 형식의 끝 날짜 |
| `--start-equity` | 실수(float) | 100.0 | 두 시리즈를 인덱싱하기 위한 기준선 (기본값 100) |
| `--output` | 문자열(str) | — | 차트를 저장할 선택적 경로 (`.png` / `.jpg` / `.pdf`) |

### 중요 사항

프로그램은 시장이 마감되는 **동부 표준시(EST) 오후 4시 이후**에 항상 실행해야 합니다. 그렇지 않으면 이전 날짜의 데이터를 기본으로 사용하게 됩니다.

이 프로그램은 과거 데이터에 의존하기 때문에, 특정 날짜의 주문은 해당 날짜의 거래 세션이 끝난 후에 생성되며 **다음 거래일**에 실행되어야 합니다. 이는 미래 예측 편향(lookahead bias)을 방지합니다. 예를 들어, 제가 ChatGPT로부터 주문을 받을 때, 프로그램을 실행하고 다음 날 마감 시점에 해당 주문을 입력합니다.

**정보**

  * 프로그램은 'chatgpt\_portfolio\_update.csv'의 과거 데이터를 사용하여 오늘의 포트폴리오를 자동으로 가져옵니다.
  * 'chatgpt\_portfolio\_update.csv'가 비어 있는 경우(과거 거래일 기록이 없다는 의미), 시작 현금을 직접 입력해야 합니다.
  * 여기에서 포트폴리오를 설정하거나 변경할 수 있습니다.
  * 스크립트는 수동 매수 또는 매도를 기록할지 묻습니다.
  * 'Enter'를 누르면 해당 날짜의 모든 계산이 이루어집니다.
  * 결과는 `chatgpt_portfolio_update.csv`에 저장되며, 모든 거래는 `chatgpt_trade_log.csv`에 추가됩니다.
  * 터미널에 일일 결과가 출력됩니다. 이 결과를 복사하여 LLM에 붙여넣으세요.
    프롬프트 자동화에 대해서는 [자동화 가이드](https://github.com/LuckyOne7777/ChatGPT-Micro-Cap-Experiment/blob/main/Other/AUTOMATION_README.md)를 확인하세요.

이 모든 것은 아직 **매우 초기 단계**이므로 버그가 있을 수 있습니다. 문제점을 발견하거나 질문이 있으시면 언제든지 연락해 주십시오.

두 스크립트 모두 초보자를 위해 설계되었으니, 학습하면서 자유롭게 실험하고 수정해 보세요.