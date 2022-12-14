## Feature List
1. 문제 요구사항 파악
    + forms는 이중 리스트다. 각 인덱스에는 사이즈가 2인, 이메일, 닉네임으로 구성된 리스트가 있다.
    + 유저들의 닉네임은 두 글자이상 연속적으로 중복되서는 안 된다. -> 유저는 1이상 10,000명 이상이란 것을 항상 생각해야 한다.
    + 이때, 닉네임이 중복된 유저들의 이메일을 담는 result에는 이메일이 중복되지 않으며, 오름차순 정렬한다. -> distinct()와 sort() 사용

2. 예외 처리
    + 제한 사항 외에 문제가 될만한 예외는 없을 것으로 보임

3. 함수 - 2개
    1. 유저 닉네임들을 문자열 하나에 모두 담아주는 함수 setUserNickname(): String 
    2. 유저 수만큼(List size만큼) for문을 돌며, 해당 인덱스의 유저 닉네임이 중복됐는지 chek 함수 checkDuplicateString(): Boolean
        + 이때, 매개변수로 모든 유저들의 이름을 담은 문자열 하나와, 탐색할 유저 닉네임 받음

4. 접근 방법
    + rowString 변수에 모든 유저들의 이름을 구분자 '_' 로 다 넣고, check 함수에서 해당 인덱스의 닉네임이 중복되는지 check

---
## 문제

## 🚀 기능 요구 사항

우아한테크코스에서는 교육생(이하 크루) 간 소통 시 닉네임을 사용한다. 간혹 비슷한 닉네임을 정하는 경우가 있는데, 이러할 경우 소통할 때 혼란을 불러일으킬 수 있다.

혼란을 막기 위해 크루들의 닉네임 중 **같은 글자가 연속적으로 포함** 될 경우 해당 닉네임 사용을 제한하려 한다. 이를 위해 같은 글자가 연속적으로 포함되는 닉네임을 신청한 크루들에게 알려주는 시스템을 만들려고 한다.


신청받은 닉네임 중 **같은 글자가 연속적으로 포함** 되는 닉네임을 작성한 지원자의 이메일 목록을 return 하도록 solution 함수를 완성하라.

### 제한사항

- 두 글자 이상의 문자가 연속적으로 순서에 맞추어 포함되어 있는 경우 중복으로 간주한다.
- 크루는 1명 이상 10,000명 이하이다.
- 이메일은 이메일 형식에 부합하며, 전체 길이는 11자 이상 20자 미만이다.
- 신청할 수 있는 이메일은 `email.com` 도메인으로만 제한한다.
- 닉네임은 한글만 가능하고 전체 길이는 1자 이상 20자 미만이다.
- result는 이메일에 해당하는 부분의 문자열을 오름차순으로 정렬하고 중복은 제거한다.

### 실행 결과 예시

| forms | result |
| --- | --- |
| [ ["jm@email.com", "제이엠"], ["jason@email.com", "제이슨"], ["woniee@email.com", "워니"], ["mj@email.com", "엠제이"], ["nowm@email.com", "이제엠"] ] | ["jason@email.com", "jm@email.com", "mj@email.com"] |



