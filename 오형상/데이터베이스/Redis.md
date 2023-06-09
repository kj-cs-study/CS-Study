# Redis

## 정의

> **Remote(원격)** 에 위치하고 프로세스로 존재하는 In-Memory 기반의 **Dictionary(key-value)** 구조 데이터 관리 **Server** 시스템
>

## 특징

- NoSql DBMS(비관계형 데이터베이스)로 분류되며 In memory 기반의 Key - Value 구조를 가진 데이터 관리 시스템
- 메모리 기반이라 모든 데이터들을 메모리에 저장하고 조회에 매우 빠르다. (리스트형 데이터 입력과 삭제가 MySQL에 비해서 10배정도 빠름)
- 메모리에 상주하면서 서비스의 상황에 따라 데이터베이스로 사용될 수 있으며, Cache로도 사용될 수 있다.
- Remote Data Storage로 여러 서버에서 같은 데이터를 공유하고 보고 싶을 때 사용할 수 있다.
- 다양한 자료구조 를 지원한다. (Strings, Set, Sorted-Set, Hashes, List ...)
- 쓰기 성능 증대를 위한 클라이언트 측 샤딩(Sharding)을 지원한다.
    - Sharding : 같은 테이블 스키마를 가진 데이터(row)를 다수의 데이터베이스에 분산하여 저장하는 방법
- 메모리 기반이지만 Redis는 영속적인 데이터 보존(Persistence)이 가능하다. (메모리는 원래 휘발성)
- 스냅샷 기능을 제공해 메모리 내용을 *.rdb 파일로 저장하여 해당 시점으로 복구할 수 있다.
- 여러 프로세스에서 동시에 같은 key에 대한 갱신을 요청하는 경우, 데이터 부정합 방지 Atomic 처리 함수를 제공한다(원자성)
- Redis는 기본적으로 1개의 싱글 쓰레드로 수행되기 때문에, 안정적은 인프라를 구축하기위해서는 **Replication(Master-Slave 구조)Visit Website** 필수이다.