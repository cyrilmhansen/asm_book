# WIP Trying to translate the content to French + RISCV-64 A Gentle Introduction to Assembly Language Programming

This textbook provides a gentle introduction to assembly language
programming. What makes this introduction "gentle" is that it assumes
the reader is already comfortable with C or C++ coding. We use this
assumed knowledge to **bridge** backward towards the low level ISA
(Instruction Set Architecture).

We drive home a very sharp point: C **is** a high level assembly
language *and* assembly language is nothing to be scared about.

## For Whom Is This Book Intended?

As mentioned, if you are already familiar with C (or languages descended
from C such as C++), this book begins with what you already know. Later
chapters dive more deeply into the corners and recesses of the ARM V8
ISA and are suitable for those wishing to master the rich instruction
set of the 64 bit ARM processors.

## Can This Book Be Used In Courses Covering Assembly Language?

Yes, absolutely.

In fact, we would argue that the study of assembly language is extremely
important to the building of competent software engineers. Further, we
would argue that teaching the x86 instruction set is cruel as that ISA
was born in the 1970s and has simply gotten more muddled with age.

The MIPS instruction set is another ISA that is often covered in College
level courses. While  kinder and gentler than the x86 ISA, the MIPS
processor isn't nearly as relevant as the ARM family. Phones, tablets,
laptops and even desktops contain ARM V8 processors making the study of
the ARM ISA far more topical. Perhaps even more "cool".

## Calling Convention Used In This Book

Assembly language programming is quite closely dependent upon the
underlying hardware architecture. The host operating environment plays
an outsized role in determining how assembly language programs are
constructed. A "calling convention" refers to how functions are called
and how parameters are passed.

In this book we will use the ARM LINUX conventions. This means:

* You will need to run a ARM Linux VM on the Macintosh - even on
  ARM-based Macs. Why? Apple. That's why.

* You will need to run WSL (Windows Subsystem for Linux) on ARM-based
  Windows machines. These do exist!

* You will need to run an ARM Linux VM on x86-based Windows machines.

## A Lot of Names

As commendable as the ARM designs are, ARM's naming conventions for
their Intellectual Properties are horrid. In this book, AARCH64 and ARM
V8 are taken to be synonyms for the 64 bit ARM Instruction Set
Architecture (ISA).

It is very difficult to find documentation at the ARM site because they
have *so many versions*, so many names for the same thing and so much
documentation in general. It really can be maddening.

Within the text we will provide germane links as appropriate.

[Here](<https://developer.arm.com/documentation/ddi0596/2021-12?lang=en>)
is a link to "a" main instruction set page.

## Section 1 - Bridging from C / C++ to Assembly Language

We start by providing what we're calling "bridging" from C and C++ to
assembly language. We use the knowledge you already have to learn new
knowledge - how cool is that!

| Chapter | Content |
| ------- | ------- |
| 1 | [Hello World](./section_1/hello_world/README.md) |
| 2 | [If Statements](./section_1/if/README.md) |
| 3 | Loops |
| .... a | [.... While Loops](./section_1/while/README.md) |
| .... b | [.... For Loops](./section_1/for/README.md) |
| .... c | [.... Implementing Continue](./section_1/for/README.md#implementing-a-continue)
| .... d | [.... Implementing Break](./section_1/for/README.md#implementing-a-break)
| 4 | Interludes |
| .... a | [.... Registers](./section_1/regs/README.md) |
| .... b | [.... Load and Store](./section_1/regs/ldr.md) |
| .... c | [.... More About `ldr`](./section_1/regs/ldr2.md) |
| .... d | [.... Register Sizes](./section_1/regs/widths.md) |
| 5 | [`switch`](./section_1/jump_tables/README.md) |
| 6 | Functions |
| .... a | [.... Calling and Returning](./section_1/funcs/README.md) |
| .... b | [.... Passing Parameters](./section_1/funcs/README2.md) |
| .... c | [.... Calling common C runtime functions](./section_1/funcs/README3.md) |
| 7 | [FizzBuzz - a Complete Program](./section_1/fizzbuzz/README.md) |
| 8 | Structs |
| .... a | [.... Alignment](./section_1/structs/alignment.md) |
| .... b | [.... Defining](./section_1/structs/defining.md) |
| .... c | [.... Using](./section_1/structs/using.md) |
|  9 | [`const`](./section_1/const/README.md)
|  10 | [Casting](./section_1/casting/README.md) |

## Section 2 - Floating Point

Floating point operations use their own instructions and their own set
of registers. Therefore, floating point operations are covered in their
own section:

| Chapter | Content |
| ------- | ------- |
| 1 | Floating Point |
| .... a | [.... What Are Floating Point Numbers?](./section_2/float/what.md)
| .... b | [.... Registers (simplified)](./section_2/float/working.md)
| .... c | [.... Literals](./section_2/float/literals.md)
| .... d | [.... `fmov` Not Yet Written](./section_2/float/)
| .... e | [.... Conversion To / From Integers](./section_2/float/rounding.md)
| .... f | [.... Four Basic Operations Not Yet Written](./section_2/float/)
| .... g | [.... Selected Additional Operations Not Yet Written](./section_2/float/)
| .... z | [.... Half Precision Floats](./section_2/float/half.md)

## Section 3 - Bit Manipulation

What would a book about assembly language be without bit bashing?

| Chapter | Content |
| ------- | ------- |
| 1 | Bit Fields |
| .... a | [.... Without Bit Fields](./section_3/bitfields/README.md) |
| .... b | [.... With Bit Fields](./section_3/bitfields/with.md) |
| .... c | [.... Review of Newly Described Instructions](./section_3/bitfields/review.md)

## Section 4 - More Stuff

| Chapter | Content |
| ------- | ------- |
| --- | [Determining string literal lengths for C functions](./more/strlen_for_c/README.md) |

## Projects

[Here](./projects/README.md) are some project specifications to offer a
challenge to your growing mastery.

The [DIRENT](./projects/DIRENT/README.md) project demonstrates how a
complex `struct` can be used in assembly language.

## About The Author

Perry Kivolowitz's career in the Computer Sciences spans just under five
decades. He launched more than 5 companies, mostly relating to hardware,
image processing and visual effects (for motion pictures and
television). Perry received Emmy recognition for his work on the The
Gathering, the pilot episode of Babylon 5. Later he received an Emmy
Award for Engineering along with his colleagues at
[SilhouetteFX, LLC](https://en.wikipedia.org/wiki/SilhouetteFX).
SilhouetteFX is used in almost every significant motion picture for
rotoscoping, paint, tracking, 2D to 3D reconstruction, compositing and
more.

In 1996 Perry received an [Academy Award for Scientific and
Technical Achievement](https://en.wikipedia.org/wiki/Academy_Award_for_Technical_Achievement)
for his invention of Shape Driven Warping and
Morphing. This is the technique responsible for many of the
famous effects in Forrest Gump, Titanic and Stargate.

Twenty twenty two marks Perry's 18th year teaching Computer
Science at the college level,
ten years at the UW Madison and now 8 at Carthage College.

Assembly language is a passion for Perry having worked in the following
ISAs:

* Univac 1100

* Digital Equipment Corporation PDP-11

* Digital Equipment Corporation VAX-11

* Motorola 68000

* ARM beginning with AARCH64

This work is dedicated to my wife Sara and sons Ian and Evan.

### Gratuitous Plug

Perry has created a library of about 200 programming projects
suitable for CS 1, CS 2, Data Structures, Networking, Operating
Systems and Computer Organization classes. If a publisher of
CS text books be interested in purchasing the library, please
reach out.
