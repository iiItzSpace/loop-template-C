# loop-template-C

A robust console loop template for modern C(23). Built with safe input sanitization, no heap allocations, and portable code that relies only on the C standard library.

***

## Features

- **C23 Native:** Uses `bool`, `true`/`false`, `nullptr`, `static constexpr`, and `[[nodiscard]]`.
- **Zero Allocations:** Operates entirely on an optimized 64-byte stack buffer.
- **Input Sanitization:** In-place bidirectional whitespace trimming (`start`/`end` pointer arithmetic).
- **Overlong Input Handling:** Detects partial reads and automatically drains `stdin` using `getchar()`.
- **Flexible Input:** Handles `Y`, `y`, `yes`, `n`, `no`, leading/trailing spaces, and direct `[Enter]` defaults.

***

## Requirements

- C23 compliant compiler (GCC 14+, Clang 18+)
- CMake 4.2+

***

## Build & Run

### Using CMake

```bash
cmake -B build
cmake --build build
./build/loop_template_C
```

### Manual Compilation

```bash
gcc -std=c23 -Wall -Wextra main.c -o loop_template_C
./loop_template_C
```