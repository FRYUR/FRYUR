# FRYUR

Systems programmer focused on C++, memory management, and low-level architecture.
I like knowing where every byte lives, and I build small projects to prove I understand the layers beneath the abstractions.

## Focus areas

- **Memory management:** arena and pool allocators, object layout, alignment, cache behavior, ownership and lifetime design
- **Data structures:** open-addressing hash tables, append-only logs, on-disk formats, crash recovery
- **Systems architecture:** clear module boundaries, explicit invariants, documented trade-offs
- **Correctness tooling:** sanitizers (ASan/UBSan), fuzzing, differential testing, static analysis

## Featured project

### [Curren-memory](https://github.com/FRYUR/Curren-memory)

An embeddable byte-oriented key-value store in C++20.

- Arena-backed open-addressing index with tombstones and load-factor rehashing
- CRC-checked append-only log with crash recovery and atomic compaction
- Tested with sanitizers, a libFuzzer harness, and randomized differential tests against `std::map`
- Design document covering memory layout, on-disk format, and durability guarantees

## Technical skills

| Area | Tools |
|---|---|
| Languages | C++ (17/20), C, CMake, Bash |
| Build and tooling | CMake, Clang/GCC, clang-tidy, clang-format, GitHub Actions |
| Debugging and analysis | GDB/LLDB, AddressSanitizer, UndefinedBehaviorSanitizer, Valgrind, perf |
| Testing | Unit tests, fuzzing (libFuzzer), differential testing, microbenchmarks |
| Platforms | Linux, macOS, POSIX file I/O (`write`, `fsync`, `rename`) |



## Currently exploring

- mmap-backed storage and page-aligned allocation
- Robin Hood hashing and probe-length analysis
- Lock-free data structures and the C++ memory model

## Principles

- Measure before claiming; publish benchmarks with hardware and flags
- Make invariants explicit and test them
- Prefer simple mechanisms that can be explained end to end


