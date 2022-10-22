# go-fiber

Fast web app framework Fiber

```
brew install go
go run main.go
```

```
brew install wrk
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

Program main use up to 350.0%, 16.6 CPU time(5s test), 6M RAM when under max load.

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
wrk -t1 -c1 -d5 --latency http://127.0.0.1
Running 5s test @ http://127.0.0.1
  1 threads and 1 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    20.67us    4.45us 163.00us   84.98%
    Req/Sec    46.68k     1.44k   48.84k    76.47%
  Latency Distribution
     50%   20.00us
     75%   22.00us
     90%   24.00us
     99%   38.00us
  236998 requests in 5.10s, 29.38MB read
Requests/sec:  46471.92
Transfer/sec:      5.76MB
```

```
wrk -t2 -c10 -d5 --latency http://127.0.0.1
Running 5s test @ http://127.0.0.1
  2 threads and 10 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency    46.58us   79.94us   8.84ms   98.70%
    Req/Sec    92.32k    14.01k  153.30k    83.00%
  Latency Distribution
     50%   42.00us
     75%   50.00us
     90%   62.00us
     99%  141.00us
  917981 requests in 5.01s, 113.81MB read
Requests/sec: 183202.24
Transfer/sec:     22.71MB
```

```
wrk -t2 -c32 -d5 --latency http://127.0.0.1
Running 5s test @ http://127.0.0.1
  2 threads and 32 connections
  Thread Stats   Avg      Stdev     Max   +/- Stdev
    Latency   205.66us  512.67us  23.15ms   99.21%
    Req/Sec    69.63k    14.82k  147.56k    80.00%
  Latency Distribution
     50%  158.00us
     75%  248.00us
     90%  327.00us
     99%  667.00us
  692702 requests in 5.04s, 85.88MB read
Requests/sec: 137472.38
Transfer/sec:     17.04MB
```