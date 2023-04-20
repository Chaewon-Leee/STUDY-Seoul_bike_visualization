# PROJECT-Seoul_bike_visualization

> [visualization 강의](https://github.com/Chaewon-Leee/TIL/tree/main/ML/Visualization) 수강 이후, 데이터에 대해 가설을 세우고 이를 시각화로 증명하고자 함

- **Data info**

  - 따릉이 (공공자전거) : [https://data.seoul.go.kr/dataList/OA-15245/F/1/datasetView.do#](https://data.seoul.go.kr/dataList/OA-15245/F/1/datasetView.do#)
  - 강수량 : [https://data.kma.go.kr/stcs/grnd/grndRnList.do?pgmNo=69](https://data.kma.go.kr/stcs/grnd/grndRnList.do?pgmNo=69)

- **Features**

  - 대여일자 : 일자
  - 대여시각 : 따릉이 대여할 때의 시각
  - 대여소번호 : 대여 장소 코드 번호
  - 대여소 : 따릉이를 대여한 장소
  - 대여구분코드 : 대여권
  - 성별 : 사용자의 성별
  - 연령대 코드 : 사용자의 연령대
  - 운동량 : 사용자의 운동량
  - 이동거리(M) : 따릉이로 이동한 거리
  - 사용시간(분) : 따릉이 사용시간

- **Hypothesis**

  1. 공유킥보드 규제 정책에 따라 따릉이 사용량이 영향 받을 것이다.
  2. 비가 오지 않는 날은 비가 오는 날보다 사용량이 더 많을 것이다.
  3. 주말의 경우, 일일권의 사용량이 더 많을 것이며, 평일의 경우 정기권의 사용량이 더 많을 것이다.
  4. 서울 지역 위치가 외곽일수록 평균 사용시간이 늘어날 것이다.
     - 4-2. 대여소 수가 적을수록 평균 사용시간이 늘어날 것이다.
  5. 대여소 위치에 따라 주되게 사용하는 연령대가 존재할 것이다.
     - 학교 주변은 10~20대가 가장 주되게 사용할 것
     - 공원 주변은 30~40대가 가장 주되게 사용할 것

- **After Seminar**
  |회고|내용|
  |:--:|:--|
  |방대한 데이터를 loading하거나 처리하는 방식|- 데이터를 직접 저장하는 것이 아닌 pickle을 사용하거나, for문 대신 내장함수를 사용한다는 등 전체적인 전처리 시간을 절약할 수 있었을 것 <br> - 또한, 함수화, 내장 함수 등에 익숙해질 필요가 있음|
  |가설 설정|- 대체적으로 예상 가능한 가설 <br>- EDA를 마친 이후, 가설을 세우는 것이 더 도움이 될 것|
  |스토리 텔링|- 전체적으로 가설 마무리가 되지 않음 <br> - 그래프의 결과물애 댜해 추가적인 분석 필요<br>- 오직 가설의 참 / 여부에 초점을 맞추는 것이 아닌, 그래프 결과 해석 및 분석 진행 <br>- ex, 1번 가설, 규제 여부가 아닌 계절의 영향을 받는 듯함 → 계절의 영향이 있는지 추가적인 분석 진행<br>- 질문, 의견이 들어올시 나의 견해를 잘 표현할 필요가 있음|
  |시각화 방식 선택|- 그래프 종류 선택, 사용해야하는 열 선택 등 아직 미숙함<br>- ex, 5번 가설 → 여러 map 지도를 만드는 게 아닌 따릉이의 사용량, 연령대, 위치를 묶어 색상, 크기 등을 달리하여 한 번에 비교가 가능하도록<br>- 현재는 다양한 그래프를 시도해보는데에 초점을 두었지만, 가설에 따라 적절한 그래프를 선택하는데에 집중할 필요가 있음|
