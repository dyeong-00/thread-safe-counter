# thread-safe-counter

## 1. This code compiled in Linux (ubuntu 18.04)

## 2. Compare performance (mutex vs semaphore)
* ### mutex
<img width="80%" src="https://user-images.githubusercontent.com/79148947/121793553-30469180-cc3b-11eb-9bae-9166083e8e16.png"/>

* ### semaphore
<img width="80%" src="https://user-images.githubusercontent.com/79148947/121793554-32105500-cc3b-11eb-9826-3d0f9a54d3f4.png"/>

## 3. analysis
Mutex is much faster than Semaphore.

This is because of the functions(lock_sem, unlock_sem) that execute the semaphore. These functions declare struct s and modify the variables every time the functions are called. Therefore, they increase the overhead.

Or because of the busy waiting. In busy waiting process keeps checking some condition continuously. It wastes CPU time.  

Binary semaphore is too complex to do simple things. Therefore, it is recommended to use mutex instead of binary semaphore.

### 자동차it융합학과 20193346 선정수

