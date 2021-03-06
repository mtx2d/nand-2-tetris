# nand-2-tetris

![Travis (.com) branch](https://img.shields.io/travis/com/ghaiklor/nand-2-tetris/master)
![GitHub](https://img.shields.io/github/license/ghaiklor/nand-2-tetris)

[![GitHub followers](https://img.shields.io/github/followers/ghaiklor.svg?label=Follow&style=social)](https://github.com/ghaiklor)
[![Twitter Follow](https://img.shields.io/twitter/follow/ghaiklor.svg?label=Follow&style=social)](https://twitter.com/ghaiklor)

In this repository, I implement all the tasks from nand2tetris course on Coursera. It contains all the source codes, starting from CPU gates (implemented in HDL language) to high-level language compilers and operating systems.

> Why Bother? Because many CS students don't understand how computers work; because fewer CS programs requires a compilation course; because many computer architecture courses are too detailed; because nothing beats the thrill of creating something from almost nothing; because Nand to Tetris engages students in implementing some of the coolest algorithms, data structures and techniques in applied computer science, and because the typical student feedback in Nand to Tetris courses is "the best course I ever took". (c) nand2tetris.org

## Demo

|      Pong Game       |      Compiler       |      VM Translator       |      Assembler       |
| :------------------: | :-----------------: | :----------------------: | :------------------: |
| ![1][Pong Game Demo] | ![1][Compiler Demo] | ![1][VM Translator Demo] | ![1][Assembler Demo] |

_NOTE:_

- Pong Game (written in Jack language and compiled through all the tool-chain to binary code)
- Compiler (Jack language -> stack-based VM language)
- VM Translator (stack-based VM language -> assembly)
- Assembler (assembly -> binary code)

## Project References

### Project 1: Boolean Logic

> A typical computer architecture is based on a set of elementary logic gates like And, Or, Mux, etc., as well as their bit-wise versions And16, Or16, Mux16, etc. (assuming a 16-bit machine). This project engages you in the construction of a typical set of basic logic gates. These gates form the elementary building blocks from which more complex chips will be later constructed.

[Source code for logical gates](./src/cpu/logical)

[Source code for logical (16 bit) gates](./src/cpu/logical16)

[Source code for plumbing gates](./src/cpu/plumbing)

[Source code for plumbing (16 bit) gates](./src/cpu/plumbing16)

### Project 2: Arithmetic Logical Unit (ALU)

> The centerpiece of the computer's architecture is the CPU, or Central Processing Unit, and the centerpiece of the CPU is the ALU, or Arithmetic-Logic Unit. In this project you will gradually build a set of chips, culminating in the construction of the ALU chip of the Hack computer. All the chips built in this project are standard, except for the ALU itself, which differs from one computer architecture to another.

[Source code for ALU](./src/cpu/alu)

### Project 3: Sequential Chips

> The computer's main memory, also called Random Access Memory, or RAM, is an addressable sequence of n-bit registers, each designed to hold an n-bit value. In this project you will gradually build a RAM unit. This involves two main issues: (i) how to use gate logic to store bits persistently, over time, and (ii) how to use gate logic to locate ("address") the memory register on which we wish to operate.

[Source code for memory gates](./src/cpu/memory)

### Project 4: Machine Language Programming

> Every hardware platform is designed to execute commands in a certain machine language, expressed using agreed-upon binary codes. Writing programs directly in binary code is a possible, yet unnecessary. Instead, we can write such programs using a low-level symbolic language, called assembly, and have them translated into binary code by a program called assembler. In this project you will write some low-level assembly programs, and will be forever thankful for high-level languages like Java and Python. (Actually, assembly programming can be highly rewarding, allowing direct and complete control of the underlying machine.)

[Source code for multiplication of two numbers](./spec/cpu/mult)

[Source code for filling the screen](./spec/cpu/fill)

### Project 5: Computer Architecture

> In previous projects we've built the computer's basic processing and storage devices (ALU and RAM, respectively). In this project we will put everything together, yielding the complete Hack Hardware Platform. The result will be a general-purpose computer that can run programs written in the Hack machine language.

[Source code for Hack Hardware Platform](./src/cpu/computer)

### Project 6: The Assembler

> Low-level machine programs are rarely written by humans. Typically, they are generated by compilers. Yet humans can inspect the translated code and learn important lessons about how to write their high-level programs better, in a way that avoids low-level pitfalls and exploits the underlying hardware better. One of the key players in this translation process is the assembler -- a program designed to translate code written in a symbolic machine language into code written in binary machine language.

[Source code for Hack Assembler (hasm)](./src/hasm)

[Examples of Assembly files hasm can translate](./spec/hasm)

### Project 7: The Virtual Machine

> Java (or C#) compilers generate code written in an intermediate language called byte-code (or IL). This code is designed to run on a virtual machine architecture like the JVM (or CLR). One way to implement such VM programs is to translate them further into lower-level programs written in the machine language of some concrete (rather than virtual) host computer. In projects 7 and 8 we build such a VM translator, designed to translate programs written in the VM language into programs written in the Hack assembly language. The VM language, abstraction, and translation process are described in chapters 7 and 8 of the book. For the purpose of this project, chapter 8 can be ignored.

[Source code for virtual machine code translator](./src/vm)

[Examples of virtual machine code](./spec/vm)

### Project 8: The Virtual Machine II

> We continue building the VM translator - a program that translates programs written in the VM language into programs written in the Hack machine language. This is a respectable chunk of engineering, so we are doing it in two stages. Welcome to stage II.

[Source code for virtual machine code translator](./src/vm)

[Examples of virtual machine code](./spec/vm)

### Project 9: High-Level Programming

> This project introduces Jack - a simple, Java-like, object-based programming language. Before building a Jack compiler in projects 10-11, it makes sense to become familiar with the language itself. That's what we'll do in this project.

[Source code for Mandelbrot Set Renderer](./examples/mandelbrot)

### Project 10: Compiler I - Syntax Analysis

> The Jack compiler, like those of Java and C#, is two-tiered: the compiler's front-end translates from the high-level language to an intermediate VM language; the compiler's back-end translates further from the VM language to the native code of the host platform. In projects 7-8 we've built the compiler's back-end (the VM translator); we now turn to building the compiler's front-end. This development will span two projects: syntax analysis (this project), and code generation (next project). Welcome to syntax analysis.

[Source code for compiler](./src/compiler)

### Project 11: Compiler II - Code Generation

> In this project we complete the construction of the Jack Compiler that we started building in the previous project.

[Source code for compiler](./src/compiler)

### Project 12: The Operating System

> An Operating System (OS) is a collection of software services, designed to close gaps between the computer's hardware and application software. For example, if you use a high-level language to write a program that prompts the user to enter some data using the keyboard, the code generated by the compiler will include (among other things) calls to OS routines that handle keyboard inputs. Therefore, the OS can also be viewed as an extension of a high-level programming language. This is a rather simplistic view of operating systems, but it will suffice for our purpose.

[Source code for OS routines](./src/os)

## License

[MIT License](./LICENSE)

All the materials used here are from [nand2tetris](https://www.nand2tetris.org) course.
Which are shared by [CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/) license.

Also, huge thanks to [Mohan Rajendran](https://github.com/mohanrajendran/nand2tetris).
In times, when I was struggling with implementation details, I was using his implementation as a hint.

[Pong Game Demo]: https://user-images.githubusercontent.com/3625244/67093349-192b7400-f1ba-11e9-92bd-1e96c2f5c850.gif
[Compiler Demo]: https://user-images.githubusercontent.com/3625244/67094267-26e1f900-f1bc-11e9-904a-39ea0e0576fc.gif
[VM Translator Demo]: https://user-images.githubusercontent.com/3625244/67094699-fc447000-f1bc-11e9-8a77-357134ac244a.gif
[Assembler Demo]: https://user-images.githubusercontent.com/3625244/67094945-7a087b80-f1bd-11e9-9f01-2dc2941c422b.gif
