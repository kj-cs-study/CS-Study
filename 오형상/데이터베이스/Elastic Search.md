# Elastic Search

### 정의

> Apache Lucene(아파치 루씬) 기반의 java 오픈소스 분산 검색 엔진으로 방대한 데이터를 신속하고 거의 실시간으로 저장, 검색, 분석할 수 있습니다.
Elasticsearch는 검색을 위해 단독으로 사용되기도 하며, ELK( Elasticsearch / Logstatsh / Kibana )스택으로 사용되기도 합니다.
> 

### **ELK( Elasticsearch / Logstatsh / Kibana ) 스택**

- **ELK**는 분석 및 저장 기능을 담당하는 **ElasticSearch**, 수집 기능을 하는 **Logstash**, 이를 시각화하는 도구인 **Kibana**의 앞글자만 딴 단어입니다.
- ELK는 접근성과 용이성이 좋아 최근 가장 핫한 Log 및 데이터 분석 도구입니다.

**Elasticsearch :** Logstatsh로 부터 받은 데이터를 검색 및 집계를 하여 필요한 관심 있는 정보를 획득

**Logstatsh :** 다양한 소스(DB, csv파일 등)의 로그 또는 트랜잭션 데이터를 수집, 집계, 파싱하여 Elasticsearch 로 전달

**Kibana :** Elasticsearch의 빠른 검색을 통해 데이터를 시각화 및 모니터링

---

### Elastic Search의 인덱스구조 vs RDBMS의 인덱스 구조

Elastic Search는 Inverted-Index 구조로 데이터를 저장합니다. 이는 책의 색인을 생각해보면 쉬운데, 특정 단어가 출현하는 doc을 저장하는 것입니다. 반면 RDBMS는 B-Tree와 그와 유사한 인덱스를 사용합니다. 데이터가 어디에 존재하는지 어떤 순서로 저장하는 지의 차이라고 생각합니다. RDBMS에도 다양한 인덱스 구조가 있으나 여기서 예로 든 것은 B-Tree 인덱스입니다.

---

### Elastic Search의 키워드 검색 vs RDBMS의 LIKE 검색

#### Elastic Search 키워드 검색 
- 텍스트를 여러 단어로 변형하거나 텍스트 특질을 이용한 동의어, 유의어를 활용한 검색이 가능
- 비정형 데이터 검색 및 색인이 가능
- 형태소 분석을 통한 자연어 처리 가능
- 역색인 지원으로 매우 빠르게 검색

#### RDBMS LIKE 검색
- 단순 텍스트 매칭에 대한 검색만을 제공 (한글 검색의 경우 빈약)
- 비정형 데이터의 색인과 검색이 불가능

### 참고

[[Elasticsearch] 기본 개념잡기](https://victorydntmd.tistory.com/308)
