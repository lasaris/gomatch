Testing
==================
* Only input parsing and matching was tested (no ouptut printing).
* Testing method: <code>time grok -f program.grok</code>, <code>time ./jsonizer</code> (precompiled).
* Each input was measured 5 times, bellow is the highest execution time (user time) reached.

Results
-----------------------------
* 50 patterns, 50 lines of text
 * grok: 0.135s
 * golang: 0.046s
* 100 patterns, 100 lines of text
 * grok: 0.469s
 * golang: 0.086s
* 150 patterns, 150 lines of text
 * grok: 1.045s
 * golang: 0.129s
* 200 patterns, 200 lines of text
 * grok: 1.839s
 * golang: 0.193s
* 250 patterns, 250 lines of text
 * grok: 2.868s
 * golang: 0.275s
* 300 patterns, 300 lines of text
 * grok: 4.138s
 * golang: 0.385s (about 0.33s takes up trie construction + matching, 0.14s matching only)

Testing machine
----------------------------
* OS: Ubuntu 13.10 (saucy) x64, Kernel 3.11.0-12-generic
* CPU: CPU Intel(R) Core(TM)2 Duo P7350 @ 2.00GHz
* Memory: 4GB RAM