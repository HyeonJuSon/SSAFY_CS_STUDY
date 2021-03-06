# 📂 Operating System



## ✏️ Question



## [**프로세스와 스레드**](#프로세스와-스레드-답변)

#### 🔍 **프로세스와 스레드를 설명해주세요**

#### 🔍 멀티프로세의와 멀티스레드의 단점을 비교설명하세요**

#### **🔍 스레드 동기화 문제점 구체적으로 말씀해주세요**

#### **🔍 스레드는 어떤 자원을 공유 하나요?**

#### **🔍 스레드의 스택은 독립적으로 할당하는 이유?**

#### **🔍 멀티프로세스 대신 멀티스레드를 사용하는 이유** 

#### **🔍 프로세스의 상태에 대해 설명해주세요**



## **[데드락](#데드락-답변)**

#### 🔍 **데드락이란?**

#### 🔍 **데드락의 발생 조건**

#### 🔍 **데드락 회피기법인 은행원 알고리즘에 대해 설명하세요**

#### 🔍 **데드락의 해결방법에 대해 설명하세요**

#### 🔍 **기아 상태를 설명해주세요**



## [동기 / 비동기](#동기/비동기-답변)

#### 🔍 **동기 / 비동기에 대해 설명해주세요**

#### **🔍 블록킹 / 논블록킹에 대해 설명해주세요**

#### 🔍 비동기 vs 논 블로킹



## [스케줄링](#스케줄링-답변)

#### 🔍 스케줄러를 간략히 설명해주세요

#### 🔍 **스케줄링에 대해 설명해주세요**

#### 🔍 **스케줄링 종류 세가지에 대해 설명해주세요**

#### 🔍 **선점형 스케줄링과 비선점형 스케줄링의 차이에 대해 설명해주세요**

#### 🔍 **CPU 스케줄링 알고리즘 종류에 대해 말해주세요**

#### 🔍 디스패처(Dispatcher)에 대해 설명해주세요

#### 🔍스케줄링 알고리즘 평가 기준을 적으시오



## [캐시의 지역성](#캐시의-지역성-답변)

#### 🔍 **캐시에 대해 설명해주세요**

#### 🔍 시간 지역성과 공간 지역성을 설명해주세요

#### 🔍 **Caching line에 대해 설명해주세요**

#### 🔍**캐시의 사상 기법(Cache Mapping)에 대해서 설명하시오**

#### 🔍**캐시의 쓰기 정책에 대해서 설명하시오**




## [힙/스택 차이](#힙-스택-차이-답변)

#### 🔍 메모리의 영역 4가지에 대해 설명해주세요

#### 🔍 **힙과 스택 영역의 차이에 대해 설명해주세요**

#### 🔍 **힙과 스택의 장단점에 대해 설명해주세요**

#### 🔍 힙 오버플로우와 스택 오버플로우가 왜 발생하나요?

#### 🔍 힙과 스택 각각의 메모리의 크기는 언제 결정되는가



## [메모리-관리](#메모리-관리-답변)

#### 🔍 스와핑이란 무엇인가?

#### 🔍 내부단편화와 외부단편화의 차이 

#### 🔍 교착상태와 기아상태에 대해 비교 설명해주세요

#### 🔍 페이징의 장점과 단점은?

#### 🔍 메모리 단편화 해결 기법에 대해 설명하세요

#### 🔍 페이징과 세그먼테이션의 차이

#### 🔍 페이지 교체 알고리즘 중 한가지를 설명해주세요

#### 🔍 LRU에 대해 설명해주세요

#### 🔍 FIFO알고리즘의 단점에 대해 설명해주세요



## [가상 메모리](#가상-메모리-답변)

#### 🔍 가상메모리란 ?

#### 🔍 페이지 부재에 대해 설명해주세요

#### 🔍 요구 페이징에 대해 설명해주세요



## [프로세스 동기화](#프로세스-동기화-답변)

#### 🔍 임계구역이란?

#### 🔍 임계구역을 해결하는 3가지 조건

#### 🔍 세마포어와 뮤텍스의 차이



## ✏️ Answer



## 프로세스와 스레드 답변

#### 🔍 **프로세스와 스레드를 설명해주세요**

- 프로세스는 현재 실행 중인 프로그램을 말하고, 스레드는 프로세스 내부에서 실행되는 작업 흐름의 단위를 말한다.



#### **🔍 멀티프로세의와 멀티스레드의 단점을 비교설명하세요**

- 멀티 스레드는 멀티 프로세스보다 적은 메모리 공간을 차지하고 문맥 전환이 빠르다 하지만 동기화 문제를 가지고 있고 오류로 인해 하나의 스레드가 종료되면 전체 스레드가 종료될 수 있다.  멀티 프로세스 방식은 하나의 프로세스가 종료되더라도 다른 프로세스는 정상적으로 수행이 가능하지만 멀티 스레드보다 많은 메모리 공간과 CPU 시간을 차지한다.



#### **🔍 스레드 동기화 문제점 구체적으로 말씀해주세요**

- 하나의 자원을 동시에 접근하게 될 때 문제가 발생할 수 있다.



#### **🔍 스레드는 어떤 자원을 공유 하나요?**

- 메모리의 data 영역, code 영역, heap 영역



#### **🔍 스레드의 스택은 독립적으로 할당하는 이유?**

- 스택 메모리 공간이 독립적이라는 것은 독립적인 함수 호출이 가능하다는 것이고 이는 독립적인 실행 흐름이 추가되는 것이다. 따라서 스레드의 정의에 따라 독립적인 실행 흐름을 추가하기 위한 최소 조건으로 독립된 스택을 할당한다.



#### **🔍 멀티프로세스 대신 멀티스레드를 사용하는 이유** 

- 하나의 프로그램 안에서 여러 작업을 해결하기 위해 사용한다. 즉, 프로세스를 생성해서 자원을 할당하는 시스템 콜이 줄어들어 자원을 효율적으로 관리할 수 있고, 스레드 간 통신의 비용이 적기 때문에 통신 부담을 줄일 수 있다.



#### **🔍 프로세스의 상태에 대해 설명해주세요**

- new : 프로세스를 생성하는 단계 

- ready : running 할 준비가 되어 있는 상태, 다음 수행 차례를 기다리는 상태 

- waiting : running 할 준비가 되어 있는 상태, I/O나 다른 이벤트가 발생하는 것을 기다리고 있는 상태

- running : CPU에서 수행이 되고 있는 상태 

- terminated : 프로세스의 실행이 완료되고 할당된 CPU를 반납하는 상태

<hr>


## 데드락 답변

#### 🔍 **데드락이란?**

- 프로세스가 자원을 얻지 못해서 다음 처리를 하지 못하는 상태, 교착상태라고 한다. 한정된 자원을 여러 프로세스에서 사용하려 할 때 발생한다.



#### 🔍 **데드락의 발생 조건**

- 상호 배제 : 한 번에 프로세스 하나만 해당 자원을 사용할 수 있다. 

- 점유 대기 :  자원을 최소한 하나 보유하고, 다른 프로세스에 할당된 자원을 점유하기 위해 대기하는 프로세스가 존재해야 한다. 

- 비선점 : 이미 할당된 자원을 강제로 빼앗을 수 없다. 

- 순환 대기 : 대기 프로세스의 집합이 순환 형태로 지원을 대기하고 있어야 한다.



#### 🔍 **데드락 회피기법인 은행원 알고리즘에 대해 설명하세요**

- 다익스트라가 제안한 방법으로, 프로세스가 자원을 요구할 때 시스템은 자원을 할당한 후에도 안정된 상태로 남아있는지를 사전에 검사하여 교착 상태를 회피하는 기법이다. 안정 상태에만 자원을 할당하고 그렇지 않으면 자원의 해지까지 대기한다.



#### 🔍 **데드락의 해결방법에 대해 설명하세요**

- 예방(Prevention) : 데드락 발생 조건 중 하나를 제거하면서 해결 : 상호 배제, 점유 대기, 비선점, 순환 대기 4가지 조건 중 하나를 제거

- 회피(Avoidance) : 데드락이 발생할 시 피해가는 방법, 은행원 알고리즘이 대표적인 기법

- 탐지 및 회복 : 자원 할당 그래프를 통해 데드락을 감지하며, 만약 데드락을 감지할 경우 이전 상태로 회복, 일부러 데드락을 발생을 허용한 후 감지해서 회복하는 경우도 있음

- 무시 : 데드락 발생을 무시하고 지나감



#### 🔍 **기아 상태를 설명해주세요**

- 특정 프로세스의 우선순위가 낮아서 원하는 자원을 계속 할당 받지 못하는 상태를 말한다. 즉 여러 프로세스가 부족한 자원을 점유하기위해 경쟁할 때 발생한다.

- 해결방법으로는 오래 기다린 프로세스의 우선순위를 높이거나 요청 순서대로 처리하는 요청 큐를 사용 

<hr>


## 동기/비동기 답변

#### 🔍 **동기 / 비동기에 대해 설명해주세요**

- 동기는 request를 보내고 response가 오면 그 다음 요청을 처리하는 방식 즉 요청과 결과가 동시에 이루어지는 것, 비동기는 request를 보내고 response 상관없이 다음 요청을 처리하는 방식



####  **🔍 블록킹 / 논블록킹에 대해 설명해주세요**

- 어플리케이션 실행시 운영체제 대기 큐에 들어가면서 요청에 대한 시스템 콜이 완료된 후에 응답을 보내면 블로킹 (다른 작업을 끝까지 기다렸다 자신의 작업 다시 시작)

- 어플리케이션 실행시 운영체제 대기 큐에 들어가지 않고 실행 여부와 관계없이 바로 응답을 보내면 논 블로킹 (다른 작업과 관계없이 자신의 작업을 계속 진행)



#### 🔍 비동기 vs 논 블로킹

- 시스템 콜이 반환될 때 실행 결과를 함께 반환할 경우 -> 논 블로킹 (시스템 콜의 리턴에 데이터가 포함, 요청한 데이터가 전부 도달 했는지 파악 가능) 

- 시스템 콜이 반환될 때 실행 결과를 함께 반환하지 않는 경우 -> 비동기 (콜백, 이벤트, 시그널 등으로 전달)

<hr>



## 스케줄링 답변

#### 🔍 스케줄러를 간략히 설명해주세요

- 어떤 프로세스에게 자원을 할당할지 결정하는 운영체제의 커널 모듈



#### 🔍 **스케줄링에 대해 설명해주세요**

- CPU나 자원을 효율적으로 사용하기 위한 정책. 프로세스가 생성되어 실행될 때 필요한 시스템의 여러 자원을 해당 프로세스에 할당하는 작업



#### 🔍 **스케줄러 종류 세가지에 대해 설명해주세요**

- 장기 스케줄러 : 작업 스케줄러라고도 불리며 어떤 프로세스를 준비큐에 넣을 것인가를 결정 / (ready)

- 중기 스케줄러 : 너무 많은 프로그램이 동시에 올라가는 것을 조절하는 스케줄러. 여유 공간을 마련하기 위해 프로세스를 메모리에서 디스크로 보내는 역할 

- 단기 스케줄러 : CPU 스케줄러라고도 불리며 준비 상태의 프로세스 중 어떤 프로세스에게 cpu를 할당시켜줄것인지를 결정. CPU와 메모리 사이의 스케줄링을 담당(running)



#### 🔍 **선점형 스케줄링과 비선점형 스케줄링의 차이에 대해 설명해주세요**

- 선점형 스케줄링은 높은 우선순위의 프로세스가 들어오면 현재 프로세스를 중지시키고 높은 우선순위의 프로세스를 처리

- 비선점형 스케줄링은 한 번 할당하면 해당 프로세스가 끝날 때 까지 다른 프로세스를 처리하지 않음



#### 🔍 **CPU 스케줄링 알고리즘 종류를 말해보세요**

- 선입 선처리 스케줄링(First-Come, First-Served Scheduling) 비선점 스케줄링 방식으로 CPU를 먼저 요청하는 프로세스를 우선적으로 할당하는 방식

- 최단 작업 우선 스케줄링 (Shortest-Job-First Scheduling) : CPU burst 길이가 짧은 순서대로 할당하는 방식

- 최소 잔여 시간 우선 스케줄링(shortest remaining time first) : 프로세스의 남은 수행 시간이 짧은 순서에 따라 프로세서에 할당하는 방식

- 라운드 로빈 스케줄링( Round - Roubin Scheduling ) : 프로세스에게 각각 동일한 CPU 할당 시간(타임 슬라이스, quantum)을 부여해서 이 시간 동안만 CPU를 할당하고, 선점형 방식을 사용해 할당 시간 동안 처리를 다 하지 못하면 CPU를 빼앗고 다음 프로세스에게 넘기는 방식

- 우선순위 스케줄링( Priority Scheduling ) : 특정 기준으로 프로세스에게 우선순위를 부여해 우선순위에 따라 프로세서에 할당하는 방식, 우선순위를 정하는 기준으로는 위에서 언급한 SJF, SRTF 알고리즘 등이 있고, 우선순위가 같은 프로세스들은 FCFS 순서로 스케줄링 하는 구조



#### 🔍 **디스패처(Dispatcher)에 대해 설명해주세요**

- 문맥교환을 해주는 모듈을 디스패처라고 한다. (프로세스에게 CPU를 넘겨주는 역할) - 스케줄러가 변경할 프로세스를 선택하면 디스패처가 실제로 변경시키는 역할을 수행한다.

- 디스패처가 하나의 프로세스를 정지하고 다른 프로세스의 수행을 시작하는 데까지 소요되는 시간을 디스패치 지연(dispatch latency)라고 한다. 디스패처는 모든 프로세스의 문맥 교환 시 호출되므로, 디스패치 지연 시간은 가능한 짧아야 한다.



#### 🔍**스케줄링 알고리즘 평가 기준을 적으시오 **

- CPU 사용률 : 전체 시스템 시간 중 CPU가 작업을 처리하는 시간의 비율
- 처리량 : CPU가 단위 시간 당 처리하는 프로세스의 개수
- 응답 시간 : 대화식 시스템에서 요청 후 응답이 오기 시작할 때까지의 시간
- 대기 시간 : 프로세스가 준비 큐 내에서 대기하는 시간의 총합
- 반환 시간 : 프로세스가 시작해서 끝날 떄 까지 걸리는 시간

<hr>




## 캐시의 지역성 답변

#### 🔍 **캐시에 대해 설명해주세요**

- 캐시메모리는 속도가 빠른 장치와 느린 장치간의 속도 차에 따른 병목 현상을 줄이기 위한 범용 메모리로, 메모리와 CPU 간의 속도 차이를 좁히기 위해 CPU가 앞으로 사용할 가능성이 높은 데이터를 미리 가져온다




#### 🔍 시간 지역성과 공간 지역성을 설명해주세요

- 시간 지역성은 한번 참조된 데이터는 잠시 후에 또 참조될 가능성이 높다는 개념이고, 공간 지역성은 데이터 배열에 연속으로 접근할 때 참조된 데이터 근처에 있는 데이터가 잠시 후에 사용될 가능성이 높다는 개념이다.




#### 🔍 Caching line에 대해 설명해주세요

- 캐시가 아무리 가까이 있더라도 찾고자 하는 데이터가 어느 곳에 저장되어 있는지 몰라 모든 데이터를 순회해야 한다면 시간이 오래 걸리게 된다. 즉, 캐시에 목적 데이터가 저장되어 있다면 바로 접근하여 출력할 수 있어야 캐시가 의미 있어진다는 것이다. 그렇기 때문에 캐시에 데이터를 저장할 때 특정 자료구조를 사용하여 묶음으로 저장하게 되는데 이를 캐싱 라인 이라고 한다

- 프로세스는 다양한 주소에 있는 데이터를 사용하므로 빈번하게 사용하는 데이터의 주소 또한 흩어져 있다. 따라서 캐시에 저장하는 데이터에는 데이터의 메모리 주소 등을 기록해 둔 태그를 달아놓을 필요가 있다. 이러한 태그들의 묶음을 캐싱 라인이라고 하고 메모리로부터 가져올 때도 캐싱 라인을 기준으로 가져온다. 종류로는 대표적으로 세 가지 방식이 존재한다.
  - Full Associative
  - Set Associative
  - Direct Map



#### 🔍**캐시의 사상 기법(Cache Mapping)에 대해서 설명하시오**

- CPU의 가상 주소를 물리주소로 변환하여 메모리에 전달하는 기법 

  → 소용량의 캐시 메모리와 상대적 대용량의 중앙 메모리 간 효율적인 메핑을 통해 캐시 적중률(Hit Rate)를 높이기 위한 매커니즘

- 직접 사상 (Direct Mapping)

  메인 메모리를 일정 블록으로 나누고 각 블록을 캐시 메모리의 특정 위치와 매핑하는 방식

  특정 블록 내 데이터가 집중적으로 읽힐 경우, 캐시 실패가 자주 발생하는 단점이 있다.

- 완전 연관 사상(Full Association Mapping)

  메인 메모리의 내용이 캐시 메모리의 어느 위치에나 매핑이 가능한 사상 기법

  캐시 메모리 내 데이터 검색 시 전체 메모리를 스캔해야 하는 제약으로 인해 고가의 메모리 사용 필요

- 집합 연관 사상

  캐시 메모리를 세트로 구성하고 메인 메모리가 세트에 대응되어 세트 내 자유롭게 매핑이 가능한 사상 기법

####  

#### 🔍**캐시의 쓰기 정책에 대해서 설명하시오**

- 데이터 변경 시 캐시 메모리와 메인 메모리의 데이터 저장 시점에 관한 정책
- Write Through
  - 캐시와 주기억장치에 동시 데이터 저장
  - 캐시와 기억장치가 동기화 -> 버스 병목 현상 존재
- Write Back
  - 변경 내용은 캐시에만 기록, Swap out 시 주 기억장치로 복사
  
  - 기억 장치 쓰기 동작을 최소화, 성능에 이저
  
  - 기억 장치와 캐시메모리 간 동기화 이슈 -> 캐시 일관성 프로토콜 
  

<hr>


## 힙 스택 차이 답변

 #### 🔍 메모리의 영역 4가지에 대해 설명해주세요

- 코드 영역 : 실행할 프로그램의 코드

- 데이터 영역 : 전역변수, 정적변수 등 기본적으로 사용되는 변수

- 힙 영역 : 개발자가 동적할당하는 영역

- 스택 영역 : 함수 호출 시 사용되는 매개변수, 지역변수 등



#### 🔍 **힙과 스택 영역의 차이에 대해 설명해주세요**

- 힙은 동적 메모리 구조를 가지며 스택은 정적 메모리 구조를 가짐. 

- 스택 영역은 함수의 호출과 관계되는 변수들이 저장되는 공간으로 함수의 호출과 동시에 할당되고, 함수가 끝나면 해제됨 

- 힙 영역은 스택 영역과 다르게 개발자가 직접 할당과 해제를 관리할 수 있는 영역



#### 🔍 **힙과 스택의 장단점에 대해 설명해주세요**

- 힙은 메모리 크기가 정해져 있지 않아 효율적인 메모리 크기 변경이 가능하나 상대적으로 액세스가 느림 

- 스택은 액세스가 빠르나 메모리 크기를 변경할 수 없음



#### 🔍 힙 오버플로우와 스택 오버플로우가 왜 발생하나요?

- 힙 영역과 스택 영역은 같은 공간을 공유

- 힙이 메모리 위쪽 주소부터 할당되고 스택은 아래쪽부터 할당

- 각 영역이 상대 공간을 침범하는 일이 발생할 수 있는데 이를 각각 힙 오버플로우, 스택오버플로우라고 한다.

  

#### 🔍 힙과 스택 각각의 메모리의 크기는 언제 결정되는가

- 코드, 데이터, 스택은 컴파일 타임에 크기가 결정되며 무한히 할당할 수 없다. 

- 힙은 런타임에 결정되기 때문에 데이터 배열의 크기가 확실하지 않고 변동이 있을때 힙 영역을 활용하여 메모리를 할당한다. 단 사용하고 반드시 해제를 해야한다.  (메모리 부족 발생)

- 힙은 스택보다 할당 가능한 메모리 공간이 많지만 포인터로 접근해야 하기 때문에 비교적 읽고 쓰기에 느리다.



## 메모리 관리 답변

#### 🔍 스와핑이란 무엇인가?

- 메모리 관리를 위해 사용되는 기법
- 프로세스를 불러들이기 위한 공간이 부족할 때 현재 메모리에 적재된 프로세스를 내보내는 작업을 Swap Out, 
  원하는 프로세스를 불러들이는 Swap In 방식으로 나누어진다.



#### 🔍 내부단편화와 외부단편화의 차이 

- 외부 단편화는 메모리에 프로세스가 할당될 만큼 충분한 공간이 존재하지만 공간이 쪼개어져 있기 때문에 프로세스를 넣을 수 없는 것
  -  6kb 공간에 1,3,2,kb 순서대로 할당 1,2kb가 종료되도라도 3kb 프로세스 할당 불가
-  내부 단편화는 프로세스가 필요한 양보다 더 큰 메모리 공간에 할당되어 메모리가 낭비되는 것
  - 6kb공간에 4kb 할당 (2kb 내부 단편) 



#### 🔍 교착상태와 기아상태에 대해 비교 설명해주세요

- 교착 상태는 둘 이상의 프로세스들이 자원을 점유한 상태에서 서로 다른 프로세스가 점유하고 있는 자원을 요구하면서 무한정 기다리는 상황을 말한다.
- 기아상태는 병행 프로세스에서 프로세스가 실행되는 데에 필수적인 자원을 끊임없이 사용하지 못하는 상황이다.



#### 🔍 페이징의 장점과 단점은?

- 장점 : 하나의 프로세스가 사용하는 메모리 공간이 연속적이어야 한다는 제약을 없애 외부 단편화 문제점을 해결할 수 있다.

- 단점 : Mapping과정이 늘어나기 때문에 Trade-Off가 발생할 수 있다.



#### 🔍 메모리 단편화 해결 기법에 대해 설명하세요

- 내부 단편화 해결 – 세그먼테이션
  - 메모리를 서로 크기가 다른 논리적인 블록 단위인 세그먼트로 분할하여 메모리를 할당하는 기법

- 외부 단편화 해결 – 페이징 기법
  - 프로세스를 일정 크기인 페이지로 잘라서 메모리에 적재하는 방식



#### 🔍 페이징과 세그먼테이션의 차이

- 페이징
  -  논리(가상)메모리도 물리 메모리와 마찬가지로 고정된 크기인 프레임 단위 페이지로 나누어 관리하는 것.        
  - 외부 단편화가 없음 / 관리가 쉬움    -
- 세그먼테이션 
  - 페이징과 달리 논리 메모리와 물리 메모리를 같은 크기의 블록이 아닌 서로 다른 크기의 논리적 단위인 세그먼트로 분할        
  - 내부 단편화가 없음 / 관리가 어려움



#### 🔍 페이지 교체 알고리즘 중 한가지를 설명해주세요

-  FIFO : 물리 메모리에 먼저 들어온 페이지 순서대로 교체 시점에 먼저 나가게 되는 알고리즘이다. 가장 구현이 간단하다.
  - 처음부터 활발하게 사용되는 페이지를 교체해서 페이지 부재율을 높이는 부작용을 초래할 수 있다.
  - Belady의 모순
    - 페이지를 저장할 수 있는 페이지 프레임의 갯수를 늘려도 되려 페이지 부재가 더 많이 발생하는 모순이 존재한다.

- OPT : 가장 오랫동안 사용되지 않을 페이지를 찾아서 그 페이지를 교체하는 알고리즘이다.

-  LRU : 최근 가장 오랫동안 사용하지 않은 페이지를 교체한다. 가장 많이 쓰이는 알고리즘이다.

-  LFU : 사용 빈도가 가장 적은 페이지를 교체한다. 바로 불러온 페이지가 교체될 수 있다는 단점.

<hr>



## 가상 메모리 답변

#### 🔍 가상메모리란 ?

- 당장 실행에 필요한 부분만 주기억장치에 저장하고, 당장 필요하지 않은 나머지 부분은 보조기억장치에 넣어 두고 실행하게 하는 방법.

- 실제 메모리를 보조하는 역할로 프로세스 전체가 메모리 내에 올라오지 않더라도 실행이 가능하게 해준다.

  

#### 🔍 페이지 부재에 대해 설명해주세요

- 프로세스가 메인 메모리에 적재되지 않은 페이지를 사용하려는 것을 말하며, 
  페이지 부재가 발생하면 오버헤드가 발생하기 때문에 CPU의 효율을 떨어뜨린다.



#### 🔍 요구 페이징에 대해 설명해주세요

- 프로그램 실행 전에 프로그램 전체를 물리 메모리로 적재하는 대신에 필요한 부분만 적재하는 전략

- 가상 메모리 시스템에서 많이 사용된다. 프로세스 실행에 실제 필요한 페이지들만 메모리로 읽어오기 때문에 시간과 메모리 낭비를 줄일 수 있다.

<hr>



## 프로세스 동기화 답변

#### 🔍 임계구역이란?

- 둘 이상의 스레드가 동시에 접근해서는 안되는 공유 자원 영역
- 한번에 하나의 프로세스만 이용하게끔 보장해주어야 한다.



#### 🔍 임계구역을 해결하는 3가지 조건

- Mutual exclusion(상호배타) 

  - 오직 한 쓰레드만이 진입 가능하다. 한 쓰레드가 임계구역에서 수행 중인 상태에서는 다른 쓰레드는 절대 이 구역에 접근할 수 없다. 

- Progress(진행)

  -  한 임계구역에 접근하는 쓰레드를 결정하는 것은 유한 시간 이내에 이루어져야한다. 

- Bounded waiting(유한대기)

  -  임계구역으로 진입하기 위해 대기하는 모든 쓰레드는 유한 시간 이내에 해당 임계구역으로 진입할 수 있어야 한다. 

    

#### 🔍 세마포어와 뮤텍스의 차이

- 세마포어
  -  프로세스의 동기화 기법으로 공유된 자원에 여러 프로세스가 동시에 접근하는 것을 막는것 
  - count를 부여해서 count 값만큼 프로세스 혹은 스레드가 접근 가능하도록 하는 기법
- 뮤텍스 
  - 스레드의 동기화 기법으로 공유된 자원의 여러 스레드가 동시에 접근하는 것을 막는 것
  - lock/unlock 으로 권한을 가진 프로세스 혹은 스레드만 접근할 수 있도록 하는 기법
- 두 기법 모두 데이터 무결성을 보장할 수 없으며 데드락이 발생할 수 있다.

