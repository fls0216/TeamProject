# TeamProject
## 0928 회의록
### 안건 : 주제 선정 및 자료 수집
#### 회의내용
##### 1. 주제 선정 

박동민, 이상준 : 현 정치, 군사적 상황 속 국방 및 정치적 이슈를 활용한 주제 탐색 

이혜린 : DACON 심리 성향 예측 AI 공모전과 최종 프로젝트를 함께 준비 제안 -> 주제 선정 완료

차노을 : 유통관련 데이터 분석 프로젝트 제안

류시호(조장) : 전체적인 의견 수렴 및 조율, 주식 데이터를 활용한 데이터 분석 및 예측


##### 2. 자료 수집
DACON 데이터 활용 예정


##### 3. 회의 결과
프로젝트에 맞게 공모전을 진행하는 아이디어 회의 필요
  1. 웹페이지에 팀이 진행한 테스트를 포함하여 각종 심리 테스트를 업로드, 활용할 수 있게 한다.
  2. 웹페이지를 통해 방문자들이 팀이 진행한 테스트를 경험해볼 수 있도록 한다. (분석한 변수 입력)
  
프로젝트 분업화
  1. 중간 프로젝트 부동산 실거래가 분석 심화 (류시호, 박동민, 이상준)
  2. 심리 성향 예측 프로젝트 전처리 (이혜린, 차노을)
      - 데이터 기본 정리 완료
      - null값 확인, 이상값 확인 

##### 4. 프로젝트 진행 계획표 작성 (목표)
###### 09/28 주제 선정
###### 10/02 심리 예측 전처리    , 부동산 예측 머신러닝/딥러닝 공부
###### 10/05 심리 예측 시각화    , 부동산 예측 딥러닝 모델링
###### 10/12 심리 예측 분석
###### 10/16 심리 예측 플랫폼
###### 10/20 프로젝트 완료
###### 10/22 PPT/마무리
###### 10/23 발표


## 1001 회의록 (참여 팀원 : 이혜린, 차노을)
### 안건 : 전처리 진행상황 정리 및 계획
#### 회의내용
##### 1. 전처리 진행상황
이상값 확인 : 숫자형 D = box plot, 막대 그래프 확인 , 문자형 D = 범주 외 값  확인
  -> 혜린 노을 전처리 회의록에 추가
  
  
##### 2. 계획
  (1) 무응답 처리 
education : 교육 수준
1=Less than high school, 2=High school, 3=University degree, 4=Graduate degree, 0=무응답

engnat : 모국어가 영어
1=Yes, 2=No, 0=무응답

hand : 필기하는 손
1=Right, 2=Left, 3=Both, 0=무응답

married : 혼인 상태
1=Never married, 2=Currently married, 3=Previously married, 0=Other

urban : 유년기의 거주 구역
1=Rural (country side), 2=Suburban, 3=Urban (town, city), 0=무응답


   (2) 성별 또는 연령별로 어떤 응답이 많은지 등등 특이사항 확인하기
   
   
## 1002 회의록 (참여 팀원 : 이혜린, 차노을)  
### 안건 : 전처리 미완성 부분 확인 및 계획
#### 회의내용
##### 1. 전처리 진행상황
전처리 미완성 요인 분석하기 : 
education : 교육 수준, engnat : 모국어가 영어, hand : 필기하는 손 -> 이혜린

familysize : 형제자매 수, wr_(01~13) : 실존하는 해당 단어의 정의을 앎, wf_(01~03) : 허구인 단어의 정의를 앎 -> 차노을

##### 2. 전처리 완료된 부분 처리건
  (1) Q_E : box plot
    응답의 차이가 매우 커서 boxplot을 그리면 box가 선으로 보일 정도로 작음
    
   굉장히 차이가 나는 값들을 최대값 기준을 정해 대체하는 방법, 삭제 하는 방법, 새로운 방법 중 어떤 방법을 쓸 지 고려 필요
   
   -> 비대면으로는 진전이 없음. 다음주에 만나서 생각해보기로 함

##### 3. 계획
  (1) 무응답 처리 
education : 교육 수준
1=Less than high school, 2=High school, 3=University degree, 4=Graduate degree, 0=무응답

engnat : 모국어가 영어
1=Yes, 2=No, 0=무응답

hand : 필기하는 손
1=Right, 2=Left, 3=Both, 0=무응답

married : 혼인 상태
1=Never married, 2=Currently married, 3=Previously married, 0=Other

urban : 유년기의 거주 구역
1=Rural (country side), 2=Suburban, 3=Urban (town, city), 0=무응답



   (2) 상관/ 연관분석
   
   성별 또는 연령별로 어떤 응답이 많은지 
   
   Q_E와 Q_A  
   
   Q_E와 교육수준 등 연관있는지 등등 특이사항 확인하기
   
   
## 1005 회의록 (참여 팀원 : 이혜린, 차노을)  
### 안건 : 전처리 결과 확인 및 추가 사항 논의
#### 회의내용
##### 1. 전처리 결과공유
##### 2. 전처리 요인별 추가 사항 논의 결과
  (1) 노을
 
 
[married] Other 93개 -> 1=Never married 로 흡수


[age_group] 50대이상 작년 투표 1 비율 많음. 50대 이상을 한 묶음으로 그룹화


[wf_]							
허구인 단어를 안다-> 거짓응답일 가능성이 높음
셋 중 하나라도 1을 답했느냐 아니냐로 분류 가능 (컬럼하나 더 생성 , 1: 있다, 0 :없다)


[wr_]							
'wr_03','wr_06','wr_09','wr_11' : 0 > 1
이 중 2개 이상 1이라고 답했냐 아니냐로 분류 후 (컬럼하나 더 생성 , 1: 있다, 0 :없다) 


[education]					
high 이상 , 이외 로 분류


[tp__(01~10)]					
-> 0,1 그룹, 2-5 그룹, 6-7 그룹



(2) 혜린


[Q_E]							
-> 절대적 수치에 신경 x , 일정한 기준을 잡아 오래걸렸다 아니다 등으로 판단
25%까지 : 짧다, 25-75 : 보통, 75 이상 : 길다


[urban] (중요 변수라고 판단)					
백인으로 흡수한 (컬럼  만들어 놓기)


[race]							
백인 흑인 아시안 을 제외하고는 한 묶음으로 묶어도 괜찮을 것 같음   


[familysize]					
1인가구,
2인가구,
3인가구,
4인가구,
5인이상가구
15인 초과 가구 -> 2인가구로


[engnat]						
무응답 77   영어 으로 분류해도 괜찮을 것 같음


[hand]						
무응답 오른손잡이

## 1006 회의록 (참여 팀원 : 이혜린, 차노을)
### 안건 : 전처리 마무리 중
#### 회의내용
##### 1. 전처리 마무리
tp //혜린   
  -> 각 항목이 반대되는 성향으로 구성되어있다고 가정. 대표 성향 1가지를 추출하여 새로운 컬럼 생성    
     수치로 계산하여 가장 차이가 많이 나는 항목을 대표 항목으로 선정   
Q_E // 노을   
  -> 각 항목별 전체 평균을 산출하여 평균보다 높은 항목을 대표 항목으로 산출, 새로운 컬럼을 생성한다.   
     모든 항목별로 동일 기준을 산출하여 각각 비교함.    
  -> 행별로 개수가 가장 많은 항목을 선정하여 대표 항목으로 선정   
     같은 개수의 항목이 있을 경우 고려해보기.          //혜린 대신 해줌 (ㄱㅅㅠㅠ)
=> 10/7(수)까지 완료

##### 2. 상관/ 연관분석 
요인(Q_E와 교육수준 등)끼리의 연관
=> 10/7(수) 회의+공부 (같이 한두개 돌려보기)
  10/8(목) 완료 (분업)

요인 하나하나 별로 voted 연관 (one-hot 인코딩)
=> 주말 내내

요인을 합쳐서 ( 여+10대 )
=> ~화

최종 요인 선택 -> 여러번 분석 돌리기
=> 수목금

토일 - > pj 완료하기
 
 
## 1007 회의록 (참여 팀원 : 이혜린, 차노을)
### 안건 : 전처리 마무리
#### 회의내용
##### 1. 전처리 마무리 완료
(1) tp : tp 원래 데이터와 tp 둘 다 각각 분석 툴에 넣어보기

(2)Q_E

  2-1) 각 항목별 전체 평균을 산출하여 평균보다 높은 항목을 대표 항목으로 산출, 새로운 컬럼을 생성한다.   
    =- 평균보다 높은 항목이 2개 이상인 행이 3분의 1이 넘음. 무의미함!  
  2-2 ) 행별로 개수가 가장 많은 항목을 선정하여 대표 항목으로 선정   //선택

##### 2. 상관/ 연관분석 
요인(Q_E와 교육수준 등)끼리의 연관
=> 10/8(목) 회의+공부 (같이 한두개 돌려보기) + (one-hot 인코딩) 공부 + (주말에 할) voted 연관 요인 분류
  10/9(금) 완료 (분업)
  

요인 하나하나 별로 voted 연관 (one-hot 인코딩)
=> 주말 내내

요인을 합쳐서 ( 여+10대 )
=> ~화

최종 요인 선택 -> 여러번 분석 돌리기
=> 수목금

토일 - > pj 완료하기  



## 1012 회의록 (전 팀원 참여)
### 안건 : 요인정리 마무리
#### 회의내용
##### 1. 전처리 상황 공유

1.	전처리 안된 원래 데이터에서 other 대답끼리 공통점이 있는 지 , 있다면 vote와 연관 있는 지 등 체크 확인
무응답이 있는 요인  : education engnat hand married race religion urban



2.	age_group	:	연령
기준 나눠서 돌려보고 점수 높은거 선택하기
원 데이터 / 노을혜린 데이터 / 
	10,20/ 3,4,50 /6070
	10,20/ 3,40 /50 ,6070
	10/ 20 30 /40 50 /60 70



3.	familysize	:	형제, 자매 수
	15초과를 other로 묶어 소 중 대로 구분한 컬럼 만들기
  
  
4.	religion		:	종교
	종교 ox
	무교 / 크리스찬~+유대 / 무슬림 /힌두 +시크+불 /나머지 



5.	urban		:	고향(유년기에 살았던 곳)
	other를 근교로 넣은 상태에서 - > 도시 + 근교 / 시골


Q_E			:	테스트 질문까지 걸린 시간
tp_		:	본인이 생각하는 성향
	어떻게 처리할 지 다시 회의



##### 2. 업무 분담
1.   전처리 안된 원래 데이터에서 other 대답끼리 공통점이 있는 지 , 있다면 vote와 연관 있는 지 등 체크 확인		//동민



2. 10,20/ 3,4,50 /6070 (0,1,2 그룹나누기만 열 이름 : age1)
3. 10,20/ 3,40 /50 ,6070 (0,1,2 그룹나누기만 열 이름 : age2)		//혜린         
(초반부에 했던 10/20/30/40/50~ 를 age3로 변경!)


4.	10/ 20 30 /40 50 /60 70 (0,1,2,3 그룹나누기만 열 이름 : age4)		//시호


5.	종교 ox (0,1 그룹나누기 , 열이름 : religion_ox)
6.	무교 / 크리스찬~+유대 / 무슬림 /힌두 +시크+불 /나머지 (0,1,2,3,4 그룹나누기 , 열이름 : religion_siho)			//상준


7.	 urban other를 근교로 넣은 상태에서 - > 도시 + 근교 / 시골 (0,1 그룹나누기 urban_group)		//노을


##### 3. 계획
Q_E			:	테스트 질문까지 걸린 시간, tp_		:	본인이 생각하는 성향

어떻게 처리할 지 다시 회의
  
간단하게 모델 돌려 요인 선택 



  
