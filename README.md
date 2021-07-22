# &#128193;이것이 코딩 테스트다 with 파이썬

### &#128198; 210701

##### &#128194; 오늘 내용 정리

1. 다수의 자연수 입력받기
   ex) a,b,c = map(int, input().split()) # split()은 공백으로 구분, 다른 기호로 구분하고 싶으면 .split('/')등으로 추가하면 됨
2. 자연수로 이루어진 배열 입력받기
   ex) a = list(map. int, input().split()) # 위와 비슷함. 그 앞에 list()를 추가하면 배열로 입력받을 수 있음
3. 배열 복사
   ex) a= [1,2,3]
   (1) b=a # 얕은 복사, 이런 식으로 복사하면 b의 값을 바꿨을 때 a의 값도 같이 바뀜
   (2) b=list(a) # 깊은 복사, b의 값을 바꾸어도 a의 값이 변하지 않음
4. 배열 정렬
   ex) a.sort() # 배열을 오름차순으로 정리할 수 있음. 가장 큰 수를 구하기 위해서는 a[n-1]을, 그 다음으로 큰 수를 구하기 위해서는 a[n-2]를 구하면 됨

------

### &#128198; 210705

##### &#128194; 오늘 내용 정리

1. 완전 탐색
   모든 경우의 수를 주저 없이 다 계산하는 해결 방법
2. 시뮬레이션
   문제에서 제시한 알고리즘을 한 단계씩 차례대로 직접 수행하는 방법
3. 알고리즘 문제 중 메모리 제한 염두해 두고 코딩 해야 함
   ex)1,000 > 약 4KB
   1,000,000 > 약 4MB
   1,000,000,000 > 약 40MB 3w
4. 문자에서 특정 값 찾기
   ex) if 'e' in 'example'
   'example'이라는 문자열 내에 문자 'e'가 있는지 검색할 수 있다. (문자 위치가 어디 있든 그 문자를 포함하는지 알려 줌)
5. 문자 > 아스키 기호(숫자) 변환
   ex) ord('a')

------

### &#128198; 210706

##### &#128194; 오늘 내용 정리

1. def 내 글로벌 변수
   함수 안에서 미리 선언한 어떤 변수를 계속 이용하고 싶다면 global을 앞에 붙여 주면 된다
   ex) a=10
   def num(): gobal a
2. 자료구조 기초

> 탐색: 많은 양의 데이터 중 원하는 데이터를 찾는 과정
>
> > 대표 알고리즘: DFS, BFS
> > DFS: Depth-First Search, 깊이우선 탐색, 그래프에서 깊은 부분을 우선으로 탐색하는 알고리즘. 두 가지 방식으로 표현 가능.
> >
> > > 인접 행렬: 2차원 배열, 그래프의 연결 관계를 표현하는 방식 - 2차원 배열에 각 노드가 연결된 형태를 기록하는 방식. 연결되지 않은 노드끼리는 무한의 비용이라고 작성
> > > 인접 리스트: 리스트로 그래프의 연결 관계를 표현하는 방식 - 모든 노드에 연결된 노드에 대한 정보를 차례대로 연결하여 저장
> > > 메모리 측면: 인접 행렬 방식은 노드 개수가 많을 수록 메모리 낭비하게 됨 vs 인접 리스트: 효율적으로 사용 가능
> > > 속도: 인접 행렬 < 인접 리스트(더 느림)
> >
> > BFS:Breadth First Search, 너비 우선 탐색, 가까운 노드부터 탐색하는 알고리즘
> >
> > > 큐 자료 구조에 기초. deque 라이브러리 사용하는 게 좋음. 일반적으로 수행 시간이 DFS보다 좋음
>
> 자료구조: 데이터를 표현하고 관리하고 처리하기 위한 구조
>
> > 스택: 선입후출(FILO)
> > 큐: 선입선출(FIFO)
> >
> > > 큐 구현을 위해서는 deque 라이브러리를 이용해야 함 (from collections import deque)
> > > Deque(데크)는 double-ended queue 의 줄임말로, 앞과 뒤에서 즉, 양방향에서 데이터를 처리할 수 있는 queue형 자료구조
>
> 재귀 함수: 자기 자신을 다시 호출하는 함수
>
> > 문제에서 재귀 함수를 이용하기 위해서는 **재귀 함수가 언제 끝날지 종료 조건을 꼭 명시해야 한다.**

------

### &#128198; 210707

##### &#128194; 오늘 내용 정리

문제 풀이만

------

### &#128198; 210714

##### &#128194; 오늘 내용 정리

1.  정렬

> 정렬: 데이터를 특정한 기준에 따라서 순서대로 나열하는 것. 프로그램을 작성할 때 가장 많이 사용되는 알고리즘 중 하나.
>
> > 선택 정렬: 매번 가장 작은 것을 선택  
> >
> > > 시간복잡도: O(N^2)  
> > > 다른 정렬 알고리즘에 비해 비효율적  
> >
> > 삽입정렬: 특정한 데이터를 적절한 위치에 __삽입__ 하는 정렬. 데이터가 거의 정렬되어 있을 때 효율적임.
> >
> > > 0step부터 n-1step까지를 보면 n개의 원소들은 오름차순으로 정렬되어 있음을 알 수 있다.
> > > 시간복잡도: O(N^2) / 최선의 경우: O(N) # 거의 정렬되어 있을 때  
> >
> > 퀵정렬: 가장 많이 사용하는 알고리즘. __기준을 설정한 다음 큰 수와 작은 수를 교환한 후 리스트를 반으로 나누는 방식으로 동작__  
> >
> > > 피벗이 사용됨. 피벗: 큰 수와 작은 수를 교환할 때 교환하기 위한 기준을 의미함.
> > > 시간복잡도: O(NlogN) / 최악의 경우: O(N^2) # 거의 정렬되어 있을 때  
> >
> > 계수 정렬: 특정한 조건이 부합할 때만 사용할 수 있찌만 매우 빠른 정렬 알고리즘
> >
> > > 시간복잡도: O(N+K)
> > > 비교 기반의 정렬 알고리즘이 아님. 
> > > 단독으로 계수 정렬을 사용하는 문제는 나올 확률 적음. 때에 따라 비효율성 초래할 수 있음.  
> >
> > 파이썬 정렬 라이브러리
> > sorted(), sort() 함수
> >
> > > 퀵 정렬과 동작 방식 비슷한 병합 정렬 기반
> > > 시간복잡도: O(NlogN)  
> > > key 매개변수 입력 받을 수 있음.  
> > >
> > > > key 값은 하나의 함수가 들어가야하고 이는 정렬 기준이 됨

2. 역순으로 정렬하기  
   ex) array=[1,4,6]  
    array = sorted(array,reverse=True)  
    array.sort(reverse=True)  
3. 튜플 형태로 입력 받기
   ex) tuple_data = tuple(map(str, input().split()))  # list -> tuple로 바뀌기만 함  
4. lambda 함수  
   lambda 인자 : 표현식  

------

### &#128198; 210715

##### &#128194; 오늘 내용 정리

1. 배열 안에서 특정 값을 갖는 인덱스 값 찾는 법  
   array.index(value)  
   ex) array.index(3) // 만족하는 값 없으면 에러 발생  

2. 탐색  

> 순차 탐색: 리스트 안에 있는 특정한 데이터를 찾기 위해 앞에서부터 데이터를 하나씩 차례대로 확인하는 방법  
>
> > 시간복잡도: 최악 - O(N)    
>
> 이진 탐색: __찾으려는 데이터와 중간점 위치에 있는 데이터를 반복적으로 비교해서__ 원하는 데이터를 찾는 방법  
>
> > __배열 내부의 데이터가 정렬되어 있어야만 사용할 수 있음__  
> > 시작점, 끝점 중간점이라는 3개의 변수를 사용  
> > 시간복잡도: O(logN)
> > 외우는 것 추천  
>
> 트리 자료구조(주요 특징)
>
> > 트리는 부모 노드와 자식 노드의 관계료 표현됨  
> > 트리의 최상단 노드를 __루트 노드__ 라고 함
> > 트리의 최하단 노드를 __단말 노드__ 라고 함  
> > 트리에서 일부를 떼어내도 트리 구조이며 이를 __서브 트리__ 라고 함  
> > 트리는 파일 시스템과 같이 계층적이고 정렬된 데이터를 다루기에 적합함  
>
> 이진 탐색 트리(특징)  
>
> > 부모 노드보다 왼쪽 자식 노드가 작음  
> > 부모 노드보다 오른쪽 자식 노드가 큼  
> > __왼쪽 자식 노드 < 부모 노드 < 오른쪽 자식 노드__  

3. 빠르게 입력 받기  
   입력 데이터가 많은 문제는 sys 라이브러리의 readline() 함수를 이용하면 됨  
   한 줄 입력 받고 나서 __rstrip()__ 함수를 꼭 호출해야 함  
   enter가 줄바꿈 기호로 입력되는데, 이를 제거하기 위해 사용함  
4. 집합 자료형  
   ex) array = set(map(int, input().split()))

------  
### &#128198; 210721

##### &#128194; 오늘 내용 정리  

1. for문 역순으로 출력하기  
ex) for i in range(n, 0, -1):  

2. 다이나믹 프로그래밍(p.208)  
> 다이나믹 프로그래밍: 메모리 공간을 약간 더 사용하여 연산 속도를 비약적으로 증가시킬 수 있는 방법 중 하나. __동적 계획법__ 이라고도 함  
> 다음과 같은 조건을 만족할 때 사용할 수 있음  
>> 큰 문제를 작은 문제로 나눌 수 있다.  
>> 작은 문제에서 구한 정답은 그것을 포함하는 큰 문제에서도 동일하다.
>> ex) 피보나치 수열  
>    
> 메모제이션(Memoization)기법
>> 다이나믹 프로그래밍을 구현하는 방법 중 한 종류  
>> 한 번 구한 결과를 __메모리 공간에 메모해두고__ 같은 식을 다시 호출하면 메모한 결과를 그대로 가져오는 기법.  
>> 한 번 구한 정보를 __리스트__ 에 저장하여 구현
>>  
>> 시간복잡도: O(N)  
>> 호출할 때 재귀 함수를 사용하면 오버헤드가 발생할 수 있음. 따라서 반복문을 사용하여 오버헤드를 줄일 수 있음  
>> __탑다운 방식__: 큰 문제를 해결하기 위해 작은 문제를 호출- __재귀함수__ 이용  
>> __보텀업 방식__: __반복문__ 을 이용하여 작은 문제부터 답을 도출


3. 질문	&#10067; p.214에서 f(2) f(3) f(4)가 왜 호출이 다시 되는지 모르겠음
    
------  
### &#128198; 210722

##### &#128194; 오늘 내용 정리  

문제 풀이만 진행  
p.223 d[i]를 구하는 식 다시 한 번 살펴보기
    
------    
