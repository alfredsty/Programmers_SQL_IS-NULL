# Programmers_SQL_IS-NULL
* 사이트명 : 프로그래머스(Programmers)
* SQL : Oracle
* 난이도 : 하
## 문제 설명
<img width="522" alt="image" src="https://user-images.githubusercontent.com/102028778/159735880-3e0eba1d-08b9-4953-b492-da2475404def.png">

| NAME | TYPE | NULLABLE |
|------|------|------|
| ANIMAL_ID | VARCHAR(N) | FALSE |
| ANIMAL_TYPE | VARCHAR(N) | FALSE |
| DATETIME | DATETIME |FALSE|
| INTAKE_CONDITION | VARCHAR(N)| FALSE |
| NAME|VARCHAR(N) | TRUE| 
| SEX_UPON_INTAKE | VARCHAR(N) | FALSE | 
## * 이름이 없는 동물의 아이디
<img width="533" alt="image" src="https://user-images.githubusercontent.com/102028778/160147125-32d5e24b-b244-412c-b214-3bc6faba3160.png">
### 설명

### 답안
> SELECT ANIMAL_ID
FROM ANIMAL_INS
WHERE NAME IS NULL
ORDER BY ANIMAL_ID;

## 이름이 있는 동물의 아이디
<img width="901" alt="image" src="https://user-images.githubusercontent.com/102028778/160149145-13e4e99f-3e7c-4a30-bbbc-b1ca067158ad.png">
### 설명

### 답안
> SELECT ANIMAL_ID 
FROM ANIMAL_INS 
WHERE NAME IS NOT NULL
ORDER BY ANIMAL_ID ASC;
## NULL 처리하기
<img width="947" alt="image" src="https://user-images.githubusercontent.com/102028778/160149306-f222b7b3-da1f-4cb9-a780-c901eebde470.png">
### 설명

### 답안
> SELECT ANIMAL_TYPE, NVL(NAME,'No name') AS NAME, SEX_UPON_INTAKE
FROM ANIMAL_INS
ORDER BY ANIMAL_ID;
