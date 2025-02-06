# 실용적인 테스트 가이드 

### 한 문단에는 한 주제의 테스트 코드를 작성하자.

### 현재 시간을 사용하지말고 고정된 시간을 사용하자. 
+ 환경에 따라 현재 시간이 다르면 영향을 받을 수 있다.

### 테스트 given 절은 정적 팩토리 메서드를 지양한다. 순수한 빌더 사용

### 공유 자원은 사용하지 말아야한다.

### 한 눈에 들어오는 Test Fixture을 구성하자. 

내가 모르는 given절이 있으면 안된다. 

**BeforeEach 사용 조건** 

+ 각 테스트 입장에서 봤을 때, 아예 몰라도 테스트 내용을 이해하는 데에 문제가 없는가? 
+ 수정해도 모든 테스트에 영향을 주지 않는가? 

### @Transactionl vs deleteAll vs deleteAllInBatch
 
+ @Transactionl은 사이드 이펙트가 있을 수 있기 때문에 유의해야 한다.
+ after절에서 delete하는 것은 순서에 영향을 받아 에러가 날 수 있다. 
+ deleteAll
  + 조회해서 하나씩 삭제 (건당 지움)
  + 다수의 쿼리 발생

