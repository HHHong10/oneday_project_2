![header](https://capsule-render.vercel.app/api?type=waving&color=75BDE0&height=300&section=header&text=EDA%20Project&fontSize=65)

# oneday_project_2
## 프로젝트 소개
### 테러 특성 및 양상 분석
- 전세계 테러 데이터(GTD) 활용
- 약 180,000 건의 데이터: 1970년 ~ 2016년의 데이터
- 135개의 column을 포함해 필요한 column 따로 추출 필요

> 전체 년도 테러 정보 데이터프레임   
> 테러 발생 상위 10개 국가 데이터프레임   
> 특정 8개 지역의 공격 형태, 대상 데이터프레임

## 프로젝트 목표
- 전세계 테러 공격 연간 추이 파악
- 과거 테러 공격의 특이점 및 이슈 파악
- 특정 8개 지역별 특성 파악
- 테러 감소를 위한 경각심 고취 시각화

## 프로젝트 내용
#### terror DataFrame   
> 전체 column 중 테러 발생시점, 공격 형태, 국가, 지역, 부상자 수 , 사망자 수, 테러 발생 지역의 위치정보, 공격대상, 동기 추출

### 1. 전체 연도별 테러 발생 횟수 집계
seaborn - countplot 활용 시각화

<img width="1075" alt="Screen Shot 2021-11-16 at 1 33 39 PM" src="https://user-images.githubusercontent.com/48639017/141921553-094ed01a-c86f-4c57-9419-53b32e37b836.png">

- 시간이 지남에 따라 테러 발생이 증가하는 추세
- 2012 ~ 2014 : 테러 발생 급증
- 테러 증가의 일반적인 원인: 중동 지역 간 분쟁 증가, 전쟁 도구로 테러 활용, 경제적 문제에 대한 불만 고조 등
- 실제, 2013년 세계경제는 유럽재정위기의 심화, 중국과 미국의 경기부진으로 글로벌 금융위기 직후인 2009년 이래 가장 나쁜 상황
- 💡 세계경제 위기로 인해 점차 테러 증가 추측
- 2012: [이노센스 오브 무슬림] 반 이슬람 영화로 반미 시위 발발
- 2013: 파키스탄 폭탄테러 발발, 정부 겨냥
- 💡 국가 간 갈등 심화로 인한 테러 증가 추측


### 2. 테러 발생 상위 10개국 파악
matplotlib.pyplot - bar 활용 시각화

<img width="1058" alt="Screen Shot 2021-11-16 at 1 33 57 PM" src="https://user-images.githubusercontent.com/48639017/141922963-2049bd2c-de17-423a-980f-20e3672a42e6.png">

- 이라크, 파키탄, 아프니탄: 상위 3개 국가
- 💡 중동, 남아시아, 남아메리카, 서유럽에서 테러가 많이 발생

### 3. 상위 10개국 사망자 및 부상자 수 파악









![header](https://capsule-render.vercel.app/api?type=waving&color=75BDE0&height=200&section=footer&fontSize=72)

