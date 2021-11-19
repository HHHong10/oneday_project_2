# oneday_project_2
## 프로젝트 소개
### 테러 특성 및 양상 분석
- 전세계 테러 데이터(GTD) 활용
- 약 180,000 건의 데이터: 1970년 ~ 2016년의 데이터
- 135개의 column을 포함해 필요한 column 따로 추출 필요

> 전체 년도 테러 정보 데이터프레임   
> 테러 발생 상위 10개 국가 데이터프레임   
> 특정 8개 지역의 공격 형태, 대상 데이터프레임

</br>

## 프로젝트 목표
- 전세계 테러 공격 연간 추이 파악
- 과거 테러 공격의 특이점 및 이슈 파악
- 특정 8개 지역별 특성 파악
- 테러 감소를 위한 경각심 고취 시각화

</br>

## 프로젝트 내용

### 1. 전체 연도별 테러 발생 횟수 집계
#### terror DataFrame   
> 전체 column 중 테러 발생시점, 공격 형태, 국가, 지역, 부상자 수 , 사망자 수, 테러 발생 지역의 위치정보, 공격대상, 동기 추출

##### seaborn - countplot 활용 시각화

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
#### terror_top DataFrame
> 국가별 그룹화 후 전체 기간 테러 발생 횟수, 사망자, 부상자, 사상자(사망+부상자) 컬럼 추가 후 발생 횟수로 내림차순 해 상위 10개국 추출

##### matplotlib.pyplot - bar 활용 시각화

<img width="1058" alt="Screen Shot 2021-11-16 at 1 33 57 PM" src="https://user-images.githubusercontent.com/48639017/141922963-2049bd2c-de17-423a-980f-20e3672a42e6.png">

- 이라크, 파키탄, 아프니탄: 상위 3개 국가
- 💡 중동, 남아시아, 남아메리카, 서유럽에서 테러가 많이 발생

### 3. 상위 10개국 사망자 및 부상자 수 파악
##### pandas.DataFrame.plot / seaborn - barplot 활용 시각화

<img width="884" alt="Screen Shot 2021-11-19 at 10 09 34 AM" src="https://user-images.githubusercontent.com/48639017/142524086-65169609-c78c-4b96-9cbe-8d6d8b774aff.png">   

<img width="896" alt="Screen Shot 2021-11-19 at 10 11 48 AM" src="https://user-images.githubusercontent.com/48639017/142525462-e388da50-71af-4e94-82ae-8cfdb16a063b.png">

- 전체적으로 테러 발생 횟수보다 사망자와 부상자 수가 높음
- United Kingdom의 경우, 유일하게 사망자가 발생 횟수보다 낮음
    - 💡 2007년 폭탄 테러 시도 실패 사례 등의 다수의 테러 실패 및 사전 검거
- Iraq의 경우 테러 발생 횟수의 6배 수치에 달하는 부상자 발생
    - 💡 Iraq에서 발생한 테러 중 쇼핑센터, 시장에서 폭탄 테러 사례로 한 번에 많은 사상자 수 발생


### 4. 특정 8개 지역 특성 파악
#### terror_country DataFrame
> 중동&북아프리카, 남아시아, 남아메리카, 서유럽, 남동아시아, 동유럽, 북아메리카, 동아시아 지역별 공격 형태, 사상자 수

#### 지역별 사망자와 사상자 시각화

<img width="784" alt="Screen Shot 2021-11-19 at 10 47 59 AM" src="https://user-images.githubusercontent.com/48639017/142550843-87411d25-e6a8-48bc-89bf-b86f49eeee20.png">

- Middle East & North Africa에서 최다 사상자 수
- 💡 앞선 상위 10개국 결과처럼 중동 테러 위험 지역으로 구분 가능

#### 지역별 테러 공격 형태 시각화

<img width="812" alt="Screen Shot 2021-11-19 at 10 28 13 AM" src="https://user-images.githubusercontent.com/48639017/142537110-bf460a63-7320-4c3a-9e5a-ea61581dd4e9.png">

![11](https://user-images.githubusercontent.com/48639017/142540391-ba7c35ef-e5ad-4b5c-b2fd-60e98b0f9910.png)

- 폭발 테러가 가장 빈번
    - 💡 중동/북아프리카에서 60%를 차지하는 것으로 보아, 폭발 테러의 피해 정도가 커 사상자 수가 많은 것으로 추측
- 대체로 두번째로 무장습격이 빈번
- East Asia/North America는 Facility/Infrastructure Attack, Western Europe은 Assassination과 Facility/Infrastructure Attack이 두번째로 많음
    - 💡 영국 정부 대상의 이슬람 테러 단체의 움직임

### 5. 특정 8개 지역 특정 기간의 양상
#### before_count, after_count DataFrame
> 1. 에서 2012~2014 테러 발생 급증 확인   
> 2011년 기준 과거와 이후의 공격 대상 카운팅
> 2011년 기준 과거와 이후의 테러 발생 횟수 카운팅  

#### 2011년 기준 지역별 테러 발생 횟수 시각화
<img width="783" alt="Screen Shot 2021-11-19 at 1 47 07 PM" src="https://user-images.githubusercontent.com/48639017/142566511-5c2875da-1f6b-41b7-8dc9-9487e045a0a1.png">

- South America, Western Europe 지역의 테러 발생 감소
    - 💡 세계경제 위기 고조와 테러 발생 증가는 비례하지 않음
- Middle East & North Africa, South Asia 지역의 테러 발생 증가
    - 💡 지역 내 세력 다툼으로 테러 증가 추측

#### 2011년 기준 공격 대상 변화 시각화
<img width="876" alt="Screen Shot 2021-11-19 at 1 29 10 PM" src="https://user-images.githubusercontent.com/48639017/142565052-b24e7870-f78b-440a-8a34-32f101fae8f5.png">

- Military, Police, Private Citizens & Property 대상 테러는 2011년 이후 증가
    - 💡 2000년대 이후 종교적 이상주의에 심취해 무고한 시민 대상의 무차별적 테러 증가
- Tourists, Airports & Aircraft, Gorvernment(General) 대상 테러는 2011년 이후 감소
    - 💡 2010년 9.11 테러 발생의 영향 있을 것으로 추측

### 6. 특정 7개 지역 1970~2010년대 특성 분석
#### period_region DataFrame
> 앞선 8개 지역 중 7개 지역을 시대별 구분하기 위한 데이터프레임    
> 해당 데이터 10년 단위로 구분

#### 시대별 지역 테러 발생 시각화
<img width="783" alt="Screen Shot 2021-11-19 at 2 12 28 PM" src="https://user-images.githubusercontent.com/48639017/142568690-36ad940c-807c-4756-bc96-28a9ad1d79fe.png">

- 시간의 흐름에 따라 테러 발생 증가
    - Western Europe 줄어듦

#### 시대별 지역 테러 발생 시각화
<img width="783" alt="Screen Shot 2021-11-19 at 2 23 33 PM" src="https://user-images.githubusercontent.com/48639017/142569784-e9694fe5-6ff0-4e8f-8281-6942fbdc7a44.png">

- 💡 시민, 군사, 경찰 대상 테러의 증가

</br>
### 참고
[최근 국외 뉴테러리즘의 사례분석과 국내 발생가능 유형에 대한 연구](https://www.koreascience.or.kr/article/JAKO201719063370032.pdf) ㄴ