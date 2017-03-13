# galeflow
A powerful, failproof and extensible workflow management tool

Galeflow aims to be a full-feature generic orchestrator and scheduler fullfilling all necessities of several workflows.
***Currently, there's no code yet.*** 

Technologies:
- Rust as core language;
- Lua for extensibles features;
- Postgresql as main database;

Principles when coding:
- Every code should be highly tested and highly testable;
- As less as possible system dependant features, mainly for persistency (e.g. no strong dependency of filesystem);
- Predictable resource usage: no explosion of process, open files, threads or memory allocs. (pools everywhere :-P);
- `Minimize weak dependencies` in the core like web-api's, rpc calls, socket connections, filesystem, etc.
- Some `weak dependependencies` are unavoidable, make them obvious to track, unlockable and asynchronous;

Working around the real-world:
- Separated tooling for database migration and maintence, but it will be embedded in full version;
- We **will** provide replication at some point, and our code design must counting on it;
- There's **no plan to provide scalling**: since galeflow aims to be thin and fast, scalling should not be necessary; Still, our code design must make a transition viable;
