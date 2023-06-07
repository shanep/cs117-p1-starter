# Project 1 - Hello World

This assignment is intended to serve as a warm up assignment. We will make sure
that all the correct tools are installed and then we will write the traditional
[Hello World](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program)

## Important Links

- Review the [grading rubric](https://shanepanter.com/cs117/grading-rubric.html)

## Tools

This project requires bash (git bash), cmake, and a C++17 compliant compiler
(GCC, Clang, VC++). All of these tools are already installed on the cs lab
machines for you to use.

### Remote Development (Optional)

There is a way to do remote development using GitHub Codespaces as described
[here](https://shanepanter.com/teaching/vscode-tips-and-tricks.html#_developing_remotely_codespaces).
Codespaces is unsupported by your instructor and only provided for those brave
enough to venture out of the lab environment 😃.

⚠ Be aware that Codespaces only gives you 60 hrs free per month so if you choose
to use Codespaces you may incur some additional costs. The Kount Computer
Tutoring Center (CCP 241) is accessible 24/7 by proxy card to all students
enrolled in CS courses. Machines in the Kount Computer Tutoring Center have all
the software you will need this semester.

## CMake

We will be using CMake in this class. Once CMake is installed it should
automatically  detect your compiler and then enable or disable features base on
what is installed. For example this project will compile with `gcc` but not be
able to take advantage of the address sanitizers that clang has.

- [cmake](https://cmake.org/)
- [clang](https://clang.llvm.org/)

## Task 1 - Write the program

Open the file `main.cpp` and write a main function that outputs "Hello World!"
as described in class.

### Sample output

```bash
shane|(master *=):build$ ./myprogram 
Hello World
```

## Task 2 - Generate Build Files

There are two scripts in the root directory named `clean.sh` and `release.sh`.
One creates a release build to compile your project and the other will delete
all the temporary files that are created during the build process.

Run the `release.sh` script from the terminal to setup your project. Note
that your output will be slightly different than what is shown below because
cmake configures the build system specific to the system that it is running on.

```bash
shane|(master *%=):solution$ ./release.sh
-- The CXX compiler identification is AppleClang 14.0.3.14030022
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /Library/Developer/CommandLineTools/usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done
-- Generating done
-- Build files have been written to: ...
```

## Task 3 - Compile your code

After you have run `release.sh` you can `cd` into the build directory to compile
and run the program.

```bash
shane|(master *%=):build$ make
[ 50%] Building CXX object src/CMakeFiles/myprogram.dir/solution.cpp.o
[100%] Linking CXX executable ../myprogram
[100%] Built target myprogram
```

If your code that you wrote in task 1 was correct you should see a executable
named `myprogram` that you can now run to see the output. If your program did
not compile you will need to return to task 1 and fix your code and then return
to this task to compile your code again. You only need to run the `release.sh`
script once if you are recompiling you can skip Task 2 above.

## Task 4 - Complete the Retrospective

Once you have completed all the tasks open the file **Retrospective.md** and
complete each section that has a TODO label. Reference the grading rubric
for details on how this will be graded.

## Task 5 - Add, Commit, Push your code

Once you are finished you need to make sure that you have pushed all your code
to GitHub for grading! You will not be submitting anything to canvas everything
will be submitted through GitHub as demonstrated in class.
