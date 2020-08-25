XOR 변환기

1. COMMAND
 - cat encrypted.txt | python xor.py "key" > result.txt
 - encrypted.txt도 hex이고, key도 hex이다.
 - 결과값을 result.txt에 저장한다.

2. encrypted.txt
 - 여기는 hex로 변환된 데이터가 들어가야 한다.
 - "I want the cookie." 등의 값이 들어가면 올바른 결과가 나오지 않는다.
 - 이 string을 변환한 hex 값인 "49 20 77 61 6e 74 20 74 68 65 20 63 6f 6f 6b 69 65 73 2e"를 올바르게 인식한다.

3. key
 - hex 값을 인식하기 위해선 echo -e를 사용한다.
  ex) cat encrypted.txt | python xor.py "echo -e '\w61\w61\w61'"
  
