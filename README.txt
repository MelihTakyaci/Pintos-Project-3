# my-pintos-tests

**Pintos** is a simple instructional operating system written in C for the 32-bit x86 architecture. This repository contains a complete implementation that passes **all test cases** defined by the original Pintos project.

📚 For background on Pintos, see the original project page:  
http://web.stanford.edu/class/cs140/projects/pintos/pintos.html

---

## 🚀 Features Implemented

This implementation includes all major components and enhancements expected in a modern OS kernel:

- ✅ **Fair Scheduler**
  - Handles both I/O-bound and CPU-bound loads effectively.
- ✅ **Priority Scheduling**
  - Includes **priority donation** to handle priority inversion.
- ✅ **Virtual Memory System**
  - Swapping to disk
  - Memory-mapped files (mmap)
  - Shared read-only pages
- ✅ **Multithreaded File System**
  - Write-back buffer cache
  - Read-ahead mechanism
  - Sparse file support

---

## 🔧 Setup & Build

### Requirements

- GCC with `-m32` support (32-bit toolchain)
- QEMU
- Python 2 or compatible `perl` scripts
- `make`, `gdb`, and standard Unix tools

### Quick Start

```bash
cd src/threads
make check   # Run thread tests

cd ../userprog
make check   # Run user program tests

cd ../vm
make check   # Run virtual memory tests

cd ../filesys
make check   # Run file system tests
