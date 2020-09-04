# ※ 팀 소개
- 팀명 : 텐텐(10 x 10 = 100% !)
- 팀원 : 박동호(팀장), 이희진, 서예지, 유세빈, 최재현
- 평균나이 : 22.6세
- 컨셉 : 열정으로 똘똘뭉친 핏덩이들의 성장일기

# 1. 데이터 시각화 프로젝트 (2020.9.2 ~ 9.9)

## Time Table
### 9.2(수)
- 목표 : 데이터 시각화(이희진), 결과작성(박동호) => 완료
### 9.3(목)
- 목표 : PPT 파일 완성(서예지), 음성녹음(유세빈) => 완료
### 과제 제출 
1) PDF파일 (전반적인 프로젝트 개요 및 설명)  
2) 발표 녹음 파일(2분 내외)
- 과제 제출 기한 9월 9일 13시까지
3) 우리의 목표 - 9/4(금) 까지 제출

# 2 인공지능 서비스 프로젝트 (2020.9.10~9.23)

## 2.1 개요
- 프로젝트 이름 : 우리집 냉장고를 부탁해
- 내용 : 코로나 사태를 맞이하여 집에서 머무는 사람이 많다. 집에 있으면 항상 끼니가 걱정인데, 배달은 비싸기도 하고 매번 시켜먹으면 질린다! 그렇기에 고안한 집에서 쉽게 요리를 해먹을 수 있도록 도와주는 서비스!
- 기능
  1. 원하는 요리를 검색하여 레시피를 찾을 수 있다. 
  2. 냉장고에 있는 재료를 인풋으로 받아, 재료에 맞는 요리들을 추천 받을 수 있다.
  3. 각 요리들에 태그를 달아 ex) 매운요리 태그별 추천도 가능
  4. 이후 등등 기능 추가~~~~
 
## Time Table
### 9.4(금)
#### 1. 첫번째 회의(11:30)
- 내용 : 각자 아이디어 구체화 및 계획안 공유. 
- 결과  

최재현 : 데이터 전처리의 문제 재료가 상당히 구체적인 경우가 많다.  
서예지 : 모델이 선택이 중요 콘텐츠 기반으로 가야한다면 시각화 디자인.  
유세빈 : 유사도 비교 추천모델을 사용하여 views.py에 바로 결과를 띄운다.  
박동호 : DB로 레시피들을 저장하여 각각의 테이블로 구성하여 DB에서 결과를 가져와 결과값 반환  
이희진 : 어떤식으로 구현할것인지 방향을 딱 잡아야한다.  
  1) CSV 파일을 기준으로 깔금하고 통일성있는 데이터를 구해야한다.
  2) 재현님과 같은 의견 전처리를 해야한다.
  3) PCA와 SVD를 사용하여 군집화를 적용하여 비슷한 종류의 요리로 묶는다. 그것을 태그로 달아서 표시를 해준다.  


#### 2. 두번쨰 회의(17:20)
- 내용 : 해먹남녀(https://www.haemukja.com/main)를 참고하여 서비스 구축방법에 대해 대략적 기획.
- 결론  
*최재현* : 중요한것 부터 잘 만들어야 한다고 생각해 일단 __조리과정과 같은 다른 서비스 빼고 재료, 음식명부터 구현하고__ 거기에 더 알파를 해야한다고 생각 데이터는 csv파일로 처리. 데이터는 아직 구체적 고민 X, 모델을 어떻게 써야할지 고민.  
*유세빈* : 해먹 사이트를 구현해본다는 쪽으로 생각. 자바스크립트가 많아서 웹은 천천히 하고, 각 요리들에 태그가 필요할 것 같다. 마지막으로 재료선택한 것이 3개면 꼭 3개가 포함된 것만 나오길래 불편했다. 이미지 재료 레시피 영양소. 유사도 모델 사용 어떤지? 데이터는 음식 커뮤니티 크롤링이 최선이다. 법이걸린다. => __기능구현.__  
*이희진* : 해먹남녀에 있는 재료로 레시피 필터링하는 기능 그게 좀 생각보다 별로다. 그런 부분을 보완하는 쪽으로 생각. 프로젝트의 목표는 서비스의 목적이 아니니, __좋은 추천 시스템(기능구현)을 중점에 두자.__ 추천 알고리즘, 비지도학습을 찾아서 기술적으로 구현해보자. => 인공지능 사관학교니까 목적에 맞게 가자  
*서예지* : 크롤링을 해서 csv파일만들어서 그것을 가지고 우리가 추천모델을 만들어서 기능을 만들어서 웹 서비스를 구현하는 쪽으로가자 => __기술중심__ 다른 서비스에서도 데이터 크롤링으로 협업필터링과 같은 모델을 사용하여 기능을 구현해보자  
*박동호* : 웹에 대한 고민은 뒤로 레시피 데이터들을 베이스로 깔고 모델을 찾아 결과 도출하자  

#### 방향성 : 재료를 받아 음식 추천해주는 시스템

#### 고민점
- 재료를 인풋으로 받아 각 종 요리를 추천해주도록 __기술적으로 구현할 방안__ 고안!
1. 데이터 : 어떤 데이터를 사용할 건지
2. 모델 등등등...
