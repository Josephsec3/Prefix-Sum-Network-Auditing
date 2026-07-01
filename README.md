# High-Speed Network Traffic & Log Analyzer (Prefix Sum Algorithm)

## 🛡️ Cyber Security Context
In Blue Team operations and **SOC (Security Operations Center)** environments, analysts often process massive log files containing millions of network packets. When investigating a potential **DDoS attack** or an unauthorized data exfiltration event, querying the total data volume between specific timestamps (e.g., between minute `L` and minute `R`) using standard loops takes $O(N)$ time, which is too slow for real-time incident response.

This project implements the **Prefix Sum Algorithm** in C++ to achieve **$O(1)$ constant time complexity** for range queries, simulating how modern SIEM systems rapidly calculate packet metrics over massive datasets.

## 🚀 Key Features
* **Optimized I/O Operations:** Utilizes `ios_base::sync_with_stdio(false)` and `cin.tie(nullptr)` for maximum execution speed when parsing large data streams.
* **$O(1)$ Range Queries:** Computes the cumulative traffic weight up to any point, allowing instantaneous data size calculations between any two network log sequences.
* **Memory Efficient:** Uses standard vectors with 64-bit integers (`long long`) to prevent integer overflow during high-volume data simulation.

## 📊 Performance Complexity
* **Preprocessing Time:** $O(N)$ — Performed once when loading the logs.
* **Query Lookup Time:** $O(1)$ — Instantaneous retrieval for each security audit check.

## 🛠️ How to Run
Compile the program using any standard C++ compiler:
```bash
g++ -O3 main.cpp -o analyzer
./analyzer
