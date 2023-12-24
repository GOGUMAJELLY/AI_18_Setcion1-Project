# 개인 프로젝트 - 2018 게임 트렌드 분석
## 목차
> [프로젝트 목표](#프로젝트-목표)  
> [프로젝트 과정](#프로젝트-과정)  
> [프로젝트 결과](#프로젝트-결과)  
> [프로젝트 회고](#프로젝트-회고)  
## 프로젝트 목표
  - 1980 ~ 2017년도 게임 판매량 데이터 세트를 활용해 2018년도 제작할 게임의 장르, 판매 플랫폼, 판매 지역의 합리적인 인사이트를 도출
  - 기초적인 데이터의 전처리 방식 및 시각화의 능력 키우기
## 프로젝트 과정
### 데이터셋 분석
<table>
   <tr>
    <td>정제 전 데이터셋 : 총 16,598개의 데이터</td>
    <td>정제 후 데이터셋 : 총 16,240개의 데이터</td>
   </tr>
  <tr>
    <td><img width="700" alt="1980~2017 game data" src="https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/a0a39db9-1a74-4011-a99a-3c3fc72aa986"></td>
    <td><img width="700" alt="1980~2017 정제된 dataset" src="https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/d5cc4384-f610-4444-8661-1ba676961901"></td>
  </tr>
</table>

### 데이터 전처리 과정
  - 전체적인 결측치 제거 및 중복값 제거
  - 판매량의 단위는 M(1,000,000)으로 전부 변환
  - Total Sales 컬럼 생성(지역별 판매량이 아닌 전체 판매량을 확인하기 위함)
  - year 컬럼에서 nnnn 형식이 아닌 nn 형식으로 기입한 데이터 발견 → 전부 nnnn 형식으로 변경
  - year 컬럼에서 소수점이 붙어있음으로 제거후 int 타입으로 변경

### 데이터 시각화 과정
<table>
  <tr>
    <td>지역별 게임 장르의 판매 비율</td>
    <td>지역별 게임 장르의 판매량</td>
  </tr>
  <tr>
    <td><img src='https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/b660a72a-0901-4adb-819d-632bcb342209'></td>
    <td><img src='https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/1ee106e9-bed4-4735-a9f5-ce4387174d98'></td>
  </tr>
</table>

- 가장 먼저 Genre 컬럼을 활용해 어느 장르가 가장 인기가 있었는지 시각화 하여 비율 및 구체적인 수량을 확인함
<table>
  <tr>
    <td>장르와 판매량의 관계 검증</td>
  </tr>
  <tr>
    <td><img src='https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/c8668916-77f2-4932-acde-ff2afbd52d3e' width='480' height='320'></td>
  </tr>
</table>

- 장르와 판매량에 연관성이 있는지 한번더 확인하기 위해 통계적 검정 기법중 하나인 카이제곱 검정을 이용
<table>
  <tr>
    <td>2000년도 이후 장르의 트렌드</td>
    <td>2017년까지의 플랫폼별 판매 및 보급량</td>
  </tr>
  <tr>
    <td><img src='https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/235deab0-9952-4647-923c-d4d2a345adf6'></td>
    <td><img src='https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/40c4aa0c-67b6-4964-8f7a-2dd5fdd5ef86'></td>
  </tr>
</table>

- 2000년도 이후 가장 많이 팔린 1순위 장르를 시각화해 트렌드를 확인 및 장르의 인사이트를 확인
- 플랫폼 보급량을 확인해 어느 플랫폼에 맞춰 게임을 제작할지 인사이트 확인
<table>
  <tr>
    <td>가장 많이 팔린 제품 확인</td>
    <td>시리즈 총 판매량 비교</td>
  </tr>
  <tr>
    <td><img src='https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/a46fb004-1f11-48b7-a667-7c69457887fb' width='480' height='320'></td>
    <td><img src='https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/08e465a4-c550-4d1c-af1b-876a563491d4' height='320'></td>
  </tr>
</table>

- 가장 많이 팔린 게임을 확인했는데 2000년도 Action 장르가 가장 인기가 있었는데 Wii Sports가 가장 많이 팔린것이 의문이 들게 됨
- 데이터를 한번더 확인한 결과 하나의 제품으로만 파는것이 아닌 시리즈로 제품을 만들어서 팔기에 데이터로 확인이 어려웠던 이유를 확인
- 스포츠 장르에선 wii게임, 액션 장르에선 GTA게임이 시리즈로 가장 많이 팔린 제품들이여서 둘을 비교
- 결과 큰 차이로 액션장르인 GTA 판매량이 높은것을 확인함
## 프로젝트 결과
<img src='https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/83c2c1dd-08a6-4ca6-8230-9568cf0d529f' width='680' height='360'>
<table>
  <tr align=left>
    <td>지역</td>
    <td>플랫폼</td>
    <td>단일 제품</td>
    <td>시리즈 제품</td>
  </tr>
  <tr>
    <td>북 아메리카</td>
    <td>PS2 or X360</td>
    <td>Sports</td>
    <td>Action</td>
  </tr>
</table>

## 프로젝트 회고
- 문제 해결 과정
  - 퍼블리셔가 뭔지 플랫폼은 뭔지 모르는 내용이 있었다
    > 도메인 지식의 중요성을 알아서 구글 검색을 이용해 확인
  - EDA과정 중 연도에서 품질 오류가 있었는데 2015년이 아닌 15년으로 기입된 데이터 종류들이 많이 확인됨
    > 구글링 해서 같은 상황을 가진 자료가 많아 참고해 if문으로 해결
  - 판매수의 단위인 'K', 'M'이 섞여있는 문제
    > 정규표현식을 사용해 K → M 으로 변환해서 통일화
  - 시각화과정에서 어떻게 확인 및 표현할지 많은 어려움들이 있었음
    > seaborn, matplotlib의 document를 활용 및 검색해서 fig, ax 개념을 이용해 시각화 자료의 사이즈를 조절 및 가시성을 높임
- 아쉬운 점
  - 프로젝트 당시 def, for, if문을 제대로 이해하지 못해 코드를 너무 풀어서 썻다.
  - 왜 3개의 연도에서 스포츠 장르가 많이 팔렸는지, 많이 팔린 이유를 연도별 행사에 연관을 지을 수 있는지 고민함
    > 고민 후 가장 연관이 있을법한 올림픽이 관련이 있는지 확인을 하고 싶어 통계적 검정이나 접목시킬 방법이 있는지 확인 했는데  
    > 시간이 너무 끌려서 포기해서 아쉬웠음
  - 연도별 게임 판매량 중 장르별로 시각화한 자료를 한번더 확인 및 파악했으면 더 좋은 프로젝트가 되지 않았을까 생각이 듦
