# Week7 Homework

## malloc challenge

### 実装

- `FREE_LIST_BIN_NUM` : heap の分割数を指定。
- `my_get_index` : size から格納するのに適当な heap の index を返す。 index は size が小さいほど小さい値を返す。分割の仕方を変えるときは、この関数を変更すれば良い。
- `my_malloc` : size が含まれる heap の index を取得し、その index 以上の heap に空きがあれば、その heap に割り当てる。割り当ては best fit で行う。

### 考察

2^(5\*n) ごとに分割: 1178,70,495,40,406,51,3734,72,1896,75,
2^n ごとに分割: 813,70,501,40,256,51,753,72,437,75,

| 分割 | Challenge #1 || Challenge #2 || Challenge #3 || Challenge #4 ||Challenge #5 ||
| | Time [ms]| Utilization [%] | Time [ms]| Utilization [%] | Time [ms]| Utilization [%] | Time [ms]| Utilization [%] | Time [ms]| Utilization [%] |
| :---: | :---: |:---: | :---: |:---: | :---: |:---: | :---: |:---: | :---: |:---: |
| $2^{5n}$ ごと | 1178 | 70 | 495 | 40 | 406 | 51 | 3734 | 72 | 1896 | 75 |
| $2^n$ ごと | 813 | 70 | 501 | 40 | 256 | 51 | 753 | 72 | 437 | 75 |
