# FRYUR

Systems programmer focused on C++, memory management, low-level architecture, and concurrent execution. I care about where every byte lives and build systems from scratch to prove an understanding of the layers beneath the abstractions.

## Focus Areas

- **Memory Management:** Arena and pool allocators, custom object layout, alignment enforcement, cache-conscious design, and precise ownership/lifetime semantics.
- **Data Structures:** Open-addressing hash tables, append-only logs, on-disk storage formats, lock-free primitives, and crash recovery routines.
- **Systems Architecture:** Clear module boundaries, strict thread-safety guarantees, explicit invariants, and documented trade-offs.
- **Correctness Tooling:** ThreadSanitizer (TSan), AddressSanitizer (ASan), UndefinedBehaviorSanitizer (UBSan), fuzzing, differential testing, and static analysis.

## Featured Projects

### [Curren-memory](https://github.com/FRYUR/Curren-memory)

An embeddable, byte-oriented key-value store built in C++20.

- **Design:** Arena-backed open-addressing index featuring tombstones, load-factor rehashing, and optimized memory alignment.
- **Durability:** CRC-checked append-only log with robust crash recovery and atomic log compaction.
- **Testing:** Validated with sanitizers, a custom `libFuzzer` harness, and randomized differential tests against `std::map`.
- **Documentation:** Comprehensive design document covering physical memory layout, on-disk serialization formats, and durability guarantees.

### [CPP-concurrency](https://github.com/FRYUR/CPP-concurrency)

Low-level concurrent data structures and synchronization primitives implemented in modern C++.

- **Concurrency Engineering:** Lock-free queues, hazard pointers, and memory-reclamation schemes exploring the nuances of the C++ memory model (`std::memory_order`).
- **Performance:** Thread-safe bounded and unbounded buffer implementations explicitly engineered to eliminate false sharing and minimize inter-core cache line contention.
- **Stress Validation:** Rigorously tested under high thread contention using ThreadSanitizer (TSan) and aggressive concurrency stress harnesses.

## Technical Skills

| Domain | Tools & Technologies |
|---|---|
| **Languages** | C++ (17/20/23), C, CMake, Bash |
| **Build & Tooling** | CMake, Clang/GCC, `clang-tidy`, `clang-format`, GitHub Actions (CI/CD) |
| **Debugging & Analysis** | GDB, LLDB, AddressSanitizer, ThreadSanitizer, UndefinedBehaviorSanitizer, Valgrind, `perf` |
| **Verification & Testing** | Unit testing, concurrency stress testing, `libFuzzer`, differential testing, microbenchmarking |
| **Platforms & APIs** | Linux, macOS, POSIX file I/O (`write`, `fsync`, `rename`), low-level multithreading primitives (`std::atomic`, `std::mutex`, condition variables) |

## Currently Exploring

- Memory-mapped (`mmap`) storage engines and page-aligned allocation strategies
- Robin Hood hashing optimizations and probe-length distribution analysis
- Lock-free ring buffers and hardware transactional memory constraints

## Engineering Principles

- **Measure First:** Never claim performance improvements without publishing reproducible benchmarks complete with hardware specifications, compiler flags, and methodology.
- **Explicit Invariants:** State assumptions clearly in code and documentation; enforce them continuously under aggressive scheduling and fuzzing.
- **Radical Simplicity:** Prefer clear, deterministic mechanisms that can be reasoned about and explained end-to-end from source code to machine instructions.

