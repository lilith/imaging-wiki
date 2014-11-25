It's difficult enough to get efficient code generated from C, let alone C#. Writing our own JIT may be prudent.

* It is possible to [store and execute arbitrary machine instructions](http://stackoverflow.com/questions/959087/is-it-possible-to-execute-an-x86-assembly-sequence-from-within-c ) in C#. (Marshal.AllocHGlobal would need to be used for malloc on mono instead of the WinAPI).
* [asmjit (x86/x64) C++ lib](https://github.com/kobalicek/asmjit)
* [Fasm.NET (32-bit onlt)](https://github.com/ZenLulz/Fasm.NET) for [fasm](http://www.flatassembler.net/) by author of [MemorySharp](https://github.com/ZenLulz/MemorySharp). From [lambda](http://lambda-the-ultimate.org/node/4866
).
* [GNU Lighting is specifically for runtime assembly and abstracting slightly over machine code](http://git.savannah.gnu.org/cgit/lightning.git/tree/)

Given the breadth of any instruction set, it's likely easier to provide a string to an assembler than to wrap an API.

* [llvm-fs](https://github.com/fsprojects/llvm-fs) exposes an F# api to the LLVM IR
* [LLVM.NET](https://github.com/aaronrandolph/LLVM.NET)
