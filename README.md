# 아파트너
## 서울시 아파트 매매가격을 예측하는 서비스

<div align=center><h1>📚 TOOLS</h1></div>

<div align=center> 
  <img src="https://img.shields.io/badge/Apache-D22128?style=for-the-badge&logo=Apache&logoColor=white"> 
  <img src="https://img.shields.io/badge/c++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white">
  <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white"> 
  <br>
  
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> 
  <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"> 
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> 
  <img src="https://img.shields.io/badge/jquery-0769AD?style=for-the-badge&logo=jquery&logoColor=white">
  <br>
  
  <img src="https://img.shields.io/badge/oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white"> 
  <img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> 
  <img src="https://img.shields.io/badge/mariaDB-003545?style=for-the-badge&logo=mariaDB&logoColor=white"> 
  <img src="https://img.shields.io/badge/mongoDB-47A248?style=for-the-badge&logo=MongoDB&logoColor=white">
  <img src="https://img.shields.io/badge/firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=white">
  <br>
  
  <img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=black"> 
  <img src="https://img.shields.io/badge/vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white"> 
  <img src="https://img.shields.io/badge/angular.js-DD0031?style=for-the-badge&logo=angularjs&logoColor=white">
  <img src="https://img.shields.io/badge/node.js-339933?style=for-the-badge&logo=Node.js&logoColor=white">
  <br>
  
  <img src="https://img.shields.io/badge/spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white"> 
  <img src="https://img.shields.io/badge/express-000000?style=for-the-badge&logo=express&logoColor=white">
  <img src="https://img.shields.io/badge/django-092E20?style=for-the-badge&logo=django&logoColor=white">
  <img src="https://img.shields.io/badge/flask-000000?style=for-the-badge&logo=flask&logoColor=white">
  <img src="https://img.shields.io/badge/flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white">
  
  <img src="https://img.shields.io/badge/bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white">
  <br>

  <img src="https://img.shields.io/badge/linux-FCC624?style=for-the-badge&logo=linux&logoColor=black"> 
  <img src="https://img.shields.io/badge/amazonaws-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white"> 
  <img src="https://img.shields.io/badge/apache tomcat-F8DC75?style=for-the-badge&logo=apachetomcat&logoColor=white">
  <br>
  
  <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
  <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
  <img src="https://img.shields.io/badge/fontawesome-339AF0?style=for-the-badge&logo=fontawesome&logoColor=white">
  <br>
</div>


###프로젝트 선정 이유
서울연구원 조사에 따르면 부동산 첫 매수로 서울로 선택하는 비율 증가 추세
서울시의 아파트는 자산 가치가 높고 변동성이 적은 안전자산이라서 매수자들에게 더 선호되는 경향으로 서울시 아파트 목적
서비스타겟:서울, 아파트, 30대 이상 중장년층
### 프로젝트 목적
‘아파트너’는 사용자가 원하는 정보를 검색할 수 있으며 지도를 통해 아파트 위치를 한눈에 알아볼 수 있습니다. 여기서 더 나아가 기존 서비스와의 차별점으로 각각 아파트마다 의료, 교통시설등 편의시설에 대한 거리를 단순수치뿐만 아니라 그래프로 시각화하여 한눈에 알아보기 쉽게 구현했습니다.
또한 LSTM 분석 모델을 활용해 개별 아파트의 향후 5개월 뒤 가격 예측 서비스까지 추가해서 아파트의 미래 전망을 쉽게 파악할 수 있도록 했습니다.

### 데이터 수집 및 전처리
분석에 필요한 아파트 가격에 영향을 주는 변수를 각 기준을 고려하여 설정하였습니다. 접근성이라는 면에서 다른 시설과의 거리데이터, 면적, 층과 같은 아파트의 구조 데이터를 중점으로 두었습니다.
좌표 형태인 편의시설 데이터를 아파트와의 최단 거리로 변환하였습니다.
아파트와 유치원의 좌표값 데이터를 불러온 뒤에 거리를 구하는 하버사인 공식에 대입하여  값을 구했습니다.아파트 주변에 위치한 유치원 중에서 최단거리에 있는 것을 기준으로 설정하여 거리 값을 데이터에 저장했습니다. 다른 편의시설의 거리 변수도 같은 방식을 사용했습니다.
분석이 가능하도록 분양형태나 시공사 이름과 같은 범주형 문자 데이터를 연산이 가능한 숫자형 데이터로 변환했습니다.

### 분석모델선정 및 예측
1.분석 모델은 다양한 시계열 예측 방법 중 가장 예측 성능이 좋았던 LSTM과 GRU를 고려하였으며, 그 중에서 더 높은 예측을 보인 LSTM 모델을 사용했습니다.
LSTM은 RNN의 단점을 보완한 시계열 예측 모델입니다. 개별 아파트의 거래빈도는 다른 재화들처럼 활발하지 않다는 점 때문에 학습데이터가 부족했습니다. 이를 보완하기 위해서  특정 아파트는 더 큰 규모의 아파트 가격에 영향을 받는다고 가정했습니다. 아파트반경 2킬로미터 내의 더 큰 규모의 아파트를 묶어 학습데이터로 사용했습니다. 
그리고 민맥 스케일링을 사용하여 정규화한 뒤, 과거데이터를 3개월씩 사용하여 모델을 학습하도록 했습니다. 아파트별로 모델을 생성하고 미래의  값을 예측하였습니다.
2.예측
아파트 미래가치를 예측하기 위해 최근 시점인 7월부터 1개월씩 추가하면서 반복적으로 학습시켰습니다. 그리고 면적별 아파트를 그룹별로 묶어서 예측된 가격을 데이터베이스로 만들었습니다.

### 크롤링
아파트에 대한 정량적 정보와 정성적 정보를 포함하기 위해  뉴스 기사를 웹스크래핑 했습니다. 해당 아파트명이 포함된 최근 네이버 뉴스 기사의 제목과 주소를 아파트 정보페이지에 포함시켰습니다. 
그리고 뉴스의 내용 중에 키워드만 추출해서 워드클라우드로 구현했습니다.

### 웹페이지 구현
먼저 전처리한 데이터와 예측 데이터를 MySQL을 이용해 데이터베이스로 구축하였습니다.
구축한 데이터베이스는 PHP를 이용하여 웹 페이지와 연동하였고  json형태로 바꾸어 자바스크립트 언어에서 사용할 수 있도록 설정하였습니다.
불러온 데이터를 바탕으로 api를 이용해 웹 서비스를 구현하였습니다.

### 서비스 설명
‘아파트너’ 웹페이지에서 아파트명을 검색하거나 직접 지도에서 탐색할 수 있습니다.
마커 클러스터링 기능을 추가하여  알아 보기 쉽게 디자인하였습니다. 원하는 지역의 아파트의 정보를 클릭만으로 빠르게 조회할 수 있도록 하였습니다.
그리고 검색창을 이용해서도 아파트 정보를 조회할 수 있습니다. 예를들어 검색창에  ‘현대’를 검색하면 다음과 같이 ‘현대’라는 단어가 포함된 아파트명과 주소가 출력됩니다. 그리고 지도의 화면은 ‘현대’가 포함된 아파트만 마커가 표시되며 마커에 커서를 올리면 아파트명이 표시 됩니다.
원하는 아파트 이름이나 마커를 클릭하면 해당 아파트의 정보를 조회할 수 있는 페이지로 이동합니다. 전체적인 정보를 한눈에 확인할 수 있도록 구성하였으며 크게 세 갈래로, 왼쪽면에 아파트 정보, 중앙에는 해당 아파트의 10년간 가격 변동 그래프와 주변시설 근접도 그래프를 배치하여 정량적 데이터를 표현했습니다. 마지막으로 오른쪽면에는 크롤링을 통해 수집한 해당 아파트 관련 기사와 워드 클라우드를 배치하여 정성적 자료를 함께 확인할 수 있도록 하였습니다.'예측가격서비스' 팝업창에서는 해당 아파트 단지의 미래가치를  LSTM으로 예측한 향후 5개월간의 평형별로 아파트 예측가가 그래프로 시각화되어 있습니다.

### 기대효과
1. 부동산의 가격 전망을 미리 예측함으로써 합리적인 주거 혹은 투자 목적을 위해 이 서비스를 활용
2. 부동산을 직접 방문하지 않아도 비전문가도 쉽게 서비스에 접근하여 부동산 정보 활용가능
3. 사용자가 선호하는 주택 특성에 따라 맞춤형으로 서비스를 이용

###발전방향
이에 그치지 않고 대상을 서울뿐만 아니라 전국으로 범위를 확장시키고 매매와 함께 전월세 정보도 포함시킨다면 이용자의 스펙트럼을 넓힐 수 있습니다. 또한 많은 데이터를 수집하고 사용을 거치면 더 정교한 분석 서비스를 제공할 수 있을 것입니다.

