# 뉴스 키워드 분석 및 시각화 웹 애플리케이션

## 개요
이 프로젝트는 네이버 뉴스 API를 활용하여 특정 키워드와 관련된 뉴스를 수집하고, 해당 뉴스 본문으로부터 핵심 키워드를 추출하여 빈도 기반 분석 및 시각화를 수행하는 웹 애플리케이션입니다.


## 시스템 구성

사용자 입력 → NaverNewsCrawler.py → 뉴스 데이터 수집 ↓ KeywordVisualizerSTApp.py ↓ myTextMining.py → 키워드 추출 및 빈도 계산 ↓ STVisualizer.py → 막대 그래프 / 워드클라우드 출력


## 주요 기능


1. 뉴스 검색
- serchNaverNews(keyword)함수를 통해 최대 1,000건의 뉴스 검색
- JSON 데이터를 Pandas DataFrame으로 변환

2. 키워드 빈도 분석
- Okt 형태소 분석기를 사용하여 명사 단위로 추출
- Counter를 이용해 단어 빈도 계산

3. CSV 업로드 및 사용자 데이터 분석
- 사용자 CSV 업로드 후 선택된 컬럼에서 키워드 분석 수행 가능

4. 시각화
- 막대 그래프: 상위 N개의 키워드를 수평 막대그래프로 시각화
- 워드클라우드: 키워드의 빈도수를 시각적으로 보여주는 구름 형태의 이미지

# 주요 파일 설명

NaverNewsCrawler.py  네이버 뉴스 API를 통해 뉴스 데이터 수집   
myTextMining.py      키워드 추출 및 빈도수 분석 처리           
STVisualizer.py         분석 결과를 시각화 (막대그래프, 워드클라우드) 
KeywordVisualizerSTApp.py  Streamlit 기반 웹 인터페이스로 통합 운영 


# 실행 방법

1. 필요한 라이브러리 설치: pip install streamlit konlpy wordcloud matplotlib pandas

2. Streamlit 앱 실행: streamlit run KeywordVisualizerSTApp.py
   
# 결론

이 애플리케이션은 손쉽게 뉴스 데이터를 분석하고 핵심 키워드를 시각적으로 파악할 수 있습니다.
