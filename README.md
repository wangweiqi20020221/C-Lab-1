### Overview

**Learning Objectives:**

*   Set up your computing environment for the rest of the quarter.
*   Compile and run C code on a Linux environment.
*   Observe C programming behaviors that will preview the topics covered in the later labs.

Be sure to read the [ ![](../images/icon_txt.png) Linux tips](../linux/) page to set up your environment and pick a text editor before starting this lab.  
Instructions on what to do are in the Gradescope quiz along with comments in the starter code.

  

### Code for this lab


```
git clone
```
  

### Instructions

  

#### Editing Code

After acquiring the source file, you will need to open `lab0.c` in your [text editor](../linux/#edit) of choice. See the tutorials if you are unsure how to make edits.

The `lab0.c` file contains a number of comments explaining some basics of C (and their differences from Java). There are five different parts to this lab and you will need to modify or write some lines of code for each one. We recommend keeping a fresh copy of `lab0.c` around for reference (as you may lose track of all the changes you end up making).

In particular, it will be helpful for this lab (and for using C moving forward) if you take a little time to familiarize yourself with [the printf() function](http://www.cplusplus.com/reference/cstdio/printf/), which is used to output formatted messages to the console.

  

#### Compiling Code

The source file `lab0.c` won't do anything by itself; you need a compiler (specifically the GNU C compiler) to generate to an executable from it. The GNU C compiler is available on the [CSE VM](https://www.cs.washington.edu/lab/vms), attu, and the instructional Linux machines in the lab.

Using any one of these machines, open a terminal and execute `gcc -v`. We see:

```
$ gcc -v
Using built-in specs.
COLLECT\_GCC=gcc
COLLECT\_LTO\_WRAPPER=/opt/rh/devtoolset-7/root/usr/libexec/gcc/x86\_64-redhat-linux/7/lto-wrapper
Target: x86\_64-redhat-linux
Configured with: ../configure --enable-bootstrap --enable-languages=c,c++,fortran,lto --prefix=/opt/rh/devtoolset-7/root/usr --mandir=/opt/rh/devtoolset-7/root/usr/share/man --infodir=/opt/rh/devtoolset-7/root/usr/share/info --with-bugurl=http://bugzilla.redhat.com/bugzilla --enable-shared --enable-threads=posix --enable-checking=release --enable-multilib --with-system-zlib --enable-\_\_cxa\_atexit --disable-libunwind-exceptions --enable-gnu-unique-object --enable-linker-build-id --with-gcc-major-version-only --enable-plugin --with-linker-hash-style=gnu --enable-initfini-array --with-default-libstdcxx-abi=gcc4-compatible --with-isl=/builddir/build/BUILD/gcc-7.3.1-20180303/obj-x86\_64-redhat-linux/isl-install --enable-libmpx --enable-gnu-indirect-function --with-tune=generic --with-arch\_32=i686 --build=x86\_64-redhat-linux
Thread model: posix
gcc version 7.3.1 20180303 (Red Hat 7.3.1-5) (GCC)
```
The output tells me a bunch of the configuration options for the my installation of GCC as well as the version number, which is 7.3.1. Assuming that you have saved `lab0.c` somewhere on your machine, navigate to that directory and then use GCC to compile it with the following command:

```
$ gcc -g -Wall -std=c99 -o lab0 lab0.c
```

It's not that important right now for you to know what all of these options do, but `-g` tells the compiler to include debugging symbols, `-Wall` says to print warnings for all types of potential problems, `-std=c99` says to use the C99 standard (now only 19 years old!), `-o lab0` instructs the compiler to output the executable code to a file called `lab0`, and `lab0.c` is the source file being compiled.

During execution of that command, you can safely ignore warning about unused variables if you haven't made any changes yet. This warning would not be shown if you removed `-Wall` from the `gcc` command, but you will want `-Wall` to catch potential errors when you write code yourself.

Having executed the `gcc` command, you should be able to see a file named `lab0` in the same directory:

```
$ ls
lab0  lab0.c
```
  

#### Running Executables

The `lab0` file is an _executable file_, which you can run using the command `./lab0`. You should see:

```
$ ./lab0
Usage: ./lab0 <num>
```

In this case, the executable `lab0` is expecting a _command-line argument_, which is text that is provided to the executable from the command-line when the program is run. In particular, `lab0` wants a number from 1 to 5, corresponding to which part of the lab code you want to run. See `main()` in `lab0.c` for more details. For example (your values of `p` and `q` may differ):

```
$ ./lab0 1
\*\*\* LAB 0 PART 1 \*\*\*
x = 351
y = 410
p = 0x7fffaec6a2ec
q = 0x7fffaec6a2e8
x & x = 351
```
  

#### Checking Your Work

With that, you should have everything you need to complete the assignment. Follow the instructions found on the associated Gradescope quiz; you will want to work on the different parts of the lab in order (from 1 to 5). Each question can be answered and/or verified by appropriate edits to the source code. Note that every time you want to test a code modification, you will need to use the `gcc -g -Wall -std=c99 -o lab0 lab0.c` command to produce an updated `lab0` executable file (**Tip:** Use the up and down keys to scroll through previous terminal commands you've executed).

You can submit each question individually on the Lab 0 submission page in Gradescope. Gradescope will indicate which questions were answered correctly and which were answered incorrectly. You have unlimited tries for each question in this lab.

Most of the code behaviors will seem inexplicable at this point, but our goal is that you will be able to explain to someone else what is going on by the end of this course! =)

  

### Submission

You will not be submitting files for this lab. Submit your answers to github.
