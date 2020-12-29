# go-fiber
Fast web app framework Fiber

```
brew install go
go run main.go
```

```
brew install wrk
```
Program main use up to 350.0%, 16.6 CPU time(5s test), 3M RAM when under max load.

```
wrk -t1 -c1 -d5 --latency http://127.0.0.1
Running 5s test @ http://127.0.0.1
  1 threads and 1 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    36.82us    7.18us 332.00us   92.21%
    Req/Sec    25.73k     1.75k   27.95k    66.67%
  Latency Distribution
     50%   35.00us
     75%   39.00us
     90%   43.00us
     99%   69.00us
  130585 requests in 5.10s, 16.19MB read
Requests/sec:  25609.22
Transfer/sec:      3.17MB
```
```
wrk -t2 -c32 -d5 --latency http://127.0.0.1
Running 5s test @ http://127.0.0.1
  2 threads and 32 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency   238.96us   63.07us   2.08ms   74.81%
    Req/Sec    57.40k     2.46k   62.84k    83.00%
  Latency Distribution
     50%  242.00us
     75%  274.00us
     90%  305.00us
     99%  402.00us
  570836 requests in 5.00s, 70.77MB read
Requests/sec: 114148.82
Transfer/sec:     14.15MB
```
```
Model Name:	MacBook Pro
Processor Name:	Quad-Core Intel Core i7
Processor Speed:	2.9 GHz
Number of Processors:	1
Total Number of Cores:	4
L2 Cache (per Core):	256 KB
L3 Cache:	8 MB
Memory:	16 GB
```
