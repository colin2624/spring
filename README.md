# spring

아래 예제는 db에 테이블을 만들 때 사용한다.

```kotlin
CREATE TABLE WORDCOUNT (
    WORD VARCHAR(100) NOT NULL,
    CNT INT(11) DEFAULT NULL,
    PRIMARY KEY('WORD')
)
```
키값이란건 중복되지 않는 값.

```kotlin
SELECT *
    FROM WORDCOUNT
```
테이블에서 데이터를 읽을 떄 사용한다. 예를 들면

```kotlin
SELECT *
    FROM WORDCOUNT
    VALUE('코틀린', 1)
```
테이블에 데이터를 넣을 떄 사용한다.

```kotlin
UPDATA WORDCOUNT
    SET CNT = CNT + 1
  WHERE WORD + '코틀린'
```
테이블에 이미 들어가 있는 데이터를 변경할때 사용한다.

```kotlin
DELETE FROM WORDCOUNT
 WHERE WORD = '코틀린'
```

