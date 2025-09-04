# 🎭 Sentiment Analysis Project

한국어 감정 분석 데이터셋을 활용한 감정 분석 프로젝트입니다.

## 🚀 빠른 시작 (Quick Start)

### 1. 가상환경 생성
```bash
uv venv venv
```

### 2. 가상환경 활성화
```bash
# Windows
venv\Scripts\activate

# Linux/Mac
source venv/bin/activate
```

### 3. 의존성 설치
```bash
# 프로덕션 의존성 설치
uv pip install -r requirements.txt

# 개발 의존성 설치
uv pip install -r requirements-dev.txt
```

### 4. Jupyter Lab 시작
```bash
jupyter lab
```

## 📦 패키지 관리

이 프로젝트는 **UV**를 사용하여 패키지를 관리합니다.

### 주요 명령어
```bash
# 가상환경 생성
uv venv venv

# 의존성 설치
uv pip install -r requirements.txt
uv pip install -r requirements-dev.txt

# Jupyter Lab 시작
jupyter lab

# 테스트 실행
pytest

# 코드 포맷팅
black .
isort .

# 린팅 검사
flake8 .
mypy .
```

### 의존성 관리
- **프로덕션 의존성**: `requirements.txt`
- **개발 의존성**: `requirements-dev.txt`
- **프로젝트 설정**: `pyproject.toml`

## 🏗️ 프로젝트 구조

```
Sentiment_Analysis/
├── venv/                    # 가상환경 (Git에서 제외)
├── pyproject.toml          # UV 프로젝트 설정
├── requirements.txt        # 프로덕션 의존성
├── requirements-dev.txt    # 개발 의존성
├── .python-version         # Python 버전 고정
├── .gitignore              # Git 무시 파일
├── .cursor/                # Cursor 설정
│   └── rules/
│       └── package-management-rule.mdc
├── data_preprocess.ipynb  # 데이터 전처리 노트북
└── README.md              # 이 파일
```

## 🛠️ 개발 환경

- **Python**: 3.11.7
- **패키지 관리자**: UV
- **가상환경**: venv 폴더
- **개발 도구**: Jupyter Lab, Black, isort, flake8, mypy, pytest

## 📊 데이터셋

- **데이터셋**: Korean Emotion Dataset
- **소스**: Hugging Face Hub (`m2af/ko-emotion-dataset`)
- **형식**: Parquet 파일

## 🔧 개발 워크플로우

### 1. 일일 개발 시작
```bash
# 가상환경 활성화
venv\Scripts\activate  # Windows
# 또는
source venv/bin/activate  # Linux/Mac

# 의존성 동기화 (필요시)
uv pip install -r requirements.txt
uv pip install -r requirements-dev.txt

# Jupyter Lab 시작
jupyter lab
```

### 2. 코드 품질 관리
```bash
# 코드 포맷팅
black .
isort .

# 린팅 검사
flake8 .
mypy .

# 테스트 실행
pytest
```

## 📝 의존성 추가/제거

### 새 의존성 추가
```bash
# 1. 가상환경 활성화
venv\Scripts\activate  # Windows
# 또는
source venv/bin/activate  # Linux/Mac

# 2. 의존성 설치
uv pip install package_name==version

# 3. requirements.txt 업데이트
uv pip freeze > requirements.txt

# 4. 커밋
git add requirements.txt
git commit -m "Add package_name dependency"
```

### 의존성 제거
```bash
# 1. 가상환경 활성화
venv\Scripts\activate  # Windows
# 또는
source venv/bin/activate  # Linux/Mac

# 2. 의존성 제거
uv pip uninstall package_name

# 3. requirements.txt 업데이트
uv pip freeze > requirements.txt

# 4. 커밋
git add requirements.txt
git commit -m "Remove package_name dependency"
```

## 🚫 주의사항

- ❌ `pip install` 직접 사용 금지 (UV 사용)
- ❌ `conda install` 사용 금지 (UV와 충돌)
- ❌ `venv/` 폴더를 Git에 커밋 금지
- ✅ 모든 의존성 버전을 정확히 명시
- ✅ 의존성 추가/제거 시 테스트 필수

## 🔍 문제 해결

### 가상환경 문제
```bash
# 가상환경 재생성
rm -rf venv  # Linux/Mac
# 또는
rmdir /s venv  # Windows

uv venv venv
venv\Scripts\activate  # Windows
# 또는
source venv/bin/activate  # Linux/Mac

uv pip install -r requirements.txt
uv pip install -r requirements-dev.txt
```

### 의존성 충돌
```bash
# 의존성 트리 확인
uv pip list

# 충돌하는 패키지 확인
uv pip check
```

## 📚 참고 자료

- [UV 공식 문서](https://docs.astral.sh/uv/)
- [Python 패키징 가이드](https://packaging.python.org/)
- [PEP 621 - 프로젝트 메타데이터](https://peps.python.org/pep-0621/)

## 📄 라이선스

MIT License

---

**마지막 업데이트**: 2024년 9월 4일
