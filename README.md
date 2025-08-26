# 페르소나 챗봇

Streamlit과 LangChain Upstage 기반의 페르소나 챗봇 프로젝트입니다.  
사용자가 선택한 캐릭터와 모델을 기반으로 대화할 수 있습니다.

---

## 설치

Python 3.9 이상을 권장합니다.

```bash
# 가상환경 생성
python -m venv mychatbotvenv

# 가상환경 활성화 (Windows)
mychatbotvenv\Scripts\activate

# 또는 (Git Bash)
source mychatbotvenv/Scripts/activate

# 패키지 설치
pip install -r requirements.txt
```

## 환경 변수 설정
1. .env.example 파일을 복사하여 .env 파일을 생성합니다.
2. .env 파일에 본인의 Upstage API 키를 입력합니다.
3. .gitignore에는 반드시 .env를 추가합니다.(배포시)

## 챗봇 실행
```bash
streamlit run app.py
```

## 캐릭터 선택
챗봇 실행 후, 드롭다운에서 캐릭터를 선택할 수 있습니다.
    - Trump
    - Heavy Grandma
    - FunCoolSexy

## 주의 사항
1. .env 파일에는 개인 API 키가 들어 있으므로 절대 GitHub에 올리지 마세요.
2. 배포 시 .env.example만 올리고, 사용자가 복사하여 .env를 생성하도록 합니다.
3. 가상환경 사용을 권장합니다.
4. Python 3.9 이상, Streamlit 1.48.1, LangChain-Upstage 0.7.3 환경을 기준으로 합니다.