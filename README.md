# ELK_Project

## 미니 프로젝트 
- 2020년 부터 2023년 9월 4일 까지의 데이터를 활용하여 데이터 시각화 대시보드 만들기

### 데이터 내용
- 2020년 2월 17일 부터 2023년 9월 4일까지의 코로나 확진자, 사망자, 격리해제 데이터

### 프로젝트 구상 
- Filebeat로 위에서 만든 csv 파일을 읽어 Logstash로 보내고, Logstash에서 필터링 후 Elasticsearch로 인덱싱을 하면, Kibana에서 연결된 Elasticsearch의 데이터를 읽어서 대시보드를 만들 것이다. 우선 설치부터 하고 각 설정들은 순서대로 살펴 가며 세팅해 보자. 설명을 하기 전에, 간단하게 Elasticsearch는 데이터 저장소, Logstash는 파이프라인(읽고 → 필터링해서 → 보낸다), Filebeat는 file의 내용 변화를 체크해서 변경 분을 수집, Kibana는 데이터를 시각화하는 툴이라 생각하면 된다.

### 최종 대시보드 
<img width="1702" alt="스크린샷 2024-04-30 오후 7 08 07" src="https://github.com/stfano/ELK_Project/assets/57385696/4d116452-7172-41cf-a8fa-4f9f6eedd1b4">

<img width="1710" alt="스크린샷 2024-04-30 오후 7 08 33" src="https://github.com/stfano/ELK_Project/assets/57385696/5e326cd1-aa33-4b20-acf6-f9cd0309f452">

