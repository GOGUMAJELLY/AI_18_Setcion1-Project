# 개인 프로젝트 - 2018 게임 트렌드 분석
## 목차
> [프로젝트 목표](#프로젝트-목표)  
> [프로젝트 과정](#프로젝트-과정)  
> [프로젝트 결과](#프로젝트-결과)  
> [프로젝트 회고](#프로젝트-회고)  
## 프로젝트 목표
  - 2018년도 까지의 게임 판매량 데이터를 활용해 2019년도 제작 할만한 게임의 장르, 판매 플랫폼, 판매 지역을 선정
## 프로젝트 과정
### 데이터셋 분석
<table>
  <td>정제 전 데이터셋 : 총 16,598개의 데이터</td>
   <tr>
     <td><img width="700" alt="1980~2017 정제된 dataset" src="https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/d5cc4384-f610-4444-8661-1ba676961901"></td>
   </tr>
  <td>정제 후 데이터셋 : 총 16,240개의 데이터</td>
  <tr>
    <td><img width="700" alt="1980~2017 game data" src="https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/879da321-efa1-4357-b05e-6b947dde5d74"></td>
  </tr>
</table>

### 데이터 전처리 과정
  - 전체적인 결측치 제거 및 중복값 제거
  - 판매량의 단위는 M(1,000,000)으로 전부 변환
  - Total Sales 컬럼 생성(지역별 판매량이 아닌 전체 판매량을 확인하기 위함)
  - year 컬럼에서 nnnn 형식이 아닌 nn 형식으로 기입한 데이터 발견 > 전부 nnnn 형식으로 변경
  - year 컬럼에서 소수점이 붙어있음으로 제거후 int 타입으로 변경
### 데이터 시각화 과정(자세한 시각화 자료는 PPT 확인)
  - 가장 판매량이 높은 3지역은 따로 시각화 하고 다른 지역은 전부 합쳐서 판매량 시각화
  - 맨 처음으로 어떤 장르가 가장 많이 팔렸는지 비율 시각화
  - 이후 어느 지역이 게임을 가장 많이 구매하는지 비율 시각화
  - 비율로는 정확히 알기 어려움으로 상세한 수치로 시각화
  - 프로젝트 중 의문점이 생김 : 그렇다면 게임의 장르와 판매량에 유의미한 관계가 있는가?
      - 가설검정을 실행해서 실질적인 관계를 파악하기로 함
      - 카이제곱을 이용해서 확인한 결과 장르와 게임 판매량은 연관이 있다.
  - 최종 확인으로 지역별 선호하는 장르를 정리해서 ppt에 기입 ( 북아메리카는 세계 시장의 49%를 장학하고 액션,스포츠,슈팅 장르를 선호함)
  - 그러면 각 지역별 선호 게임 장르는 시대상을 반영하는지 확인히 하고 싶어져 시각화
  - 수집한 데이터셋은 1980~2017년의 게임 판매량을 가진 데이터 셋이라 약 37년밖에 확인이 불가하지만 확인하기로 결정
  - 2000년도 전에는 각 장르들이 큰 차이가 없이 선호되어 왔지만 2000년 이후를 기점으로 액션 장르가 가장 선호되고 그 후로 스포츠 장르가 선호됨
    - 이 과정에서 과연 2000, 2006, 2009년도에 스포츠 장르가 1위로 급부상 하는데 그 이유를 찾으려함
    - 올림픽이 상관있지 않을까 싶어 올림픽 데이터셋을 찾아봄
    - 올림픽 데이터셋과 비교할려 했지만 시간을 너무 잡아먹어 이 과정은 하지 않기로 결정
  - 연도별 플랫폼 보급량도 시각화 시작
  - 대표적인 5개의 플랫폼은 PS2, X360, PS3, Wii, DS 순서로 보급이 되어있음.
    - 그렇다면 지역별 플랫폼 보급량도 확인
  - 지역별 선호 장르, 플랫폼의 보급율 확인을 하였으니 단일 제품중 가장 많이 팔린 제품을 확인
  - 윌 스포츠가 압도적으로 1위였다.
    - 왜 스포츠 게임이 압도적인지? 2000년대 이후 액션 장르가 가장 선호하는 장르였는데 단일 제품인 wii Sports인 스포츠 장르가 가장 판매량이 높음
  - 액션 장르의 게임중 전체 판매량을 기준으로 데이터셋을 다시 확인해봄
    - 확인해 보니 wii 게임은 시리즈가 아닌 한 제품만으로 팔아서 압도적인 1위였고
    - 액션 장르중 GTA 제품들이 많이 팔렸는데 시리즈가 매우 많아서 단일 제품으로는 wii Sports가 압도적인 사실인걸 확인함
    - 각 시리즈 총 판매량을 확인했는데 GTA 시리즈가 2천만장 더 많이 팔림
  - 이제 장르, 플랫폼, 지역, 단일제품 기준 판매량 을 확인해 2019년 제작하기에 적절한 게임을 결과로냄
## 프로젝트 결과
![결과](https://github.com/GOGUMAJELLY/AI_18_Setcion1-Project/assets/60537140/a2b548cc-9202-448f-8633-4eecf468955a)

## 프로젝트 회고
- 개인 프로젝트 당시 def문, for문을 제대로 이해하지 못해 코드를 너무 풀어서 썻다.
- 왜 3개의 연도에서 스포츠 장르가 많이 팔렸는지 연관 지을만한 올림픽 데이터를 어떻게 적용할지 어려워서 못한것이 아쉽다.
- 연도별 게임 판매량 중 장르별로 시각화한 자료를 좀더 다듬었으면 어땠을까 싶다.
