# journel

## distributed system

### job scheduler
- [cronsun](https://github.com/shunfei/cronsun)
    - A Distributed, Fault-Tolerant Cron-Style Job System
    - Architecture
    ```                                                 [web]
                                                  |
                                     --------------------------
           (add/del/update/exec jobs)|                        |(query job exec result)
                                   [etcd]                 [mongodb]
                                     |                        ^
                            --------------------              |
                            |        |         |              |
                         [node.1]  [node.2]  [node.n]         |
             (job exec fail)|        |         |              |
          [send mail]<-----------------------------------------(job exec result)
    ```
  - [dkron](https://github.com/victorcoder/dkron)
    - Distributed, fault tolerant job scheduling system 
    - [Reliable Cron across the Planet -- google paper](https://queue.acm.org/detail.cfm?id=2745840)
### auto discovery
- [sleuth](http://ursiform.github.io/sleuth/)
    -  A Go library for master-less peer-to-peer autodiscovery and RPC between HTTP services
    -  [Service autodiscovery in Go with sleuth](http://darian.af/post/master-less-peer-to-peer-micro-service-autodiscovery-in-golang-with-sleuth/)

### kafka-like queue

