# 페르소나 챗봇

Streamlit과 LangChain Upstage 기반의 페르소나 챗봇 프로젝트입니다.  
사용자가 선택한 캐릭터와 모델을 기반으로 대화할 수 있습니다.

---

## 📂 프로젝트 구조
```markdown
streamlit-LLM_Chatbot/
│
├─ app.py # Streamlit 앱 메인
├─ utils.py # 모델 로딩, 체인 초기화, 메모리 설정 등 유틸 함수
├─ requirements.txt # 프로젝트 패키지 및 버전
├─ README.md
└─ venv/ # 가상환경
```

## ⚡ 주요 기능

- LangChain 기반 LLM 모델 연동
- Streamlit UI에서 실시간 챗봇 대화
- 세션 메모리 기반 대화 상태 유지

## 설치 및 실행

Python 3.11 권장

```bash
# 저장소 클론
git clone <your-repo-url>
cd streamlit-LLM_Chatbot

# 가상환경 생성
python -m venv <your-venv>

# 가상환경 활성화 (Windows)
<your-venv>\Scripts\activate

# 또는 (Git Bash)
source mychatbotvenv/Scripts/activate

# pip, setuptools, wheel 업그레이드 및 재설치
python -m pip install --upgrade --force-reinstall pip setuptools wheel

# 패키지 설치
pip install -r requirements.txt

# 패키지 상태 확인
pip check

# Streamlit 앱 실행
streamlit run app.py
```
⚠️ 주의: 이전 설치에서 경고가 나올 수 있으나, 위 명령어를 실행하면 정상 설치됩니다.

## 🛠️ 사용한 라이브러리
    - streamlit : 웹 UI
    - langchain, langchain-core, langchain-openai : LLM 모델 및 체인
    - openai : OpenAI API
    - pandas, numpy : 데이터 처리
    - SQLAlchemy : 메모리 저장용 DB
    - python-dotenv : 환경 변수 관리

## 🔑 환경 변수 설정
1. .env.example 파일을 복사하여 .env 파일을 생성합니다.
2. .env 파일에 본인의 Upstage API 키를 입력합니다.
3. .gitignore에는 반드시 .env를 추가합니다.(배포시)

## 💡 참고 사항
    - 패키지 버전은 requirements.txt 기준으로 설치해야 호환성 문제 없음
    - 모델 API Key 등은 .env 파일에 저장 후 로딩

## 🎭 캐릭터 선택
챗봇 실행 후, 드롭다운에서 캐릭터를 선택할 수 있습니다.
    - Trump
    - Heavy Grandma
    - FunCoolSexy

## 📌 앞으로 개선할 점
    - 챗봇 메모리 최적화
    - PDF, 웹 페이지 등 다양한 문서 처리 추가
    - 사용자 UI 개선 및 테마 적용
    - 페르소나가 무너지지 않도록 주의하며 페르소나 구축

## ⚠️ 주의 사항
1. .env 파일에는 개인 API 키가 들어 있으므로 절대 GitHub에 올리지 마세요.
2. 배포 시 .env.example만 올리고, 사용자가 복사하여 .env를 생성하도록 합니다.
3. 가상환경 사용을 권장합니다.