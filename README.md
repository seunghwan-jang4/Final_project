# OTT 성향에 맞는 드라마/애니/영화 추천 AI 챗봇

## 📌 프로젝트 소개

<details>
<summary>프로젝트 개요 및 일정</summary>

### 프로젝트 개요

각 OTT가 제공하는 콘텐츠(영화/드라마/애니메이션)를 분석 및 분류하여, 분위기가 비슷한 것들끼리 묶어서 새로운 카테고리를 생성합니다. 그리고 사용자에게 카테고리를 선택하게 하여, 적절한 추천 목록을 제공하는 추천 시스템입니다.

### 개발 환경 및 사용 예정 기술
- **IDE**: Visual Studio Code
- **OS**: Windows, macOS
- **가상 환경**: myvenv
- **버전 관리**: Git

### 개발 일정
- **12월 30일 ~ 1월 3일**: 역할 분담 및 아이디어 정리, SA문서, README 작성, 와이어프레임 작성
- 이후 일정은 추가 예정
  
</details>

<details>
<summary>폴더 구조</summary>
   
### 폴더 구조 

```bash
OTTRecommendationSystem/   # (1) repository_root
├─ .gitignore
├─ README.md
├─ requirements.txt
├─ venv/                    # 가상 환경
├─ my_project/              # (2) project_root
│  ├─ apps/
│  │  └─ myapp/
│  │     ├─ models/
│  │     │  ├─ __init__.py
│  │     │  ├─ profile.py
│  │     │  └─ instagram.py
│  │     ├─ views/
│  │     ├─ forms/
│  │     ├─ admin.py
│  │     ├─ models.py
│  │     └─ tests.py
│  ├─ config/                # (3) configuration_root
│  │  ├─ settings/
│  │  │  ├─ __init__.py
│  │  │  ├─ base.py
│  │  │  ├─ dev.py
│  │  │  └─ prod.py
│  │  ├─ asgi.py
│  │  ├─ urls.py
│  │  └─ wsgi.py
│  ├─ static/
│  │  └─ assets/             # 정적 파일
│  ├─ media/
│  │  └─ uploads/            # 업로드 파일
│  ├─ templates/
│  │  └─ myapp/
│  └─ manage.py
```

</details>

---

## 🌟 프로젝트 선정 이유


<details>
<summary>내용 보기</summary>

요즘은 각 OTT마다 방대한 양의 미디어 콘텐츠가 제공되고 있어, 사용자가 원하는 콘텐츠를 선택하는 데 많은 시간이 소요됩니다.  
특히, 플랫폼마다 추천 알고리즘의 편차가 커 사용자가 자신의 취향에 딱 맞는 콘텐츠를 찾기 어려운 상황입니다.  

이 프로젝트는 이러한 문제를 해결하기 위해 시작되었습니다.  
OTT에서 제공하는 콘텐츠를 분석 및 분류하여 **사용자 맞춤형 추천 시스템**을 개발함으로써, 번거로움 없이 바로 콘텐츠에 몰입할 수 있는 환경을 제공하고자 합니다.  
이를 통해 사용자는 **플랫폼의 경계를 넘어선 통합 추천 경험**을 얻을 수 있으며, **콘텐츠 소비의 효율성** 또한 크게 향상될 것으로 기대됩니다.


</details>

---

## 📁 프로젝트 구조

<details>
<summary>내용 보기</summary>

![프로젝트구조(12조)](https://github.com/user-attachments/assets/7565ee2b-c461-42dc-8c59-af33f6ab26da)

</details>

---

## 🎮 주요 기능

<details>
<summary>내용 보기</summary>

1. **콘텐츠 분석 및 분류**
   - 영화, 드라마, 애니메이션 등 다양한 OTT 콘텐츠의 분위기를 자동으로 분석.
   - 분석된 콘텐츠를 새로운 카테고리로 묶어 사용자에게 제공.

2. **추천 시스템**
   - 사용자가 선호하는 카테고리를 선택하면 관련 콘텐츠 추천.
   - 유사 콘텐츠 추천 알고리즘 적용.

3. **사용자 인터페이스**
   - 직관적인 UI로 카테고리 선택 및 추천 결과 확인 가능.
   - 검색 필터 기능으로 세부적인 콘텐츠 검색 지원.

4. **데이터 관리**
   - MariaDB를 사용해 콘텐츠 데이터를 안전하고 효율적으로 저장.
   - Django Admin을 통해 데이터 관리 및 검토 가능.

</details>

---

## 🛠 기술 스택

<details>
<summary>내용 보기</summary>

- **Backend**: Django REST Framework, Python 3.10
- **Database**: MariaDB
- **Frontend**: React (Optional)

</details>

---

## 💻 설치 및 실행 방법

<details>
<summary>내용 보기</summary>

### 1. **환경 설정**
1. 저장소를 클론합니다.
   ```bash
   git clone https://github.com/your-repository-url.git
   cd your-repository-name

2. 가상 환경을 생성하고 활성화합니다.

```bash
python -m venv myvenv
source myvenv/bin/activate  # macOS/Linux
myvenv\Scripts\activate
```
3. 필수 패키지를 설치합니다.

```bash
pip install -r requirements.txt
```


### 2. **데이터 베이스 설정**

1. settings.py에서 데이터베이스 정보를 수정합니다.
```python
DATABASES ={
}
```
2. 마이그레이션을 실행합니다.

```bash
python manage.py makemigrations
python manage.py migrate
```


### **3. 서버 실행**

1. 개발 서버를 실행합니다.
```bash
python manage.py runserver
```

</details>

---

## 🔍 트러블슈팅
<details>
<summary>해결된 이슈 목록</summary>

| 문제 발생일   | 이슈 내용   | 해결 방안 | 담당자 |
|--------------|-------------|-----------|-------|
|              |             |           |       |

</details>


## 결과

<details>
<summary>내용 보기</summary>

(공란)

</details>


  
### 역할 분담
<details>
<summary>역할 분담</summary>

| 이름     | 역할       | 업무                                       |
|----------|------------|--------------------------------------------|
| 장승환   | 프론트엔드 | 프로젝트 일정 관리 및 문서화 작업, UI 설계 및 구현 |
| 김건태   | 크롤링     | 데이터 크롤링                             |
| 박수호B  | 백엔드 및 데이터 엔지니어 | LangChain 활용 데이터 처리 및 RAG 시스템 구현 |
| 이명혜   | 크롤링     | 데이터 크롤링                             |

</details>



### ERD
<details>
<summary>ERD 1.0 </summary>
<img src = https://github.com/user-attachments/assets/0fffd09e-036f-426a-ac29-901c0dbfdca1>
</details>

<details>
<summary>ERD 1.1 </summary>
<image (1) src = https://github.com/user-attachments/assets/b3abd6a2-bf37-4c42-89c8-3842f104225f>
</details>

<details>
<summary>ERD 1.11 </summary>
<image (2) src = https://github.com/user-attachments/assets/6ad73f79-c7a4-4ce6-9bff-8bda5e604938>
</details>

### 레퍼런스 
<details>
<summary>레퍼런스 출처</summary>
https://teamsparta.notion.site/SA-97b05811e819459db6bfd1cd79ae6c1a

</details>

