``` ini

BenchmarkDotNet=v0.13.2, OS=Windows 10 (10.0.19044.2251/21H2/November2021Update)
Intel Core i5-3570K CPU 3.40GHz (Ivy Bridge), 1 CPU, 4 logical and 4 physical cores
.NET SDK=7.0.100
  [Host]     : .NET 7.0.0 (7.0.22.51805), X64 RyuJIT AVX
  Job-ZDIAMS : .NET 7.0.0 (7.0.22.51805), X64 RyuJIT AVX

InvocationCount=1  UnrollFactor=1  

```
|           Method | EntityCount |       Mean |     Error |    StdDev | CacheMisses/Op |   Allocated |
|----------------- |------------ |-----------:|----------:|----------:|---------------:|------------:|
|             Arch |      100000 |   12.08 ms |  0.237 ms |  0.382 ms |         62,393 |      9.7 MB |
|       DefaultEcs |      100000 |  14.638 ms | 0.2001 ms | 0.2870 ms |        174,816 | 15417.45 KB |
|          Entitas |      100000 |  99.232 ms | 1.4946 ms | 1.3980 ms |      1,287,851 | 59021.43 KB |
|           HypEcs |      100000 |  44.893 ms | 0.8285 ms | 0.7749 ms |        360,448 | 45333.15 KB |
|      LeopotamEcs |      100000 |  31.291 ms | 0.5453 ms | 0.5100 ms |        254,225 | 14709.32 KB |
|  LeopotamEcsLite |      100000 |  18.763 ms | 0.1752 ms | 0.1553 ms |        118,511 | 10219.15 KB |
| MonoGameExtended |      100000 |  46.995 ms | 0.6238 ms | 0.5835 ms |        577,946 | 23372.73 KB |
|           RelEcs |      100000 | 115.301 ms | 1.2339 ms | 1.0939 ms |      1,304,166 | 50750.64 KB |
|        SveltoECS |      100000 |  67.121 ms | 1.2610 ms | 2.1752 ms |      1,149,821 |     2.16 KB |
