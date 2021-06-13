# thread-safe-counter

## 1. This code compiled in Linux (ubuntu 18.04)

## 2. Compare performance (mutex vs semaphore)
* ### mutex
<img width="80%" src="https://user-images.githubusercontent.com/79148947/121793553-30469180-cc3b-11eb-9bae-9166083e8e16.png"/>

* ### semaphore
<img width="80%" src="https://user-images.githubusercontent.com/79148947/121793554-32105500-cc3b-11eb-9826-3d0f9a54d3f4.png"/>

## 3. analysis
mutex is much faster than semaphore
This is because of the code that executes the semaphore.
