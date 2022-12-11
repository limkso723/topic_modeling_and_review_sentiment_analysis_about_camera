### 카메라 토픽 모델링 및 리뷰 감성 분석
### topic_modeling_and_review_sentiment_analysis_about_camera
---

### 1. 프로젝트 목적
- 협업 및 의사소통 능력 향상
- Crawling, TF-IDF를 이용한 키워드 추출
- 데이터 분석 능력 배양
- Word Cloud 생성
- Konlpy 라이브러리 활용 형태소 분석기 비교(OKT, Mecab) 및 사용법 숙달
- 리뷰 감성 분석
- 데이터 전처리(re 모듈) 및 분석
- N-gram 이용 키워드 추출



### 2. 주제 선정 이유
<img src="https://user-images.githubusercontent.com/83712521/206904233-34fd33af-edd4-4ce8-b814-8d21a4ef327b.png" width="500" height="300">

#### (1) 배경
- 10년 간 카메라 매출액이 1/4배로 급하락 및 
- 카메라 시장의 변화 (DSLR 단종, 미러리스 발전)
#### (2) 도출 사항
- 크게 비교되는 두 회사(소니, 캐논)의 특징이 잘 드러남

    → 두 회사 및 제품들의 감성 분석 비교 용이  
- 카메라 시장의 변화 추이가 뚜렷함

    → 토픽 모델링 시 변화 차이 확인 및 데이터 분석 용이



### 3. 데이터 및 모델
#### (1) 데이터
- 리뷰 감성 분석
    - 네이버 쇼핑 제품 리뷰 약 12,000개 
    
       (캐논, 소니 카메라 제품 중 리뷰가 100개 이상인 제품) 
- 토픽 모델링
    - 카메라 관련 10개 언론사의 기사 약 14,000개  
#### (2) 모델
- 형태소 분석기
    - konlpy (OKT, Mecab)
- TF-IDF


### 4. 과정
#### (1) 데이터 핸들링
- 불용어 처리
    - 1차 : 카메라와 관련 없는 단어를 불용어로 판단하여 제거
    - 2차 : 카메라의 성능과 관련없는 단어를 불용어로 판단하여 추가 제거 
<img src="https://user-images.githubusercontent.com/83712521/206904554-7fb0fbc3-eba8-43ab-acf1-038b90df15fb.png" width="200" height="200">
- 데이터 시각화 (matplotlib, seaborn, plotly)
#### (2) 모델 핸들링
- 형태소 분석기
    - OKT, Mecab이용 토큰화 및 품사 태깅 (명사, 형용사, 부사)
- TF-IDF 


### 5. 결과 및 성과
#### (1) 느낀점
- 머신러닝, 딥러닝은 데이터 확보가 중요하다는 것을 배웠고, Crawling 사용 방법을 숙달하였다. 
하지만 보호영역을 부정한 방법으로 접근하면 불법이므로 위법하지 않은지 확인하고 crawling을 해야한다는 것을 배웠다. 
- konlpy를 이용한 형태소 분석으로 리뷰의 감성을 분석하고 뉴스의 키워드를 추출하였다.
추출한 키워드로 word cloud를 생성하였고 TF-IDF를 적용하여 topic modeling을 하는 일련의 과정을 숙달하였다.
- topic modeling한 데이터를 시각화하여 분석하는 능력을 숙달하였다. 특히 년도별 추출한 키워드들이 카메라 시장의 변화 추이를 반영한 결과로 도출되어 놀라웠다.
- 처음 팀 프로젝트를 진행하며 자연어 처리에 흥미를 갖게 되는 계기가 되었고, 가설 설정과 입증하는 과정을 통해 모델의 성능 향상을 예측하는 방향성을 배웠다.
- 발표 자료를 작성하고 발표를 하면서 머신러닝 엔지니어가 주목해야 하는 내용이 성능 개선에 대한 노력이고, 이를 위해 데이터 전처리와 모델의 하이퍼 파라미터를 조절해야 한다는 것을 배웠다.

#### (2) 사진
- 키워드 시각화
<img src="https://user-images.githubusercontent.com/83712521/206905386-0807cc57-8d07-4395-bba4-c158752ac102.png" width="500" height="300">
- 토픽 모델링
<img src="https://user-images.githubusercontent.com/83712521/206905316-0be2d07e-708e-49ec-83c8-b48fed1b4010.png" width="500" height="300">
- N-gram
<img src="https://user-images.githubusercontent.com/83712521/206905465-15e27798-27ed-44de-9828-b2dd7c089044.png" width="500" height="300">
- word cloud
<img src="https://user-images.githubusercontent.com/83712521/206904080-77d47eb3-2e2a-44e5-8a72-7b7a4cf7e510.png" width="300" height="300">

### 6. 추후 개선 방향
- cosine similarity(코사인 유사도) 활용 문서별 토픽 모델링 진행
- BERT 모델을 이용한 감성분석 진행

### 7. 구성원 및 역할
- 공통 : 불용어 사전 작성, 코드 정리, 발표자료 작성
- 국승용 : crawling (소니 카메라 리뷰), konlpy OKT, TF-IDF, Uni-gram, 키워드 시각화(word cloud), 발표
- 김채리 : crawling (소니 카메라 리뷰), konlpy OKT, TF-IDF, Bi-gram, 키워드 시각화(histogram)
- 손정환 : crawling (1~5번 언론사 뉴스 기사), konlpy OKT, 키워드 시각화(histogram)
- 양병진 : crawling (6~10번 언론사 뉴스 기사), konlpy OKT, 키워드 시각화(histogram)
- 최현호 : crawling (캐논 카메라 리뷰), konlpy Mecab, Bi-gram(부정 리뷰), 키워드 시각화(histogram)
