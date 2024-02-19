

## 문제 #1  **브론즈4**

[**링크**](https://www.acmicpc.net/problem/2752)

![img](https://prod-files-secure.s3.us-west-2.amazonaws.com/74553f09-e822-477e-abed-c52903d69b9f/ae981fb5-79d7-4578-84f2-bb73b2022bc6/Untitled.png)

- 해설 #1
    
    !https://velog.velcdn.com/images/banghogu/post/ecc6a18b-d24e-48d4-8d49-3e8310decf61/image.png
    
    배열에 숫자를 담고 오름차순 해주었다. 문자열을 출력 할 때 일일이 console.log 하는 것이 아니라 항상 answer = '' 빈 문자열을 만들어서 추가해야 효율적이다.
    

---

## 문제 #2 브론즈2

[링크](https://www.acmicpc.net/problem/2750)

![img](https://prod-files-secure.s3.us-west-2.amazonaws.com/74553f09-e822-477e-abed-c52903d69b9f/66ebc679-5c19-42fc-9e45-1f3eb7b05fbb/Untitled.png)

- 해설 #2
    
    !https://velog.velcdn.com/images/banghogu/post/94fa6a7d-0e3e-425d-94ae-e7920543fc71/image.png
    
    문제 1과 똑같이 오름차순 해주었다
    

---

## 문제 #3 실버2

[링크](https://www.acmicpc.net/problem/18870)

![img](https://prod-files-secure.s3.us-west-2.amazonaws.com/74553f09-e822-477e-abed-c52903d69b9f/bfbaa91a-8e8f-4981-b53d-4aca0261663b/Untitled.png)

- 해설 #3
    
    ![img](https://prod-files-secure.s3.us-west-2.amazonaws.com/74553f09-e822-477e-abed-c52903d69b9f/71e06e89-02b7-4c40-83f5-a87dc12d7b72/Untitled.png)
    
    **접근법** : 처음에는 반복문으로 현재 인덱스 보다 큰 값이 있을시 카운트를 증가시켜 카운트값을 배열에 넣는거라고 생각했는데 1 ≤ N ≤ 1,000,000의 범위를 가지고 있기 때문에 첫번째 인덱스부터 1,000,000의 범위까지 일일이 비교하는 과정은 시간 오류가 났다.
    
    **해결법** : 먼저 N log N의 시간복잡도를 가진 sort를 사용해서 값들을 오름차순으로 정렬한다. 가장 작은값은 다른 값들과 비교해도 카운트가 0이고 그 다음 작은 값은 제일 작은값보다 1 더 큰값이기 때문에 단순히 제일작은값부터 0에서 i값으로 쭉쭉 매핑시키면 아무리 큰 배열이 들어와도 직선상에서의 매핑된 값만 찾고 그 인덱스만 리턴하면 되니까 시간 초과가 되지 않는다.
    
    1. 중복값을 없애기 위해 직전 문제처럼 집합에 넣었다가 다시 배열로 만들어준다. arr = 원본 배열, set = 오름차순된 배열
    2. mySet 이라는 Map 객체를 만든다. 처음에는 그냥 객체를 만들어서 `[${set[i}]` 에 인덱스를 매칭하려고 했는데 그냥 일반 객체는 키값이 오직 문자열로만 저장된다. 그래서 나중에 원본배열에서 키값을 통해 찾을 때 오류가 발생할 수 있으므로 키값으로 숫자를 지정할 수 있는 map 객체를 사용한다.
    - map 객체의 사용법
        
        ![img](https://prod-files-secure.s3.us-west-2.amazonaws.com/74553f09-e822-477e-abed-c52903d69b9f/d3b81a66-0842-48fd-8a43-501c0f676b23/Untitled.png)
        
    

---

## 문제 #4 실버5

[링크](https://www.acmicpc.net/problem/1181)

![img](https://prod-files-secure.s3.us-west-2.amazonaws.com/74553f09-e822-477e-abed-c52903d69b9f/f6849c94-dbc1-4c59-8002-23001b5e8348/Untitled.png)

- 해설 #4
    
    ![img](https://prod-files-secure.s3.us-west-2.amazonaws.com/74553f09-e822-477e-abed-c52903d69b9f/81945fb4-5122-47b7-b775-be274b818b2f/Untitled.png)
    
    1. 중복을 제거하기 위해 배열을 집합에 넣고 spread 연산자를 통해 객체 안 요소를 전부 풀어 다시 배열로 집어넣었다.
    - 배열 내 중복 제거 후 다시 배열로 만드는 법
        
        ```jsx
        let arr = [1,1,2,3,4,5,6,6]
        arr = [...new Set(arr)]
        ```
        
    1. a.length - b.length = 길이가 짧은순대로 리턴
    2. 길이가 같다면 사전순으로 리턴 → [참고](https://www.notion.so/2-624c3941f78445f585341317e925f1a1?pvs=21) 
    

---
