# HappyHouse_Java
### 아파트 거래 정보 GUI 구현

![ezgif com-gif-maker (1)](https://user-images.githubusercontent.com/54715744/127612321-2b56eadb-d79b-44f8-becf-6c8798842773.gif)

2019년 12월 서울 종로구 아파트/주택 별 매매 및 전/월세 거래내역

### 구현 기능
* 화면 UI 를 통해서 원하는 주택 정보를 검색
* 동 또는 아파트를 선택 후, 검색어로 조회 가능
* 아파트 매매, 아파트 전월세, 주택 매매, 주택 전/월세로 구분하여 선택 가능

### 구현 클래스
* **HouseInfo**
  * 주택 정보에 관한 기본데이터 (아파트 식별 번호, 법정 동명, 아파트 이름, 법정 동 코드,  건축 연도, 지번, 이미지 경로)
* **HouseDeal**
  * 주택 거래정보 (거래 식별 번호, 법정 동명, 아파트 이름, 법정 동 코드, 거래 금액, 건축 연도, 거래 연도, 거래 월, 거래 일, 전용 면적, 층, 지번, 거래 타입, 월세)
* **HouseSAXHandler**
  * AptInfo.xml 파일에서 아파트 정보를 읽어 Parsing 하는 Handler
  * Map 형태의 주택 정보 제공
* **HouseDealSAXHandler**
  * HouseDealHistory.xml 파일의 다세대, 주택 매매 정보를 분석하여 List 로 제공
* **HouseRentSAXHandler**
  * HouseRentHistory.xml 파일의 다세대, 주택 전/월세 정보를 분석하여 List 로 제공
* **AptDealSAXHandler**
  * AptDealHistory.xml 파일의 아파트 매매 정보를 분석하여 List 로 제공
* **AptRentSAXHandler**
  * AptRentlHistory.xml 파일의 아파트 전/월세 정보를 분석하여 List 로 제공
* **HouseSaxParser**
  * 모든 Handler 클래스를 활용해 추출한 주택 기본 정보와 주택 거래 정보를 병합한 결과 제공
* **HouseDaoImpl**
  * XML 문서를 파싱하여 만들어진 House 객체에 데이터를 저장하고 관리
* **HouseServiceImpl**
  * HouseDaoImpl 클래스의 searchAll(HousePageBean bean) 를 호출하여 얻은 데이터 리턴
---
### Contributor
* 강바울
* 이지우
